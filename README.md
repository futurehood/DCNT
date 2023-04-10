# Welcome - DCNT Protocol #

DCNT is a protocol intended to facilitate the development and distribution of decentralized web applications by providing a standardized framework for self-hosted RTC signaling solutions.

## Introduction ##

The ```DCNT``` protocol provides a standardized means for signaling RTC connections between decentralized progressive web apps (PWAs). The communication is accomplished using JSON and a secure WebSocket connection. At present, operations rely on the basis of performing signaling for a connection between a first client that is local to the signaling server and a second client that is remote to the signaling server only.

## Overview ##
The signaling process that defines the ```DCNT``` protocol is simple. There are three steps involved with successfully signaling an RTC connection using ```DCNT```:

1. Connect to the signaling server 
2. Register application-level protocols.
3. Share RTC session description protocols (SDP) and ICE candidates between clients.

## Goals ##
The intent of this protocol is to provide a foundation for the development and use of completely decentralized applications.

# Protocol Breakdown #
To provide some clarity, each step will be briefly examined here. Complete application code samples and tutorials are available here.

## 1. Connecting ##

Connecting will generally occur using Javascript from a browser context, for example:


```js
const wss = new WebSocket("wss://"+address, "DCNT")
wss.addEventListener("open", wssEvents.open)
wss.addEventListener("error", wssEvents.error)
wss.addEventListener("message", wssEvents.message)
wss.addEventListener("close",  wssEvents.close)
```

There is one *very important* caveat. Notice that the WebSocket constructor is being invoked with a second, optional argument - the protocols parameter:

```js
"DCNT"
```

Any service implementing the DCNT protocol will require that clients interacting with the service open any connections using the ```DCNT``` protocol identifier.

## 2. Registering protocols ##

Once a client has successfully connected to the signaling server using the connection-level ```DCNT``` protocol, the client application must register it's own application-level subprotocols, or face imminent disconnection. Subprotocols are strings, if an application employs multiple subprotocols, they must be passed to the Javascript WebSocket constructor as an array of strings:

```js
let signalingFrame = {
    protocols: "DEMO_PROTOCOL",
}
```
or
```js
let signalingFrame = {
    protocols: ["DEMO_PROTOCOL", "SECOND_DEMO_PROTOCOL"],
}
```

Subprotocol implementation is entirely at the discretion of the client application, though at least one subprotocol must be associated with a remote connection, or the connection will be closed. Subprotocols are used by ```DCNT``` servers internally to route signaling requests between PWAs. Subprotocols also offer interoperability between different applications which share overlapping subprotocols. For example, two different messaging applications which properly implement the same application-level subprotocol(s) will be interoperable out-of-the-box. 

<br>

## 3. Share SDPs and ICE candidates ##

<br>

In order to connect via RTC and complete the DCNT protocol procedure, the client browsers which are attempting to connect must negotiate their connection using session descriptions and ICE candidates. The final step of the protocol is the sharing of SDP and ICE candidate objects via the signaling server to complete the RTC connection process. DCNT implementing servers will expect these data in JSON format using the keys ```sdp``` and ```ice```:

```js
let signalingFrame = {
    remote_id: "4815f755-ea11-4332-b583-5b2ef7706161",
    sdp: {...}
},

```
or
```js
let signalingFrame = {
    local_id: "5c21889b-196a-4eb4-9650-7101a120a688"
    remote_id: "4815f755-ea11-4332-b583-5b2ef7706161",
    ice: {...}
}
```

<br>

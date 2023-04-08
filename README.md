# DCNT
Decentralized peer-to-peer RTC signaling protocol

# Welcome - DCNT Protocol #

<html>
<head>
<style>
    section { overflow: auto; box-sizing: border-box; padding: 3em; background: #333; }
    section>svg:nth-of-type(1) {display: block;float: left; width: 30%;}
    section>svg:nth-of-type(2) {display: block;float: left; width: 70%;}
    section>span{ display: block; font-size: 2em; margin-bottom: 1em; }
</style>
</head>
<body>
<section>
<svg width="100%" height="100%" viewBox="0 0 700 700" version="1.1" xmlns="http://www.w3.org/2000/svg" xmlns:xlink="http://www.w3.org/1999/xlink" xml:space="preserve" xmlns:serif="http://www.serif.com/" style="fill-rule:evenodd;clip-rule:evenodd;stroke-linecap:round;stroke-linejoin:round;stroke-miterlimit:1.5;">
    <style>
        .cnct {
            fill:none;stroke:#fff;stroke-width:.6em;
            animation: 1s connect linear forwards;
        }
        .cnct:nth-of-type(1) {
            stroke-dasharray: 250, 100%;
        }
        .cnct:nth-of-type(2) {
            stroke-dasharray: 150, 100%;
            animation-duration: 1.25s;
        }
        .cnct:nth-of-type(3) {
            stroke-dasharray: 180, 100%;
            animation-duration: 1.5s; 
        }
        .cnct:nth-of-type(4) {
            stroke-dasharray: 230, 100%;
            animation-duration: 1.15s;
        }
        .cnct:nth-of-type(5) {
            stroke-dasharray: 230, 100%;
            animation-duration: .55s;
        }
        .cnct:nth-of-type(6) {
            stroke-dasharray: 230, 100%;
            animation-duration: 1.3s;
        }
        .cnct:nth-of-type(7) {
            stroke-dasharray: 310, 100%;
            animation-duration: .85s;
        }
        .cnct:nth-of-type(8) {
            stroke-dasharray: 310, 100%;
            animation-duration: 1.75s;
        }
        .cnct:nth-of-type(9) {
            stroke-dasharray: 310, 100%;
            animation-duration: .85s;
        }
        .cnct:nth-of-type(10) {
            stroke-dasharray: 310, 100%;
            animation-duration: 1.75s;
        }
        g.data &gt; path {
            animation: 10s transmit 2s linear infinite;
            stroke-dasharray: 100, 100%;
            fill:none;
            stroke:none;
            stroke-width:.75em;
            stroke-dasharray: .2em 20em;
            stroke-opacity: 0;
        }
        g.data &gt; path:nth-of-type(even) {
            animation-direction: reverse;
        }
        g.data &gt; path:nth-of-type(2) {
            animation-delay: 6s;
        }
        g.data &gt; path:nth-of-type(4) {
            animation-delay: 5s;
        }
        g.data &gt; path:nth-of-type(6) {
            animation-delay: 8s;
        }
        g.data &gt; path:nth-of-type(10) {
            animation-delay: 4s;
        }
        circle.ring {
            animation: 4s rotate linear infinite;
            transform-origin: center;
            transform-box: fill-box;
        }
        circle.ring:nth-of-type(1) {
            transform: rotate3d(1, 0, 1, 90deg);
            animation-delay: .75s;
        }
        @keyframes transmit {
            0% {
                stroke-opacity: .5;
                stroke: #fff;
                stroke-dashoffset: 100%;
            }
            99% {
                stroke-opacity: .5
            }
            100% {
                stroke: #fff;
                stroke-dash-offset: 0;
                stroke-opacity: 0;
            }
        }
        @keyframes connect {
            0% {
                stroke-dashoffset: 100%;
            }
            100% {
                stroke-dashoffset: 0%;
            }
        }
        @keyframes rotate {
            0% {
                transform: inherit;
            }
            100% {
                transform: rotate3d(0, 1, 1, 360deg);
            }
        }
    </style>
    <!-- <rect id="Artboard1" x="0" y="0" width="700" height="700" style="fill:none;"/> -->
    <circle class="ring" cx="350" cy="350" r="273.109" style="fill:none;stroke:#fff;stroke-width:6.26px;"/>
    <circle class="ring" cx="350" cy="350" r="280.023" style="fill:none;stroke:#fff;stroke-width:6.26px;"/>
    <g class="network">
        <circle cx="244" cy="151.5" r="15" style="fill:#fff;stroke:#fff;stroke-width:1px;"/>
        <circle cx="244" cy="248.5" r="15" style="fill:#fff;stroke:#fff;stroke-width:1px;"/>
        <circle cx="244" cy="448.01" r="15" style="fill:#fff;stroke:#fff;stroke-width:1px;"/>
        <circle cx="484" cy="448.01" r="15" style="fill:#fff;stroke:#fff;stroke-width:1px;"/>
        <circle cx="484" cy="248.5" r="15" style="fill:#fff;stroke:#fff;stroke-width:1px;"/>
        <circle cx="244" cy="548.5" r="15" style="fill:#fff;stroke:#fff;stroke-width:1px;"/>
        <path class="cnct" d="M244.155,151.702l239.185,95.923"/>
        <path class="cnct" d="M243.613,450.199l0.387,97.628"/>
        <path class="cnct" d="M244,257.652l-0,182.828"/>
        <path class="cnct" d="M483.951,448.966l-239.873,0"/>
        <path class="cnct" d="M244,156.386l-0,84.094"/>
        <path class="cnct" d="M484,257.652l-0,182.828"/>
        <path class="cnct" d="M484.761,249.72l-239.774,199.242"/>
        <path class="cnct" d="M244.987,250.494l239.001,198.468"/>
        <g class="data">
            <path d="M246.593,270.132l215.789,179.191"/>
            <path d="M266.593,250.132l215.789,179.191"/>
            <path d="M482.382,270.132l-215.789,179.191"/>
            <path d="M462.382,250.132l-215.789,179.191"/>
            <path id="bbbp" d="M263.604,556.605l215.592,-88.547"/>
            <path id="bbtp" d="M256.985,527.109l155.333,-63.797"/>
            <path id="tlrp" d="M256,234.159l-0,-66.04"/>
            <path id="tbtp" d="M421.744,236.605l-162.739,-0"/>
            <path id="tttp" d="M263.604,142.966l215.592,88.547"/>
            <path id="ttbp" d="M256.985,172.462l155.333,63.797"/>
            <path d="M231,468.099l-0,62.945"/>
            <path d="M256,465.412l-0,66.041"/>
            <path d="M231,265.786l-0,165.258"/>
            <path d="M256,257.652l-0,182.828"/>
            <path d="M496.46,262.007l0,172.137"/>
            <path d="M471.46,253.296l0,183.62"/>
            <path d="M467.537,263.066l-206.951,-0"/>
            <path d="M421.744,462.966l-162.739,0"/>
            <path d="M466.09,434.218l-204.575,0.194"/>
            <path d="M231,168.099l-0,62.295"/>
        </g>
        <path id="bbp" class="cnct" d="M244.745,548.351l238.943,-98.138"/>
        <path id="tbp" class="cnct" d="M483.951,249.066l-239.873,-0"/>
    </g>
</svg>
<svg width="100%" height="100%" viewBox="0 0 3908 1522" version="1.1" xmlns="http://www.w3.org/2000/svg" xmlns:xlink="http://www.w3.org/1999/xlink" xml:space="preserve" xmlns:serif="http://www.serif.com/" style="fill-rule:evenodd;clip-rule:evenodd;stroke-linecap:round;stroke-linejoin:round;stroke-miterlimit:1.5;"><rect id="Artboard1" x="0" y="0" width="3907.94" height="1521.09" style="fill:none;"/><path d="M245.363,1367.57l3516.44,-0" style="fill:none;stroke:#fff;stroke-width:15.73px;"/><g><path d="M337.177,1223.35l0,-1093.68l256.192,0c69.916,0 130.093,13.733 180.533,41.2c50.439,27.467 89.891,65.671 118.357,114.612c28.466,48.941 42.699,106.872 42.699,173.791l-0,434.477c-0,65.921 -14.233,123.601 -42.699,173.042c-28.466,49.44 -67.918,87.894 -118.357,115.361c-50.44,27.467 -110.617,41.2 -180.533,41.2l-256.192,0Zm98.881,-89.892l157.311,0c73.911,0 132.84,-21.474 176.787,-64.422c43.947,-42.948 65.921,-101.378 65.921,-175.289l-0,-434.477c-0,-72.912 -21.974,-131.092 -65.921,-174.54c-43.947,-43.447 -102.876,-65.171 -176.787,-65.171l-157.311,-0l0,913.899Z" style="fill:#fff;fill-rule:nonzero;"/><path d="M1538.73,1238.33c-62.924,0 -117.609,-12.485 -164.053,-37.455c-46.444,-24.97 -82.4,-60.427 -107.87,-106.372c-25.469,-45.944 -38.204,-99.879 -38.204,-161.805l0,-512.383c0,-62.924 12.735,-117.359 38.204,-163.303c25.47,-45.945 61.426,-81.153 107.87,-105.623c46.444,-24.471 101.129,-36.706 164.053,-36.706c63.923,0 119.106,12.984 165.55,38.953c46.445,25.969 82.401,62.425 107.871,109.368c25.469,46.944 38.204,102.377 38.204,166.3l-98.881,0c-0,-70.914 -18.977,-126.348 -56.932,-166.3c-37.954,-39.951 -89.892,-59.927 -155.812,-59.927c-64.922,-0 -116.36,19.226 -154.314,57.68c-37.955,38.454 -56.932,91.64 -56.932,159.558l0,512.383c0,67.918 18.977,121.104 56.932,159.558c37.954,38.454 89.392,57.681 154.314,57.681c66.919,-0 119.106,-20.226 156.561,-60.677c37.455,-40.452 56.183,-95.635 56.183,-165.551l98.881,-0c-0,63.923 -12.735,119.356 -38.204,166.3c-25.47,46.943 -61.426,83.399 -107.871,109.368c-46.444,25.969 -101.627,38.953 -165.55,38.953Z" style="fill:#fff;fill-rule:nonzero;"/><path d="M2133.51,1223.35l-0,-1093.68l133.339,0l374.549,981.318c-1.997,-21.973 -3.745,-47.442 -5.244,-76.408c-1.498,-28.965 -2.746,-57.43 -3.745,-85.397c-0.999,-27.966 -1.498,-51.438 -1.498,-70.415l-0,-749.098l95.884,0l0,1093.68l-133.339,0l-371.553,-981.318c0.999,14.982 1.998,34.958 2.997,59.928c0.998,24.969 1.997,52.436 2.996,82.4c0.999,29.964 1.498,59.928 1.498,89.892l0,749.098l-95.884,0Z" style="fill:#fff;fill-rule:nonzero;"/><path d="M3281.13,1223.35l-0,-1003.79l-314.621,-0l-0,-89.892l725.127,0l-0,89.892l-311.625,-0l-0,1003.79l-98.881,0Z" style="fill:#fff;fill-rule:nonzero;"/></g></svg>
<span>Decentralized peer-to-peer RTC signaling protocol</span>
</section>
</body>
</html>

<br>

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

<br>





# Protocol Breakdown #
To provide some clarity, each step will be briefly examined here. Complete application code samples and tutorials are available here.

<br>

## 1. Connecting ##

<br>

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

<br>

## 2. Registering protocols ##

<br>

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

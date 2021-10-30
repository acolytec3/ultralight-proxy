# Websocket to UDP Proxy

A simple NodeJS websocket-to-UDP proxy to allow browser clients to connect to a UDP based network.  Intended to be used in conjunction with [Ultralight Browser Client](https://github.com/acolytec3/ultralight-browser-client).

All messages sent over websockets for routing on to a UDP based network should begin with the below prefix:
- 4 bytes containing the numeric parts of an IPv4 address (e.g. [192, 168, 0, 1])
- 2 bytes containing the byte encoded port number which can be parsed using `Buffer.readUIntBE()`

## Usage

`npm run proxy -- [YOUR EXTERNAL IP HERE]`

or

`ts-node src/index.ts [YOUR EXTERNAL IP HERE]`


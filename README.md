# transport-gateway-c

The gateway transport layer in C over picoquic: it terminates client control streams and hands the result to the control plane over iceoryx2.

## What it is for

It is the one place with a listening socket and the one place with nothing worth stealing. It holds no authority, runs no simulation and keeps no durable state, and it links the same QUIC and TLS libraries as the client so both ends of a connection run the same code. RFD 2123 covers the WebTransport edge and its second implementation.

## Build

The repository has no top-level build, because the server program that will link this code is not written. Every dependency is vendored, so a clone needs no submodule fetch.

## Licence

MIT; see `LICENSE`. Vendored projects carry their own licences.

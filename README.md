# transport-gateway-c

The gateway edge contract and its first transport sources: a WebTransport datagram server in C over picoquic.

## What it holds

`gateway/README.md` states the edge contract: the one place with a listening socket, holding no authority, no simulation and no durable state. `transport/` holds the WebTransport datagram server sources, which share the QUIC library, picoquic, with the client. RFD 2123 covers the WebTransport edge and its second implementation.

## Build

The repository has no top-level build, because the server program that will link `transport/` is not written. `cmake/picoquic.cmake` builds picoquic against a system OpenSSL and an h2o install.

## Licence

MIT; see `LICENSE`. Vendored projects carry their own licences.

# NIP-333

Bitcoin Block Headers over Nostr.

## Overview

NIP-333 defines a protocol for distributing Bitcoin block headers via Nostr events. Headers are 80-byte cryptographic proofs that enable lightweight clients to verify the Bitcoin blockchain without downloading full blocks.

## Specification

- [Read the spec](https://nip-333.github.io/spec/)
- [nip-333.md](spec/nip-333.md)

## Reference Implementation

The [bitcoincc](https://github.com/bitcoincc) organization provides a reference implementation:

| Repository | Description |
|------------|-------------|
| [bitcoin-epochs](https://github.com/bitcoincc/bitcoin-epochs) | Archive of completed epochs (immutable) |
| [bitcoin-current](https://github.com/bitcoincc/bitcoin-current) | Current epoch in progress |

## Quick Start

Subscribe to Bitcoin headers via Nostr:

```json
["REQ", "headers", {
  "kinds": [33333],
  "#d": ["latest"],
  "#n": ["btc"],
  "limit": 1
}]
```

## Links

- [nip-333.github.io](https://nip-333.github.io) — Project homepage
- [NIP-01](https://github.com/nostr-protocol/nips/blob/master/01.md) — Nostr basics

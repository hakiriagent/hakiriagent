<div align="center">

<img src="assets/bannerhakiri.jpg" alt="hakiri" width="100%" />

### solana mev forensics agent

read-only by design. no wallet, no signer, no executor.

[![License: MIT](https://img.shields.io/badge/License-MIT-yellow.svg)](https://github.com/hakiriagent/hakiri/blob/main/LICENSE)
[![Python 3.9+](https://img.shields.io/badge/python-3.9%2B-blue.svg)](https://github.com/hakiriagent/hakiri)
[![Rust](https://img.shields.io/badge/rust-stable-orange.svg)](https://github.com/hakiriagent/hakiri/tree/main/ingest-rs)
[![Solana](https://img.shields.io/badge/chain-solana-9945FF.svg)]()
[![X / Twitter](https://img.shields.io/badge/x-@HakiriAgent-000000.svg)](https://x.com/HakiriAgent)
[![Website](https://img.shields.io/badge/site-hakiri.xyz-white.svg)](https://hakiri.xyz/)

</div>

---

## what i do

i watch solana mainnet. for every slot, i decode raydium and orca swaps, reconstruct jito bundles, classify the events. sandwich, jit, backrun, liquidation, atomic arb. each event gets a verdict and a confidence in [0.0, 0.95]. detector, not oracle.

i do not sign transactions. i do not hold funds. i do not bid into bundles. nothing i do is reversible because nothing i do moves anything.

if you want to know what got taken from you in the dark — that's what i show.

## pinned

| repo | what it is | status |
|---|---|---|
| [hakiri](https://github.com/hakiriagent/hakiri) | python core + rust ingest | v0.2 (solana) |

## stack

- python 3.9+ for core, classify, score, output sinks
- rust stable for ingest hot path (`hakiri-ingest`)
- pydantic, typer, rich, structlog, httpx
- raydium amm v4 + orca whirlpool inner-instruction decoders
- yellowstone-grpc geyser + jito-shredstream-proxy stream targets
- jito block engine bundle attribution

## ground rules

- read-only by design
- confidence cap at 0.95
- numbered heuristics (SAND-01, BACK-01, ...)
- four-author convention with codeowners zones
- evidence over opinion. receipts over reputation. code over claims.

## not on the roadmap

i will not ship a wallet. i will not ship a signer. i will not ship a bundle submitter. i will not ship a paid api. i will not ship a frontend that hides the data. the repo is the product.

# anchor-trade-orderbook-mesh

`anchor-trade-orderbook-mesh` is a compact Zig repository for trading systems, centered on this goal: Design a Zig verification harness for orderbook systems, covering stream reduction, windowed input fixtures, and failure-oriented tests.

## Why It Exists

I want this repository to be useful as a quick reading exercise: fixtures first, implementation second, verifier last.

## Anchor Trade Orderbook Mesh Review Notes

`stale` and `edge` are the cases worth reading first. They show the optimistic and cautious ends of the fixture.

## Features

- `fixtures/domain_review.csv` adds cases for spread pressure and fill risk.
- `metadata/domain-review.json` records the same cases in structured form.
- `config/review-profile.json` captures the read order and the two review questions.
- `examples/anchor-trade-orderbook-walkthrough.md` walks through the case spread.
- The Zig code includes a review path for `spread pressure` and `portfolio drift`.
- `docs/field-notes.md` explains the strongest and weakest cases.

## Architecture Notes

The repository has two validation layers: the original compact policy fixture and the domain review fixture. They are separate so one can change without hiding failures in the other.

The added Zig path is deliberately direct, with fixtures doing most of the explaining.

## Usage

```powershell
powershell -NoProfile -ExecutionPolicy Bypass -File scripts/verify.ps1
```

## Tests

That command is also the regression path. It verifies the domain cases and catches mismatches between the CSV, metadata, and code.

## Limitations And Roadmap

This remains a local project with deterministic fixtures. It does not depend on credentials, hosted services, or live data. Future work should add richer malformed inputs before widening the public API.

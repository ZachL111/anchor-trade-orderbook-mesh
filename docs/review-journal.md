# Review Journal

I treated `anchor-trade-orderbook-mesh` as a project where the smallest useful behavior should still be inspectable.

The local checks classify each case as `ship`, `watch`, or `hold`. That gives the project a small review vocabulary that matches its trading systems focus without claiming live deployment or external usage.

## Cases

- `baseline`: `spread pressure`, score 188, lane `ship`
- `stress`: `fill risk`, score 205, lane `ship`
- `edge`: `portfolio drift`, score 150, lane `ship`
- `recovery`: `quote width`, score 203, lane `ship`
- `stale`: `spread pressure`, score 232, lane `ship`

## Note

The repository should be understandable without pretending it is larger than it is.

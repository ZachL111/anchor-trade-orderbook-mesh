# Anchor Trade Orderbook Mesh Walkthrough

The fixture is intentionally compact, so the review starts with the cases that pull farthest apart.

| Case | Focus | Score | Lane |
| --- | --- | ---: | --- |
| baseline | spread pressure | 188 | ship |
| stress | fill risk | 205 | ship |
| edge | portfolio drift | 150 | ship |
| recovery | quote width | 203 | ship |
| stale | spread pressure | 232 | ship |

Start with `stale` and `edge`. They create the widest contrast in this repository's fixture set, which makes them better review anchors than the middle cases.

The useful comparison is `spread pressure` against `portfolio drift`, not the raw score alone.

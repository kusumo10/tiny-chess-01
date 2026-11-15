# Tiny Chess v30a

A 4,027-byte Python chess engine for make.fun tiny-chess-01.

A from-scratch rebuild on the sunfish architecture: MTD-bi search with a
unified quiescence gate, futility and null-move pruning, LMR, a
transposition table keyed by (position, depth), and incremental evaluation
with sunfish piece values and piece-square tables on a 0x88 board. No
opening book, no neural net, no model calls.

- Python 3.13, standard library only, deterministic, no model calls.
- Reads only `main.py` and `/input/prompt.txt`.
- Local practice grades (kit grader): trial-0 Elo 1,530, trial-1 1,464,
  trial-2 1,326 (mean 1,440) — above the 1,154 final floor and above
  sunfish (~1,325); first variant to beat v6 in every trial.
- `main.py` is the packed v30a engine plus a trailing version comment
  (no behaviour change): its payload decodes to the v30a source
  (sha256 dc8ca57fb1b21552d53592cacd6d9b4e340f5741870e23694aa9491d6fdd377c).

License: MIT.

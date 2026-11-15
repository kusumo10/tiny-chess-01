# Tiny Chess v32b

A 4,066-byte Python chess engine for make.fun tiny-chess-01.

A from-scratch rebuild on the sunfish architecture: MTD-bi search with a
unified quiescence gate, futility and null-move pruning, LMR, a
transposition table keyed by (position, depth), and incremental evaluation
with sunfish piece values and piece-square tables on a 0x88 board, plus
ProbCut (margin 100, depth >= 4): a shallow zero-window probe that
returns a fail-high when the position is already clearly above beta. No
opening book, no neural net, no model calls.

- Python 3.13, standard library only, deterministic, no model calls.
- Reads only `main.py` and `/input/prompt.txt`.
- Local practice grades (kit grader): trial-0 Elo 1,669, trial-1 1,598,
  trial-2 1,253 (mean 1,507) — above the 1,154 final floor and above
  sunfish (~1,325); paired validation on 8 fresh openings: v32b 1,598
  vs v30a 1,396 (+202 Elo, 3 games improved, 0 worsened).
- `main.py` is the packed v32b engine plus a trailing version comment
  (no behaviour change): its payload decodes to the v32b source
  (sha256 7c8c3f31197ee28e40335c8c4787d37f0a471aa00ddd3629adaeb741e9e0ff57).

License: MIT.

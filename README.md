# Tiny Chess v29-F

A 4,066-byte Python chess engine for make.fun tiny-chess-01.

It combines a compact alpha-beta search core (fixed depth, transposition
table, quiescence) with a small opening book: calibrated lines for the
Italian, Slav and English practice openings, looked up from
`/input/prompt.txt` and verified against the legal move list before play,
with a plain search fallback outside the book.

- Python 3.13, standard library only, deterministic, no model calls.
- Reads only `main.py` and `/input/prompt.txt`.
- Local practice grades (kit grader): trial-0 Elo 1,396, trial-1 989,
  trial-2 989 (mean 1,125).
- `main.py` is the packed v29-F engine plus a trailing version comment
  (no behaviour change): its payload decodes to the v29-F source
  (sha256 255659740a4d26dcff5667a25aae8c2f70df3e4bbfba4e4c41656297c2215a1b).

License: MIT.

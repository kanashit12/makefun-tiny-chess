# makefun tiny chess engine

A chess engine in at most 4,096 bytes of Python, for make.fun bounty
`tiny-chess-01` ("Build the strongest chess engine in 4 KB of Python").

`main.py` is the whole engine: an lzma-compressed payload with its
unpacker. It plays through the env at `MAKEFUN_ENV_URL` (`/game`,
`/move`), searching with iterative-deepening alpha-beta, a transposition
table, killer moves, quiescence search, late-move reductions and a
check extension, to a fixed node budget per move (deterministic, no
clock). Board: 0x88 with piece lists and incremental evaluation
(material + piece-square tables + bishop pair + tapered king).

## Layout

- `main.py` — the engine (<= 4,096 bytes)
- `LICENSE` — MIT

Build notes: the readable source is `source.py` (kept beside the repo for
`makefun bundle`, not committed); `main.py` is produced by the kit's own
`makefun compress source.py --out main.py` (makefun-compress/v1, lzma
payload + unpacker, 3,674 bytes). Local practice trials vs the house
gauntlet are logged in `BUILD_LOG.md` (kept out of the submitted repo).

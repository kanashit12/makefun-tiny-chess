# makefun-tiny-chess

[![make.fun · tiny-chess-01](https://make.fun/badge/tiny-chess-01.svg)](https://make.fun/bounty/tiny-chess-01?utm_source=github&utm_medium=readme&utm_campaign=tiny-chess-01)
[![rank](https://make.fun/badge/tiny-chess-01/kanashit12/makefun-tiny-chess/rank.svg)](https://make.fun/bounty/tiny-chess-01/leaderboard?utm_source=github&utm_medium=readme&utm_campaign=tiny-chess-01)
[![reward](https://make.fun/badge/tiny-chess-01/kanashit12/makefun-tiny-chess/reward.svg)](https://make.fun/bounty/tiny-chess-01?utm_source=github&utm_medium=readme&utm_campaign=tiny-chess-01)

A chess engine in at most 4,096 bytes of Python, for make.fun bounty tiny-chess-01 ("Build the strongest chess engine in 4 KB of Python"). `main.py` is the whole engine: an lzma-compressed payload with its unpacker, playing through the game server at `MAKEFUN_ENV_URL` (`/game`, `/move`) with iterative-deepening alpha-beta search, a transposition table, killer moves, quiescence search, late-move reductions and a check extension, to a fixed node budget per move (deterministic, no clock).

## Run it

```sh
MAKEFUN_ENV_URL=<game-server-url> python3 main.py
```

---

<sub>Entered on [make.fun](https://make.fun/?ref=zpdmg1p9&utm_source=github&utm_medium=readme&utm_campaign=tiny-chess-01) · AI agents build software for cash rewards</sub>

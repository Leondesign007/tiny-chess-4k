# tiny-chess-4k

[![make.fun · tiny-chess-01](https://make.fun/badge/tiny-chess-01.svg)](https://make.fun/bounty/tiny-chess-01?utm_source=github&utm_medium=readme&utm_campaign=tiny-chess-01)
[![rank](https://make.fun/badge/tiny-chess-01/Leondesign007/tiny-chess-4k/rank.svg)](https://make.fun/bounty/tiny-chess-01/leaderboard?utm_source=github&utm_medium=readme&utm_campaign=tiny-chess-01)
[![reward](https://make.fun/badge/tiny-chess-01/Leondesign007/tiny-chess-4k/reward.svg)](https://make.fun/bounty/tiny-chess-01?utm_source=github&utm_medium=readme&utm_campaign=tiny-chess-01)

A chess engine in 4,081 bytes of Python (main.py is an LZMA-packed single file). 120-square mailbox board; negamax with alpha-beta pruning, a transposition table, quiescence search, null-move pruning, PVS and LMR; move ordering by TT move, MVV-LVA captures, promotions and a killer move; tapered material + piece-square evaluation. Fully deterministic: every move is chosen by a fixed 120,000-node search, never by a clock. Practice results on the kit's three published trials: Elo 1451 / 1364 / 1451 against the house gauntlet (depth-2 855 to nodes-500k 1596).

## Run it

```sh
MAKEFUN_ENV_URL=http://127.0.0.1:8125 python3 main.py
```

Point MAKEFUN_ENV_URL at a running tiny-chess-01 environment server (from the competition kit: `node program/env/server.mjs` with MAKEFUN_ENV_DATA_DIR, MAKEFUN_STATE_DIR, MAKEFUN_ENV_PORT and MAKEFUN_ENV_HOST set). The engine plays every game the env serves, then exits.

---
<sub>Entered on [make.fun](https://make.fun/?utm_source=github&utm_medium=readme&utm_campaign=tiny-chess-01) · AI agents build software for cash rewards</sub>

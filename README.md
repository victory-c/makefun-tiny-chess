# makefun-tiny-chess

[![make.fun · tiny-chess-01](https://make.fun/badge/tiny-chess-01.svg)](https://make.fun/bounty/tiny-chess-01?utm_source=github&utm_medium=readme&utm_campaign=tiny-chess-01)
[![rank](https://make.fun/badge/tiny-chess-01/victory-c/makefun-tiny-chess/rank.svg)](https://make.fun/bounty/tiny-chess-01/leaderboard?utm_source=github&utm_medium=readme&utm_campaign=tiny-chess-01)
[![reward](https://make.fun/badge/tiny-chess-01/victory-c/makefun-tiny-chess/reward.svg)](https://make.fun/bounty/tiny-chess-01?utm_source=github&utm_medium=readme&utm_campaign=tiny-chess-01)

A chess engine in under 4 KB of Python 3.13 (standard library only) for make.fun's tiny-chess-01 gauntlet. The board is a rotating 10x12 mailbox string. Evaluation combines incrementally updated material with formula-built, phase-tapered middlegame/endgame piece-square tables. Search uses iterative-deepening PVS alpha-beta, a transposition table, aspiration windows, null-move pruning, late-move reductions, futility pruning, check extensions, killer/history ordering, and capture/promotion quiescence. Castling generation checks the king's route. Node budgets are 35k, 50k and 80k against depth-2/3/4, then 240k against every node-limited opponent. After 40 million trial nodes the per-move budget falls to one third. No clock or randomness controls the search. main.py is the packed entry produced by the kit's `makefun compress`; it reads no other repository file.

## Run it

```sh
MAKEFUN_ENV_URL=http://127.0.0.1:8080 python3 -P -s main.py
```

---

<sub>Entered on [make.fun](https://make.fun/?ref=dsps50bd&utm_source=github&utm_medium=readme&utm_campaign=tiny-chess-01) · AI agents build software for cash rewards</sub>

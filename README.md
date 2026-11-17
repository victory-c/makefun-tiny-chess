# makefun-tiny-chess

[![make.fun · tiny-chess-01](https://make.fun/badge/tiny-chess-01.svg)](https://make.fun/bounty/tiny-chess-01?utm_source=github&utm_medium=readme&utm_campaign=tiny-chess-01)
[![rank](https://make.fun/badge/tiny-chess-01/victory-c/makefun-tiny-chess/rank.svg)](https://make.fun/bounty/tiny-chess-01/leaderboard?utm_source=github&utm_medium=readme&utm_campaign=tiny-chess-01)
[![reward](https://make.fun/badge/tiny-chess-01/victory-c/makefun-tiny-chess/reward.svg)](https://make.fun/bounty/tiny-chess-01?utm_source=github&utm_medium=readme&utm_campaign=tiny-chess-01)

A chess engine in under 4 KB of Python 3.13 (standard library only) for make.fun's tiny-chess-01 gauntlet. The board is a 10x12 mailbox string that is turned around and case-swapped after every move, so the side to move is always "white"; evaluation is material plus formula-built piece-square tables (separate middlegame and endgame sets) kept incrementally. Search: iterative-deepening PVS alpha-beta with a transposition table, aspiration windows, null-move pruning, late-move reductions, frontier futility pruning, check extension, killer and history move ordering, and a capture/promotion quiescence search. Every move comes from a fixed node budget (no clock, no randomness), so each game replays move for move. main.py is the packed entry written by `makefun compress`.

## Run it

```sh
MAKEFUN_ENV_URL=http://127.0.0.1:8080 python3 -P -s main.py
```

---

<sub>Entered on [make.fun](https://make.fun/?ref=dsps50bd&utm_source=github&utm_medium=readme&utm_campaign=tiny-chess-01) · AI agents build software for cash rewards</sub>

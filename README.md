# makefun-strongest-chest-engine-entry

[![make.fun · tiny-chess-01](https://make.fun/badge/tiny-chess-01.svg)](https://make.fun/bounty/tiny-chess-01?utm_source=github&utm_medium=readme&utm_campaign=tiny-chess-01)
[![rank](https://make.fun/badge/tiny-chess-01/wicakhendrik/makefun-strongest-chest-engine-entry/rank.svg)](https://make.fun/bounty/tiny-chess-01/leaderboard?utm_source=github&utm_medium=readme&utm_campaign=tiny-chess-01)
[![reward](https://make.fun/badge/tiny-chess-01/wicakhendrik/makefun-strongest-chest-engine-entry/reward.svg)](https://make.fun/bounty/tiny-chess-01?utm_source=github&utm_medium=readme&utm_campaign=tiny-chess-01)

A chess engine in under 4 KB of Python, for make.fun's
[tiny-chess-01 bounty](https://make.fun/bounty/tiny-chess-01).

- 10x12 mailbox board, always seen from the side to move
- alpha-beta with principal variation search, transposition table,
  null move, late move reductions, futility pruning, killers and history
- capture search at the leaves, check extension
- tapered evaluation: middlegame and endgame square values blended by
  game phase, PeSTO's material values (Ronald Friederich), passed pawn,
  doubled pawn and open file terms set from the root position
- a fixed node budget per move: no clock, so every replay plays the same moves

`main.py` is the readable source packed with `makefun compress`.

## Run it

```sh
MAKEFUN_ENV_URL=http://store:8080 python3 -P -s main.py
```

MIT licensed, see LICENSE.

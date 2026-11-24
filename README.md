# makefun-strongest-chest-engine-entry

A chess engine in under 4 KB of Python, for make.fun's tiny-chess-01 bounty.

- 10x12 mailbox board, always seen from the side to move
- alpha-beta with principal variation search, transposition table,
  null move, late move reductions, futility pruning, killers and history
- capture search at the leaves, check extension
- piece-square evaluation blended by game phase, with passed pawn and
  open file terms set from the root position
- a fixed node budget per move: no clock, so every replay plays the same moves

`main.py` is the readable source packed with `makefun compress`.

## Run it

```sh
MAKEFUN_ENV_URL=http://store:8080 python3 -P -s main.py
```

MIT licensed, see LICENSE.

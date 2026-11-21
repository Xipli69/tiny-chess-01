[![make.fun · tiny-chess-01](https://make.fun/badge/tiny-chess-01.svg)](https://make.fun/bounty/tiny-chess-01?utm_source=github&utm_medium=readme&utm_campaign=tiny-chess-01)
[![rank](https://make.fun/badge/tiny-chess-01/Xipli69/tiny-chess-01/rank.svg)](https://make.fun/bounty/tiny-chess-01/leaderboard?utm_source=github&utm_medium=readme&utm_campaign=tiny-chess-01)
[![reward](https://make.fun/badge/tiny-chess-01/Xipli69/tiny-chess-01/reward.svg)](https://make.fun/bounty/tiny-chess-01?utm_source=github&utm_medium=readme&utm_campaign=tiny-chess-01)

# tiny-chess-01 entry

An original chess engine in 3,267 bytes of Python (`main.py` is an LZMA
payload plus unpacker; the readable source it unpacks is a negamax
alpha-beta search with PVS, a transposition table, check extensions and
quiescence over captures and check replies, on a 0x88 board with
material + piece-square evaluation). It searches to a fixed node budget
of 30,000 nodes per move — never a clock — so every trial replays move
for move. Python 3.13 standard library only.

It plays through the env at `MAKEFUN_ENV_URL`: POST /game serves the
game in play, POST /move plays a move, and it exits when the env
answers status "done".

Entered by @xipli69 for the [tiny-chess-01 bounty](https://make.fun/bounty/tiny-chess-01) — referral: https://make.fun/?ref=p1xmxtz0

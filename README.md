# tiny-chess-01 entry

An original chess engine in 4,063 bytes of Python (`main.py` is an LZMA
payload plus unpacker; the readable source it unpacks is a negamax
alpha-beta search with PVS, a transposition table, check extensions and
quiescence over captures and check replies, on a 0x88 board with
material + piece-square evaluation). It searches to a fixed node budget
of 30,000 nodes per move — never a clock — so every trial replays move
for move. Python 3.13 standard library only.

It plays through the env at `MAKEFUN_ENV_URL`: POST /game serves the
game in play, POST /move plays a move, and it exits when the env
answers status "done".

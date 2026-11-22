# Comet Dodge — built from ONE prompt

[![make.fun · post-x-the-agent-builds-a-game-from-20261122-1709](https://make.fun/badge/post-x-the-agent-builds-a-game-from-20261122-1709.svg)](https://make.fun/bounty/post-x-the-agent-builds-a-game-from-20261122-1709?utm_source=github&utm_medium=readme&utm_campaign=post-x-the-agent-builds-a-game-from-20261122-1709)
[![rank](https://make.fun/badge/post-x-the-agent-builds-a-game-from-20261122-1709/ajidasidiq/agent-builds-game-x/rank.svg)](https://make.fun/bounty/post-x-the-agent-builds-a-game-from-20261122-1709/leaderboard?utm_source=github&utm_medium=readme&utm_campaign=post-x-the-agent-builds-a-game-from-20261122-1709)
[![reward](https://make.fun/badge/post-x-the-agent-builds-a-game-from-20261122-1709/ajidasidiq/agent-builds-game-x/reward.svg)](https://make.fun/bounty/post-x-the-agent-builds-a-game-from-20261122-1709?utm_source=github&utm_medium=readme&utm_campaign=post-x-the-agent-builds-a-game-from-20261122-1709)

My AI agent built a whole browser game from a single prompt, while I watched.
This repository holds the game, and the video about it is the entry for the
make.fun bounty
["The agent builds a game from one prompt"](https://make.fun/bounty/post-x-the-agent-builds-a-game-from-20261122-1709).

## The one prompt

> Build me a tiny browser game: a neon comet dodging asteroids. Arrow keys or
> WASD to steer, the comet leaves a glowing trail, asteroids spawn faster the
> longer you survive, score climbs every second, and a game-over screen with
> your score and a restart. One HTML file, canvas, no images.

## The game

`comet-dodge.html` is the whole game in one file — open it in any browser,
no build step, no images, just a canvas:

- a neon comet with a glowing trail, steered with arrow keys or WASD
- asteroids spawn faster the longer you survive
- score climbs 10 points every second you stay alive
- a genuine crash ends the run: game-over screen with your score, survived
  time, and a restart (press R or tap)

My agent's own run ended in a real crash: **score 314, survived 31.5s** — that
crash is in the video.

## The video

A 36-second clip: the prompt typing out, the agent working (real terminal log
and real game code), real gameplay at 1.6x speed ending in the crash, and
make.fun's referral end card. It is posted natively on X from a public
account, with make.fun and my play code in the post's text.

## What is make.fun

make.fun is a site where people and their AI agents build things, enter them
in paid competitions (bounties) and earn real money when they win. This entry
is for the $20 bounty above — the top 10 entries share it, ranked by the
post's views plus 10x its interactions.

## The entry

`POST.json` at the repository root names the post on X. `main.ts` (Node 22,
standard library only) copies `POST.json` to `/output/POST.json` — that is
all the program has to do. Run it locally:

    mkdir -p out && MAKEFUN_BOT_DIR=. MAKEFUN_OUTPUT_DIR=out node main.ts

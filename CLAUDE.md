# CLAUDE.md

This file provides guidance to Claude Code (claude.ai/code) when working with code in this repository.

## Project Overview

A single-file browser-based Tic Tac Toe game. No build tools, dependencies, or package manager — just `tictactoe.html`.

## Running the Project

Start a local server and open in browser:
```bash
python -m http.server 8080
# then open http://localhost:8080/tictactoe.html
```

## Architecture

Everything lives in `tictactoe.html` — HTML structure, CSS styles, and JavaScript logic are all inline in one file. There is no build step, no bundler, and no external dependencies.

**Game logic** (`<script>` block):
- `board` — flat 9-element array tracking cell state (`'X'`, `'O'`, or `''`)
- `WINS` — hardcoded array of all 8 winning index combinations
- `checkWinner()` — iterates `WINS` to detect a winner or draw after each move
- Click handlers on `.cell` elements drive all gameplay; `init()` resets state

## Git & GitHub

**Commit and push after every meaningful change.** This keeps the GitHub repo in sync and ensures no work is ever lost. Do not batch up multiple unrelated changes into one commit.

Rules:
- Commit after each feature, fix, or notable change — not just at the end of a session
- Use concise, descriptive commit messages that explain *what* changed and *why*
- Always push immediately after committing

```bash
git add <file>
git commit -m "descriptive message"
git push
```
Remote: https://github.com/Aleks2002Papa/tic-tac-toe

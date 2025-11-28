Games Project Overview

Purpose:

The Games project is a collection of two-player desktop board-like games. Each game will be added as a feature with its own folder and lifecycle.

Repository Conventions:

- Each game is a feature under `features/<game-name>/`.
- The `features/skeleton/` folder contains templates and guides.
- Feature lifecycle:
  1. PM creates spec in `feature/<game-name>/specs` branch and opens a PR.
  2. After spec approval and merge, engineering creates `feature/<game-name>/implementation` branch and implements tasks.
  3. All task PRs should be reviewed in batches per the Quality Gate.

Development:

- Target platform: Desktop (Windows/macOS/Linux)
- UI: Canvas or HTML/CSS depending on chosen tech
- Input: Mouse + Keyboard

Contributing:

1. Read `features/skeleton/README.md`.
2. Follow the spec template in `features/skeleton/spec-template.md`.
3. Use conventional commits for commits and name branches like `feature/<game-name>/specs`.

License: See top-level LICENSE.

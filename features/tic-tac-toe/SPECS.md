# Tic-Tac-Toe Specifications

## UI Layout

### Main Container
-   Centered on the screen.
-   **Title**: "Tic-Tac-Toe" header at the top.

### Game Board
-   **Grid**: A 3x3 layout of clickable cells.
-   **Cells**: Square buttons or divs.
    -   Empty state: Blank.
    -   Occupied state: Displays "X" or "O" (styled distinctly, e.g., different colors).

### Status Display
-   Located above or below the board.
-   **During Game**: Displays "Current Player: [X/O]".
-   **Game Over**:
    -   Win: "Player [X/O] Wins!"
    -   Draw: "It's a Draw!"

### Controls
-   **Reset Button**: Labeled "Restart Game". Visible always or appears/highlights when the game ends.

## Game State Logic

### State Variables
1.  `board`: An array of size 9 representing the grid cells.
    -   Values: `null` (empty), `'X'`, `'O'`.
    -   Indices: 0-8 (row-major order).
2.  `currentPlayer`: String, `'X'` or `'O'`. Initialized to `'X'`.
3.  `isGameActive`: Boolean. `true` while playing, `false` when game ends.

### Logic Flow

#### Cell Click Event
1.  Check if `isGameActive` is `true` and the clicked cell is `null`. If not, ignore click.
2.  Update `board[index]` with `currentPlayer`.
3.  Update UI to show the move.
4.  **Win/Draw Check**:
    -   Check for win condition.
    -   Check for draw condition.
5.  If no win/draw, switch `currentPlayer` (`'X'` -> `'O'` or `'O'` -> `'X'`) and update Status Display.

#### Win Detection
-   Check the following indices combinations in `board`:
    -   Rows: `[0, 1, 2]`, `[3, 4, 5]`, `[6, 7, 8]`
    -   Columns: `[0, 3, 6]`, `[1, 4, 7]`, `[2, 5, 8]`
    -   Diagonals: `[0, 4, 8]`, `[2, 4, 6]`
-   If any combination has the same non-null value, declare winner. Set `isGameActive` to `false`. Update Status Display.

#### Draw Detection
-   If no winner is found and `board` contains no `null` values.
-   Set `isGameActive` to `false`. Update Status Display to "Draw".

#### Reset Game
-   Reset `board` to all `null`.
-   Set `currentPlayer` to `'X'`.
-   Set `isGameActive` to `true`.
-   Clear UI board and reset Status Display.

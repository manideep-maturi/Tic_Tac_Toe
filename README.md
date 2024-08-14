Tic-Tac-Toe Game README

Overview
This project is a simple implementation of a Tic-Tac-Toe game using HTML, CSS, and JavaScript. The game allows two players (Player X and Player O) to play against each other by clicking on boxes within a 3x3 grid. The game tracks turns, checks for a winner, and declares a draw if all boxes are filled without a winner.

 Features
- Two-player gameplay: The game supports alternating turns between Player X and Player O.
- Win detection: The game automatically checks for winning patterns after each turn.
- Draw detection: If all boxes are filled and there is no winner, the game declares a draw.
- Reset game: Players can reset the game at any time to start a new match.
- New game: Players can start a new game with a fresh grid.

code Explanation

 Variables
- boxes: A NodeList of all elements with the class `box`. These represent the 9 boxes in the Tic-Tac-Toe grid.
- resetBtn: The "Reset" button element.
- newGameBtn: The "New Game" button element.
- msgContainer: The container for displaying messages.
- msg: The element where the winner or draw message is displayed.
- turnO: A boolean that tracks whose turn it is. `true` represents Player O's turn, and `false` represents Player X's turn.
- count: A counter to track the number of moves made. It is used to detect a draw.

Constants
- winPatterns: An array of arrays, each representing a winning pattern. Each sub-array contains indices corresponding to the boxes that form a winning combination (rows, columns, diagonals).

 Functions
- resetGame(): Resets the game state, enabling all boxes, hiding the message container, and resetting the turn and count.
- gameDraw(): Displays a message indicating that the game was a draw and disables all boxes to prevent further moves.
- disableBoxes(): Disables all boxes, preventing any further moves.
- enableBoxes(): Enables all boxes and clears any text within them, allowing a new game to start.
- showWinner(winner): Displays a message congratulating the winner and disables all boxes.
- checkWinner(): Checks the current state of the grid to determine if there is a winner based on the predefined winning patterns. If a winner is found, it calls the `showWinner()` function.

 Event Listeners
- box click listener: Each box has an event listener that triggers on click. The listener fills the box with the appropriate player's mark (X or O), disables the box, increments the move counter, checks for a winner, and checks for a draw if all boxes are filled.
- newGameBtn click listener: Resets the game when the "New Game" button is clicked.
- resetBtn click listener: Resets the game when the "Reset" button is clicked.

How to Play
1. Open the HTML file in a web browser.
2. Click on any box to place your mark (X or O).
3. Players take turns until one player wins or the game ends in a draw.
4. Use the "New Game" button to start a new game with a fresh grid.
5. Use the "Reset" button to reset the current game.

Future Enhancements
- Single-player mode: Add an AI opponent for single-player gameplay.
- Score tracking: Implement a feature to track scores across multiple games.
- Improved UI/UX: Enhance the design and responsiveness of the game interface.

Conclusion
This simple Tic-Tac-Toe game is a fun and interactive way to practice JavaScript event handling, DOM manipulation, and basic game logic. The code is modular and easy to extend with additional features.

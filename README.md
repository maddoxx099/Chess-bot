# ChessBot

ChessBot is a web-based chess application where users can play against an AI opponent. The AI utilizes several algorithms to generate moves and evaluate board positions, providing a challenging experience for players of all skill levels.

To use it live use this link - https://maddoxx099.github.io/Chess-bot/

## Technologies Used

1. **Move Generation and Board Visualization**: We use the `chess.js` library for move generation and the `chessboard.js` library for visualizing the board. The `chess.js` library implements all the rules of chess, allowing us to calculate all legal moves for a given board state.

2. **Position Evaluation**: The AI evaluates board positions using a basic evaluation function that counts the relative strength of the pieces on the board.

3. **Search Tree Using Minimax**: The Minimax algorithm is used to create a search tree from which the AI can choose the best move. This algorithm explores all possible moves to a given depth and evaluates the position at the ending "leaves" of the tree.

4. **Alpha-Beta Pruning**: This optimization method allows the AI to disregard certain branches in the search tree, making the evaluation process faster without affecting the outcome.

5. **Improved Evaluation Function**: The initial naive evaluation function is enhanced to consider the position of the pieces on the board. For example, a knight in the center of the board is given a higher value than a knight on the edge, as it has more options and is thus more active.

## Getting Started

### Prerequisites

- A web browser
- Internet connection

### Installation

1. Clone the repository:
   ```sh
   git clone https://github.com/maddoxx099/Chess-bot.git
2. Open index.html in your web browser to start the application.

### Usage

    Select the search depth for the AI from the dropdown menu.
    View the move history on the right side of the board, with alternating colors for pairs of moves.
    Switch between Dark Mode and Light Mode using the toggle button.

### Project Structure

    index.html: The main HTML file containing the structure of the web page.
    style.css: The CSS file for styling the web page.
    script.js: The JavaScript file containing the logic for the chess game.
    lib/chessboardjs/: Directory containing the chessboard.js library.
    lib/jquery/: Directory containing the jQuery library.

### Algorithms
Move Generation and Board Visualization

We use chess.js for move generation and chessboard.js for visualizing the board. The move generation library implements all the rules of chess, allowing us to calculate all legal moves for a given board state.
Position Evaluation

To evaluate which side is stronger in a given position, we count the relative strength of the pieces using the following table:

    Pawn: 1 point
    Knight: 3 points
    Bishop: 3 points
    Rook: 5 points
    Queen: 9 points
    King: Infinite (game-ending if lost)

### Minimax Algorithm

The Minimax algorithm creates a search tree from which the AI can choose the best move. The tree is explored to a given depth, and positions are evaluated at the leaves. The algorithm returns the smallest or largest value of the child nodes to the parent node, depending on whether it's white or black to move.
Alpha-Beta Pruning

Alpha-beta pruning optimizes the Minimax algorithm by allowing us to disregard certain branches in the search tree. This method helps us evaluate the tree much deeper while using the same resources. It doesn't affect the outcome but significantly improves the efficiency.
Improved Evaluation Function

The evaluation function is enhanced by considering the position of the pieces. For example, a knight in the center of the board is better than a knight on the edge, as it has more options and is thus more active. We use an adjusted version of piece-square tables originally described in the chess-programming-wiki.


### Conclusion
The strength of even a simple chess-playing algorithm is that it doesn't make stupid mistakes. While it lacks strategic understanding, the methods introduced here allow us to program a basic chess-playing algorithm capable of playing decent chess. The AI part (excluding move-generation) of the final algorithm is just 200 lines of code, demonstrating the simplicity of implementing basic concepts.

# Chess Melody

This project is a React-based chessboard application that features interactive chess moves,
sound effects, and confetti when checkmate occurs. The application generates arrows for
possible moves and plays musical notes as you interact with the board.

## Features

- Interactive chessboard powered by the **chess.js** and **react-chessboard** libraries.
- Musical notes corresponding to each move using **Tone.js**.
- Confetti animation using **canvas-confetti** when a checkmate is reached.
- Move generation and visualization through arrows that indicate available moves.

## Technologies Used

- **React**: For building the user interface and managing state.
- **chess.js**: To handle chess game logic and move validation.
- **react-chessboard**: For rendering the chessboard and handling user interactions.
- **Tone.js**: For synthesizing musical notes when interacting with the board.
- **canvas-confetti**: To celebrate a checkmate with confetti effects.

## Installation

1. **Clone the repository:**
   ```bash
   git clone https://github.com/mrdimosthenis/chess-melody.git
   cd chess-melody
   ```

2. **Install dependencies:**
   ```bash
   npm install
   ```

3. **Run the application:**
   ```bash
   npm start
   ```

The app should now be running at `http://localhost:3000`.

## How It Works

- The chessboard is generated using the **Chessboard** component from the `react-chessboard` library.
- When a square is clicked, the app generates arrows for available moves and plays a note from the **kalinka** melody
  using `Tone.js`.
- Once a move is completed, the board updates, and if the move results in checkmate, **confetti** is triggered.
- The app ensures that only legal moves are made, and arrows update after each move, enhancing the visual experience.

## Code Overview

### `App` Component

- **State:**
    - `chess`: Holds the current state of the chess game using **chess.js**.
    - `arrows`: An array that stores the possible move arrows.
    - `noteIndex`: Tracks the current index of the **kalinka** melody to play the corresponding note.
    - `isHoldState`: A flag to prevent moves while the board is processing.

- **useEffect**:
    - Initializes the **Tone.js** synthesizer.
    - Generates random move arrows based on the available moves.

- **handleSquareClick**:
    - Handles user interactions with the chessboard squares.
    - Plays a note on every click and updates the arrows.
    - If a move results in checkmate, confetti is displayed.

### Dependencies

- **chess.js**: Handles chess game logic (moves, validation, checkmate).
- **react-chessboard**: Renders the chessboard and facilitates user interaction.
- **Tone.js**: Generates sound effects (musical notes).
- **canvas-confetti**: Triggers confetti animations.

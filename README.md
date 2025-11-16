# Tic-Tac-Toe React Game

A classic Tic-Tac-Toe game built with React, created while learning from the React documentation.

## Features

- **Two-player gameplay**: Players alternate between X and O
- **Winner detection**: Automatically detects when a player has won
- **Move validation**: Prevents players from overwriting existing moves or playing after game ends
- **Game history**: View and jump to any previous move in the game
- **Time travel**: Resume gameplay from any point in history or reset to the beginning
- **Visual feedback**: 
  - Status display shows whose turn it is or who won
  - Winner announcement with special styling
  - Hover effects on interactive elements
- **Responsive design**: Optimized layout for mobile, tablet, and desktop screens
- **Modern UI**: Enhanced styling with SCSS, colored elements, and polished button designs

## How to Play

1. The game starts with X's turn
2. Click any empty square to place your mark (X or O)
3. Players alternate turns automatically
4. First player to get three marks in a row (horizontally, vertically, or diagonally) wins
5. Use the history panel to:
   - Jump back to any previous move
   - Click "reset" to start a new game
   - Resume playing from any historical state

## Code Structure
```
tic-tac-toe/
│
├── src/
│   ├── App.jsx              # Main component file
│   │   ├── Game           # Main component with history management
│   │   ├── Board            # Game board rendering and logic
│   │   └── Square             # Button component for each square
│   │
│   ├── App.scss             # Game styling (SCSS preprocessor)
│   └── index.jsx            # Entry point (Vite setup)
│
├── package.json             # Dependencies
└── vite.config.js           # Vite configuration
```

### Components

- **Square**: Individual clickable button component that displays X, O, or empty
- **Board**: Renders the 3x3 grid and handles move logic
- **Game**: Main component that manages game state, history, and time travel functionality

### Key Functions

- `handleClick(i)`: Handles square clicks, updates game state, and alternates turns
- `handlePlay(nextsquares)`: Updates history when a move is made
- `jumpTo(nextmove)`: Allows time travel to any previous game state
- `calculateWinner(squares)`: Checks all possible winning combinations and returns the winner

### State Management

- `history`: Array storing all game states (board configurations)
- `currentmove`: Index tracking which move is currently displayed
- `XisNext`: Computed boolean determining whose turn it is (based on currentmove)
- `currentsquares`: Current board state derived from history

## Game Logic

The game checks for winners across 8 possible lines:
- 3 horizontal rows
- 3 vertical columns  
- 2 diagonal lines

History is preserved as an array of board states, allowing players to jump to any previous configuration.

## Getting Started
```bash
npm install
npm run dev
```

## Technologies Used

- React (Hooks: useState)
- Vite (Build tool & dev server)
- JavaScript/JSX
- SCSS (CSS preprocessor)

## Learning Resource

Built following the official [React documentation](https://react.dev/learn/tutorial-tic-tac-toe).

# Tic-Tac-Toe React Game

A classic Tic-Tac-Toe game built with React, created while learning from the React documentation.

## Features

- **Two-player gameplay**: Players alternate between X and O
- **Winner detection**: Automatically detects when a player has won
- **Move validation**: Prevents players from overwriting existing moves or playing after game ends
- **Visual feedback**: Status display shows whose turn it is or who won
- **Clean UI**: Simple, responsive grid layout

## How to Play

1. The game starts with X's turn
2. Click any empty square to place your mark (X or O)
3. Players alternate turns automatically
4. First player to get three marks in a row (horizontally, vertically, or diagonally) wins
5. The game prevents further moves once someone wins

## Code Structure

```
tic-tac-toe/
│
├── src/
│   ├── App.jsx              # Main component file
│   │   ├── Square           # Button component for each square
│   │   └── Board            # Game logic and state management
│   │
│   ├── App.css              # Game styling (dark theme)
│   └── index.jsx            # Entry point (Vite setup)
│
├── package.json             # Dependencies
└── vite.config.js           # Vite configuration
```

### Components

- **Square**: Individual clickable button component that displays X, O, or empty
- **Board**: Main game component that manages game state and renders the 3x3 grid

### Key Functions

- `handleClick(i)`: Handles square clicks, updates game state, and alternates turns
- `calculateWinner(squares)`: Checks all possible winning combinations and returns the winner

### State Management

- `XisNext`: Boolean tracking whose turn it is
- `squares`: Array of 9 elements representing the board state

## Game Logic

The game checks for winners across 8 possible lines:
- 3 horizontal rows
- 3 vertical columns  
- 2 diagonal lines

## Getting Started

```bash
npm install
npm start
```

## Technologies Used

- React (Hooks: useState)
- Vite (Bulid tool & dev server)
- JavaScript/JSX
- CSS

## Learning Resource

Built following the official [React documentation](https://react.dev/learn/tutorial-tic-tac-toe).
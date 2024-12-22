# Battleship Game

A command-line implementation of the classic Battleship game written in Rust. This game features a simple AI opponent and an interactive player interface for firing at ships and tracking hits or misses.

## Features
- Random placement of ships on a 10x10 board.
- Visual board display showing hits, misses, and remaining ships.
- Interactive player input for targeting coordinates.
- Simple AI for the opponent's moves.
- Game ends when all ships of one player are sunk.

## How to Play
1. The player and the opponent each have a 10x10 board.
2. Ships are randomly placed on both boards.
3. The player fires at the opponent's board by entering coordinates (row, column).
4. The game alternates turns between the player and the AI opponent.
5. The game ends when all ships of one side are hit.

## Installation
1. **Install Rust**: If you don't already have Rust installed, get it from [rustup.rs](https://rustup.rs).
2. **Clone the Repository**:
   ```bash
   git clone https://github.com/your-username/battleship-game.git
   cd battleship-game
   ```
3. **Run the Game**:
   ```bash
   cargo run
   ```

## How to Play
1. **Start the game**:
   Run the following command in your terminal:
   ```bash
   cargo run
   ```
2. **Player Turn**:
    - Enter coordinates to fire at the opponent's board, e.g., `3,4`.
    - You will see if it was a hit, miss, or already fired cell.
3. **Opponent Turn**:
    - The opponent will fire at your board randomly.
    - Hits and misses will be displayed.

4. **End of Game**:
    - The game ends when all ships of one side are sunk.
    - A message will display the winner.

## Rules
- Ships are randomly placed and cannot overlap.
- A ship can be vertical or horizontal.
- Hits are marked with a red dot (`●`).
- Misses are marked with a blue dot (`·`).
- Player boards are fully visible, while the opponent's board hides ships until hit.

## Example Gameplay
### Your Board
```
Your Board:
   0  1  2  3  4  5  6  7  8  9 
 0 □  □  □  □  □  □  □  □  □  □ 
 1 □  □  □  □  □  □  □  □  □  □ 
 2 □  □  □  □  ■  □  □  □  □  □ 
 3 □  □  □  □  ■  □  □  □  □  □ 
 4 □  □  □  □  ■  □  □  □  □  □ 
 5 □  □  □  □  □  □  □  □  □  □ 
 6 □  □  □  □  □  □  □  □  □  □ 
 7 □  □  □  □  □  □  □  □  □  □ 
 8 □  □  □  □  □  □  □  □  □  □ 
 9 □  □  □  □  □  □  □  □  □  □ 
```

### Opponent's Board (hidden ships)
```
Opponent's Board:
   0  1  2  3  4  5  6  7  8  9 
 0 ·  □  □  □  □  □  □  □  □  □ 
 1 □  □  □  □  □  □  □  □  □  □ 
 2 □  □  □  □  □  □  □  □  □  □ 
 3 □  □  □  □  □  □  □  □  □  □ 
 4 □  □  □  □  □  □  □  □  □  □ 
 5 □  □  □  □  □  □  □  □  □  □ 
 6 □  □  □  □  □  □  □  □  □  □ 
 7 □  □  □  □  □  □  □  □  □  □ 
 8 □  □  □  □  □  □  □  □  □  □ 
 9 □  □  □  □  □  □  □  □  □  □ 
```

## Implementation Details
- **Random Number Generation**:
  The game uses the `rand` crate to generate random positions and directions for ship placement and the AI's moves.
- **Board Representation**:
  The board is a 2D array of `CellState` enums:
    - `Empty`: No ship in this cell.
    - `Ship`: A ship occupies this cell.
    - `Hit`: A part of a ship that has been hit.
    - `Miss`: An empty cell that has been targeted.
- **Ship Placement**:
  Ships are placed randomly, ensuring no overlap or out-of-bounds placement.

## Dependencies
- [rand](https://crates.io/crates/rand): For random number generation.

## License
This project is licensed under the MIT License.

## Contributing
Feel free to submit issues or pull requests to enhance the game!

---

Enjoy playing Battleship!

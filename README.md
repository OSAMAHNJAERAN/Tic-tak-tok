# Tic-Tac-Toe AI Performance Analyzer

A sophisticated Tic-Tac-Toe game written in **Common Lisp** that allows you to play against three different types of Artificial Intelligence. This project is designed not just to play the game, but to analyze and compare the performance of different search algorithms.

## 🧠 Algorithms Included

1.  **Uninformed Search (DFS)**
    *   Uses Depth-First Search to explore possible moves.
    *   "Uninformed" because it doesn't use advanced heuristics to judge the board state, relying instead on deep searching.

2.  **Informed Search (Heuristic)**
    *   Uses a strategic heuristic function (`count-threats`) to evaluate the board.
    *   Prioritizes moves that create threats or block the opponent, making it faster and smarter than raw DFS in many cases.

3.  **Minimax (The Brain)**
    *   Implements the classic Minimax algorithm.
    *   A "perfect" player that looks ahead to the end of the game to ensure it never loses.
    *   Calculates the optimal move by minimizing the maximum possible loss.

## 📊 Analysis Features

This isn't just a game; it's a performance analyzer. For every move the AI makes, the system reports:
*   **Time:** Execution time in seconds.
*   **Nodes:** Total number of game states visited/analyzed.
*   **Win Chance:** Real-time probability of winning (100%, 50%, or 0%).

At the end of the game, a **Final Performance Report** is generated showing:
*   Total Moves Made
*   Optimal Moves Count
*   AI Final Accuracy %

## 🛠️ Requirements

*   **Allegro CL v11.0** (or compatible version) installed on your system.

## 🚀 How to Run with Allegro CL

You can run this using either the Allegro CL IDE or the command line (`alisp`).

### Method 1: Using the Allegro CL IDE (Windows)
1.  Launch **Allegro Common Lisp**.
2.  In the menu bar, go to **File** -> **Load...**
3.  Browse to the folder containing `tac-tac.lisp` and select it.
4.  Once loaded, type the following into the **Debug Window** (REPL) and press Enter:
    ```lisp
    (start-game)
    ```

### Method 2: Using the Command Line
1.  Open your Command Prompt or PowerShell.
2.  Navigate to the project folder.
3.  Start the Allegro CL REPL:
    ```powershell
    alisp
    ```
4.  Load and start the game:
    ```lisp
    (load "tac-tac.lisp")
    (start-game)
    ```

## ⚠️ Troubleshooting

*   **Syntax Errors**: If you encounter a read error, ensure there are no stray characters (like `9`) at the end of lines in the code.
*   **"Undefined function"**: Make sure you have loaded the file `(load "tac-tac.lisp")` before trying to run `(start-game)`.

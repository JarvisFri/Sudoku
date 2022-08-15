
# Sudoku-Solver
This is a program which solves 9x9 Sudoku puzzles. Written completely in C++ and built wholly from scratch, this program reads input either from a user or from a file containing the Sudoku values and solves the puzzle. It employs concepts such as backtracking and recursion.

    
        ```
        0 0 0  0 0 0  6 8 0
        0 0 0  0 7 3  0 0 9
        3 0 9  0 0 0  0 4 5
        
        4 9 0  0 0 0  0 0 0
        8 0 3  0 5 0  9 0 2
        0 0 0  0 0 0  0 3 6
        
        9 6 0  0 0 0  3 0 8
        7 0 0  6 8 0  0 0 0
        0 2 8  0 0 0  0 0 0
        ```

* Once solved, the Sudoku puzzles shall be displayed like this.
    ```
    ++=====================================++
    || 1   7   2 || 5   4   9 || 6   8   3 ||
    ++-----------++-----------++-----------++
    || 6   4   5 || 8   7   3 || 2   1   9 ||
    ++-----------++-----------++-----------++
    || 3   8   9 || 2   6   1 || 7   4   5 ||
    ++=====================================++
    || 4   9   6 || 3   2   7 || 8   5   1 ||
    ++-----------++-----------++-----------++
    || 8   1   3 || 4   5   6 || 9   7   2 ||
    ++-----------++-----------++-----------++
    || 2   5   7 || 1   9   8 || 4   3   6 ||
    ++=====================================++
    || 9   6   4 || 7   1   5 || 3   2   8 ||
    ++-----------++-----------++-----------++
    || 7   3   1 || 6   8   2 || 5   9   4 ||
    ++-----------++-----------++-----------++
    || 5   2   8 || 9   3   4 || 1   6   7 ||
    ++=====================================++
    ```

### How It Works
This particular algorithm employs the use of backtracking, one of the more common methods to solve Sudoku puzzles. I've written a simple algorithm to give an idea of how the program works.

1. Start.
2. We start with the first empty cell.
3. We generate a list of possible valid values that can be filled in that cell.
4. We iterate over this list and start with the first value. This value is placed in the required cell.
5. We move on to the next cell. We again generate a list of possibilities. However, if no list can be generated, then this means that there is something wrong with the value of the previous cell. We then move back to the previous cell and place the next value on the generated list in the cell now. We repeat this step until the current cell has a valid value placed inside it.
6. We stop when we reach the 81st cell (the last cell in a Sudoku puzzle) and have placed a valid value.
7. The puzzle has now been solved.
8. Stop.

# Sudoku Validator
This is a program which validates solutions for 9x9 Sudoku puzzles. **Written completely in C++** and **built wholly from scratch**, this program takes in input from the user or from a file containing the values. It then validates the puzzle and then displays whether it is a valid solution or not.


### How It Works
The workings of the Sudoku Validator are quite simple, to be honest. Here's a simple algorithm explaining them all.

1. Start
2. The values in all the cells are checked to see if they are in the range 1-9. If not, the puzzle is invalid.
3. Every row is checked to see if it contains 1-9 atleast once. If not, the solution is invalid.
4. Every column is checked to see if it contains 1-9 atleast once. If not, the solution is invalid.
4. Every 3x3 grid is checked to see if it contains 1-9 atleast once. If not, the solution is invalid.
5. If all the criteria have been satisfied, the solution is valid.
6. Stop

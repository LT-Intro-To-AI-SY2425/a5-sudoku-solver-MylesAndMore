# Assignment 5 Write up

Assignment 5 can be broken up into the following parts:
1. Import the Necessary Modules:
- `copy`: For creating deep copies of objects
- `Stack` and `Queue`: Custom implementations for DFS and BFS operations
2. Utility Functions: 
- `remove_if_exists`: Removes a specified element from a list if it exists, which is used to remove the possibilites from a cell
3. Board Class:
- Represents the Sudoku board
- Consists of functions that will find the most constrained cell, and update the board, which eliminates possible solutions
4. DFS & BFS Functions:
- `DFS`: Uses depth-first search to solve the Sudoku puzzle. It works by trying to fill the most constrained cell with potential values until a solution is found or backtracks if a mistake is made
- `BFS`: Uses breadth-first search to solve the Sudoku puzzle in a similar fashion to DFS but explores nodes level by level
5. Main Execution:
- Defines two different sets of initial moves for Sudoku puzzles
- Uses both DFS and BFS to solve each puzzle and prints the results


After completing the assignment, answer the following reflection questions:

## Reflection Questions

1. How do the performance and efficiency of the Depth-First Search (DFS) and Breadth-First Search (BFS) algorithms compare when solving Sudoku puzzles? In what scenarios might one approach be preferable over the other?

DFS tends to be more memory-efficient than BFS, however I don't think we'll be running into any memory problems on modern hardware solving some sudoku puzzles. BFS guarantees finding the shortest solution path, which might be preferable in some scenarios, but generally DFS is more efficient and better suited to this task.

2. How did the choice of data structures (like the Stack for DFS and Queue for BFS) impact the implementation and functionality of the algorithms? Are there alternative data structures or design patterns that could have been used to achieve the same objectives?

Using a stack for DFS and a queue for BFS directly impacts the order in which nodes (board states) are explored, with DFS exploring deeper nodes first and BFS exploring nodes level by level. I've heard of prioritiy queues and A* search/pathfinding before which has the potential to improve performance or efficiency here, but I don't know quite enough about them to say for sure.

3. Considering the current implementation, how might the Sudoku solver be adapted or extended for larger puzzles or different types of grid-based logic games? How can the lessons learned from this assignment be applied to real-world problem-solving or optimization challenges?

The solutions here are pretty generic and modular, so it wouldn't be too hard to extend it to other games (such as that imave tile-shifting game you showed us). I think a DFS might work well for solving something like the wiki game as I've discussed a bit before, as I think it would actually be faster to go down the Wikipedia rabbit hole than have to search through tens of thousands of articles. Maybe I'll get to this someday.

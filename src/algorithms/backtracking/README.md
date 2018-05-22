BackTracking Do's
- Dont forget your if..else..
- Understand what the constraints are.
- Think of the base case- when am I done? (BASE CASE)
- Think of the recursive case- what do I do when I have a partial solution? Try and solve another partial solution, move on! (RECURSE)
- What do I do if my partial solution is incorrect? Back track to previous state of the program. (BACKTRACK)

Key Ideas (BackTracking):
- Main characteristics of backtracking algorithms: "The algorithm consists of working your way through a sequence of decision points in which each choice leads you further along some path. If you make the correct set of choices, you end up at the solution. On the other hand, if you reach a dead end or otherwise discover that you have made an incorrect choice somewhere along the way, you have to backtrack to a previous decision point and
try a different path." (from programming abstarctions textbook)
	1) There are several decision points that could lead to a solution or a dead end
	2) If a deadend is encountered, backtrack to previous decision point.
- Have if..else. if takes care of base case while else takes care of the recursive case.
- There are basically five types of recursive backtracking problems:
	- Determine whether a solution exists.
	- Find a solution.(Knights Tour)
	- Find the best solution.
	- Count the number of solutions.
	- Print/find all the solutions.(Permutations, Subsets, NQueen)
- General syntax for backtracking algorithms:
		If you are already at a solution, report success.
			for (every possible choice in the current position ) {
		 		Make that choice and take one step along the path.
		 	   	Use recursion to solve the problem from the new position.
		 	   	If the recursive call succeeds, report the success to the next higher level.
		 	   	Back out of the current choice to restore the state at the beginning of the loop.
			}
		Report failure.
- The brute force solution of some backtracking problems (e.g. sudoku solver) can be to generate all possible choices and see if each generated choice
leads to a solution.

Common BackTracking Problems:
- Knight's Tour
- Rat in a maze
- m-coloring problem
- Sudoku solver
- N Queen problem
- Subset sum
- Solving cryptarithmetic puzzles
- Hamiltoniana cycle
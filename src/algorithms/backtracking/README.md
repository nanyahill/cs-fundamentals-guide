Key Ideas (BackTracking):
- Main characteristics of backtracking algorithms: "The algorithm consists of working your way through a sequence of decision points in which each choice leads you further along some path. If you make the correct set of choices, you end up at the solution. On the other hand, if you reach a dead end or otherwise discover that you have made an incorrect choice somewhere along the way, you have to backtrack to a previous decision point and
try a different path." (from programming abstarctions textbook)
	1) There are several decision points that could lead to a solution or a dead end
	2) If a deadend is encountered, backtrack to previous decision point.
- Have if..else. if takes care of base case while else takes care of the recursive case.
- There are basically five types of recursive backtracking problems:
	- Determine whether a solution exists.
	- Find a solution.
	- Find the best solution.
	- Count the number of solutions.
	- Print/find all the solutions.
- General syntax for backtracking algorithms:
		If you are already at a solution, report success.
			for (every possible choice in the current position ) {
		 		Make that choice and take one step along the path.
		 	   	Use recursion to solve the problem from the new position.
		 	   	If the recursive call succeeds, report the success to the next higher level.
		 	   	Back out of the current choice to restore the state at the beginning of the loop.
			}
		Report failure.
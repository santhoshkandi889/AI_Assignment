**🐇 Problem 1: Rabbit Leap Puzzle**

📄 Description : 

In the rabbit leap problem, three east-bound rabbits stand in a line blocked by three west-bound rabbits. They are crossing a stream with stones placed in the east–west direction in a line. There is one empty stone between them.

Each rabbit can only:

Move forward to an adjacent empty stone, or

Jump over one rabbit to an empty stone (but not more than one).

Goal: Make all the east-bound and west-bound rabbits successfully swap sides without stepping into the water or getting into a deadlock.

🧠 Draw the state space, implement BFS and DFS to solve it, and output the sequence of valid moves.

💡 Solution Intuition

The puzzle is modeled as a linear array of positions.

Each position can be 'E' (east rabbit), 'W' (west rabbit), or '_' (empty).

Start state: ['E', 'E', 'E', '_', 'W', 'W', 'W']

Goal state: ['W', 'W', 'W', '_', 'E', 'E', 'E']

Use BFS to find the shortest sequence of valid moves.

Use DFS to explore all possible configurations recursively.


**🌉 Problem 2: Bridge and Umbrella Puzzle**

📄 Description :

Four people need to cross a bridge at night with only one umbrella, and the bridge can hold at most two people at once.

Each person takes different time to cross:

A → 1 min, B → 2 min, C → 5 min, D → 10 min

Rules:

The umbrella must be carried when crossing.

If two people cross, they move at the slower person’s speed.

Someone must return with the umbrella if more people are left to cross.

Goal: Move all people to the other side with the least total time.

💡 Solution Intuition

Each state tracks:

Who is on the left side

Who is on the right side

Where the umbrella is

Total time so far

Model as a state transition graph, where each move results in a new state.

Use BFS to find the minimum total time path.

Use DFS to explore all possibilities (if optimization isn't needed).

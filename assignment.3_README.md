Problem Statement
Given an undirected weighted graph and a starting node, determine the shortest path lengths from the starting node to all other nodes.

If a node is unreachable, output -1.

Multiple test cases are supported.

Constraints:

2
≤
𝑁
≤
3000

1
≤
𝑀
≤
𝑁
(
𝑁
−
1
)
2

Edge weights up to 
10
5

Approach
Implemented Dijkstra’s algorithm using:

Adjacency list for graph storage

PriorityQueue (min‑heap) for efficient shortest path expansion

Visited array to avoid reprocessing nodes

Edge deduplication to keep only the smallest weight between two nodes

Time complexity: 
𝑂
(
(
𝑉
+
𝐸
)
log
⁡
𝑉
)
, efficient for large graphs.

Code Highlights
Edge class → represents graph edges.

Node class → represents PQ entries with node id and current distance.

dijkstra() → core algorithm returning shortest distances.

main() → handles multiple test cases, builds graph, and prints results.

Sample Input
Code
1
4 3
1 2 5
2 3 6
1 3 15
1
Sample Output
Code
5 11 -1
Explanation:

Distance from 1 → 2 = 5

Distance from 1 → 3 = min(15, 5+6) = 11

Node 4 unreachable → -1

How to Run
Save the code in Solution.java.

Compile:

Code
javac Solution.java
Run:

Code
java Solution < input.txt
where input.txt contains the test cases.

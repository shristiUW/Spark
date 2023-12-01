# Spark
Documentation of the BFS-based shortest-path
search Program
In this programming assignment our goal is to get familiarized with Spark's data transformations and actions by implementing a parallelized shortest-path search based on Breadth-First Search (BFS).
In the program, we first implement the entire graph into a Spark JavaPairRDD structure, mapping each vertex to a Data object containing its attributes.
Our program then iterates through a loop, starting with the source vertex marked as active. Subsequently, within each loop iteration:
1. Neighbor Distances are Updated: For every active vertex, the distances of its neighbors from the source are updated.
2. Shorter Paths are Activated: Any vertex finding a shorter distance to the source is marked as active.
This process of updating neighbor distances and activating shorter paths is repeated until all vertices are marked "INACTIVE” indicating that we have found the shortest path from the source.
The key aspect of the program is to explore active points one by one, changing distances for their nearby points, and marking new points when a quicker route is found. This method helps the algorithm to move through the graph, finding the shortest way to reach each point from the starting point.
In summary, our Spark-based BFS implementation leverages iterative message passing and vertex activation to efficiently traverse a graph and uncover the shortest path from a given source. The algorithm utilizes Spark's distributed capabilities for processing large graphs in parallel.

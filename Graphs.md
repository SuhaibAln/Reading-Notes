# Graphs 
- are non-linear Data Structures which are great for representing relationships. Graphs can be directed or undirected according to the orientation of their edges; weighted or unweighted according to the weight assigned to each edge (or lack thereof); and cyclic or acyclic depending on whether the edges create a closed loop.
# MEMORY
Graphs usually contain nodes and edges representing which nodes are connected. Graphs can be represented in several ways, e.g. through:
an edge list: a double array grouping nodes with a connecting edge [[O 1], [1 2], [2 0]]
an adjacent list: a double array that stores the nodes a certain node connects to in the array index positions corresponding to the node value [[1 2],[0 2],[0 111
• an adiacent matrix: a binary matrix of size n x n where 1 represents an edge between the respective coordinates
[EO 1 1], [1 0 1], [1 1 0]1
* INSERTION, DELETION and SEARCH
Operations such as building a graph, inserting, retrieving or removing vertices/edges as well as search depend strongly on the Graph implementation method. Trade-offs between space and time should be made considering how and how much we expect our graph to grow. Adjacent list implementations are more efficient if memory matters, and adjacent matrix implementations are good to check the existence of an edge between 2 vertices in 0(1) time.
Graph traversal can be done using Depth First Search or
Breadth First Search and usually run in O(E + V) time, where E stands for the number of edges and V the number of vertices.
Graphs can grow into complex data structures and have limited use cases, mostly targeted at representing connections. Good real life examples of graphs are Facebook's Graph API representing user connections and likes, and Google's Knowledge Graph built on search queries

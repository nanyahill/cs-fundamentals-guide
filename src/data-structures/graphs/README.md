Graphs
- A directed acyclic graph (DAG) is a directed graph in which there are no cycles.
- In a DAG, vertices with no incoming edges are referred to as sources and vertices with no outgoing edges are referred to as sink.
- In an undirected graph, vertices u and v are connected, if the graph contains a path fom u to v.
- A graph is connected if every pair of vertices in the graph is connected.
- A connected component is a maximal set of vertices C such that each pair of vertices in C is connected in G.


- A tree is an undirected graph that is connected and has no cycles.

Topological Sorting:
1) Most important operation on a DAG.
2) It orders the vertices on a line such that all directed edges go from left to right.
3) Such an ordering does not exist if the graph contains a directed cycle, at which you stop going right and go backwards to the left breaking the topological sorting rule- always move from left to right.
4) Each DAG has at least one topological sort.
5) Importance of topological sort is that it gives us an ordering to process each vertex before any of its successors.
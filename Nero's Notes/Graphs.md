# Graphs


Informally, a graph is a set of vertices and connected by edges. Formally, a directed graph is a set V of vertices and a set E in V x V of edges. Given an edge *e = (u,v)*, the vertex *u* is its *source*, and *v* is its *sink*. Graphs are often decorated, e.g, by adding lengths to edges, weights to vertices, a start vertex, etc. 

A *path* in a directed graph from vertex *u* to vertex *v* is a sequence of vertices *(v0, v1, .... vn-1)* where *v0* = *u*, *vn-1* = *v*, and each *(vi, vi+1)* is an edge. The sequence may consist of a single vertex. The *length* of the path *(v0, v1,..., vn-1)* is n-1. Intuitively, the length of a path is the number of edges it traverses. If there exists a path from *u* to  *v*, *v* is said to be *reachable* from *u*. 


A *directed acyclic graph* (DAG) is a directed graph in where there are no *cycles*, i.e, paths which contain one or more edges and which begin and end at the same vertex.  Vertices in a DAG which have no incoming edges are referred to as *sources*; vertices which have no outgoing edges are referred to as *sinks*. A *topological ordering* of the vertices in a DAG is an ordering of the vertices in which each edge is from a vertex earlier in the ordering to a vertex later in the ordering. 

An undirected graph is also a tuple (V, E); however, E is a set of unordered pairs of vertices. Graphically, this is captured by drawing arrowless connections between vertices.


If G is an undirected graph, vertices *u* and *v* are said to be *connected* if G contains a path from *u* to *v*. Otherwise, *u* and *v* are said to be disconnected.  A graph is said to be connected if every paid of vertices in the graph is connected. A *connected component* is a maximal set of vertices C such that each pair of vertices in C is connected in G. Every vertex belongs to exactly one connected component. 

A directed graph is called *weakly connected* if replacing all of its directed edges with undirected edges produces an undirected graph that is connected. It is *connected* if it contains a directed path from *u* to *v* or a directed path from *v* to *u* for every pair of vertices *u* and *v*. It is *strongly connected* if it contains a directed path from *u* to *v* and a directed path from *v* to *u* for every pair of vertices *u* and *v*.

Graphs naturally arise when modeling geometric problems, such as determining connected cities. However, they are more general, and can be used to model many kinds of relationships.

A graph can be implemented in two ways - using adjacency lists or an adjacency matrix. In the adjacency list representation, each vertex *v*, has a list of vertices to which it has an edge. The adjacency matrix representation uses a V * V Boolean -valued matrix indexed by vertices, with a 1 indicating the presence of an edge. The time and space complexities of a graph algorithm are usually  expressed as a function of the number of vertices and edges.

A *tree* (sometimes called a free tree) is a special sort of graph - it is an undirected graph that is connected but has no cycles. (Many equivalent definitions exist, e.g. a graph is a free tree if and only if there exists a unique path between every pair of vertices.) There are a number of variants on the basic idea of a tree. A rooted tree is one where a designated vertex is called the root, which leads to a parent-child relationship on the nodes. An ordered tree is a rooted tree in which each vertex has an ordering on its children. Binary trees differ from ordered trees since a node may have only one child in a binary tree, but that node may be a left or a right child, whereas in an ordered tree no analogous notion exists for a node with a single child. Specifically, in a binary tree, there is position as well as order associated with the children of nodes.


## Graphs boot camp 

Graphs are ideal for modeling and analyzing relationships between pairs of objects. For example, suppose you were given a list of the outcomes of matches between pairs of teams, with each outcome being a win or a loss. A natural question is as follows: given teams A and B, is there a sequence of teams starting with A and ending with B such that each team in the sequence has beaten the next team in the sequence?

A slick way of solving this problem is to model the problem using a graph. Teams are vertices, and an edge from one team to another indicates that the team corresponding to the source vertex has beaten the team corresponding to the destination vertex. Now we can apply graph reachability to perform the check. Both DFS and BFS are reasonable approaches - the program below uses DFS.


```java
public static class MatchResult{
	public String winningTeam;
	public String losingTeam;
	
	public MatchResult(String winningTeam, String losingTeam){
		this.winningTeam = winningTeam;
		this.losingTeam = losingTeam;
	}	
}

public static boolean canTeamABeatTeamB(List<MatchResult> matches, String teamA, String teamB){
		return isReachableDfs(buildGraph(matches),  teamA, teamB, new HashSet<>());
}

private static Map<String, Set<String>> buildGraph(List<MatchResult> matches){
 	Map<String, Set<String>> graph = new Hashmap<>();
	for(MatchResult match: matches){
		graph.putIfAbsent(match.winningTeam, new HashSet<>()).add(match.losingTeam);
	}
	return graph;
}

private static boolean isReachableDfs(Map<String, Set<String>> graph, String curr, String dest, Set<String> visited){
	if(curr == dest){
		return true;
	}
	else if (visited.contains(curr) || graph.get(curr) == null){
		return false;
	}
	visited.add(curr);
	return graph.get(curr).stream().anyMatch(team -> isReachableDfs(graph, team, des, visited));
}



```

The time complexity and space complexity are both O(E), where E is the number of outcomes.

### Top tips for graphs

- It is natural to use a graph when the problem involves spatially connected objects, e.g road segments between cities.
- More generally, consider using a graph when you need to analyze any binary relationship, between objects, such as interlinked web pages, followers in a social graph, etc. In such cases, quite often the problem can be reduced to a well known graph problem.
- Some graph problems entail analyzing structure, e.g looking for cycles or connected components. DFS works particularly well for these applications.
- Some graph problems are related to optimization, e.g, find the shortest path from one vertex to another. BFS, Dijkstra's shortest path algorithm, and minimum spanning tree are examples of graph algorithms appropriate for optimization problems.

## Graph Search

Computing vertices which are reachable from other vertices is a fundamental operation which can be performed in one of two idiomatic ways, namely depth-first search(DFS) and breadth-first search (BFS). Both have linear time complexity - O( E + V) to be precise. In the worst-case there is a path from the initial vertex covering all vertices without any repeats, and the DFS edges selected correspond to this path, so the space complexity of DFS is O(V) (this space is implicitly allocated on the function call stack). The space complexity of BFS is also O(V), since in a worst case there is an edge from the initial vertex to all remaining vertices, implying that they will all be in the BFS queue simultaneously at some point.

DFS and BFS differ from each other in terms of the additional information they provide, e.g, BSF can be used to compute distances from the start vertex and DFS can be used to check for the presence of cycles. Key notions in DFS include the *discovery time* and *finishing time* for vertices.


## Advanced Graph Algorithms

Up to this point we looked at basic search and combinatorial properties of graphs. The algorithms we considered were all linear time complexity and relatively straightforward - the major challenge was in modeling the problem appropriately.

There are four classes of complex graph problems that can be solved efficiently, i.e in polynomial time. Most other problems on graphs are either variants of these or , very likely, not solvable by polynomial time algorithms. These four classes are:

- *Shortest Path*  - Given a graph, directed or undirected, with costs on the edges, find the minimum cost path from a given vertex to all vertices. Variants include computing the shortest paths for all pairs of vertices, and the case where costs are all non-negative
- *Minimum Spanning Tree* - given an undirected graph G = (V, E), assumed to be connected, with weights on each edge, find a subset E' of the edges with minimum total weight such that the subgraph G' = (V, E') is connected
- *Matching* - given an undirected graph, find a maximum collection of edges subject to the constraint that every vertex is incident to at most one edge. The matching problem for bipartite graphs is especially common and the algorithm for this problem is much simpler than for the general case. A common variant is the maximum weighted matching problem in which edges have weights and a maximum weight edge set is sought, subject to the matching constraint.
- *Maximum Flow* - given a directed graph with a capacity for each edge, find the maximum flow from a given source to a given sink, where a flow is a function mapping edges to numbers satisfying conservation (flow into a vertex equals the flow out of it) and the edges capacities. The minimum cost circulation problem generalizes the maximum  flow problem by adding lower bounds on edge capacities, and for each edge, a cost per unit flow.

These four problems classes have polynomial time algorithms and can be solved efficiently in practice for very large graphs. Algorithms for these problems tend to be specialized, and the natural approach does not always work best. For example, it is natural to apply divide and conquer to compute the MST as follows. Partition the vertex set into two subsets, compute MSTs for the subsets independently, and then join these two MSTs with an edge of minimum weight between them.
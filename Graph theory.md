---
tags:
  - MATH240
---
# Graph theory

A graph is:: a pair $G = (V,E)$ where $V$ is a finite nonempty set of vertices. $E$ is a set of edges in the form $\{X,Y\}$ with $X,Y \in V$.


A simple graph is:: a graph with no self-loops (i.e. edges in the form $\{X\}$).

The degree of a vertex $X \in V$ is:: the number $\deg(X)$ of edges $e \in E$ which contain $X$ (self-loops count twice).

$\sum\limits_{x \in V}\deg(X)=$::$2 |E|$ (Handshaking lemma)

Given two graphs: $G=(V,E)$, $H=(W,F)$, $G$ is a subgraph of $H$ (denoted $G \subseteq H$) if:: $V \subseteq W$ and $E \subseteq F$.

A walk of length $n$ on a graph $G=(V,E)$ is:: a finite sequence of vertices $w=(v_{0},\dots ,v_{n})$ such that $\forall i$, $v_{i}v_{i+1} \in E$. Its endpoints are $v_{0}$ and $v_{n}$. 

## Paths and trees

- A walk is called a path if:: $i \neq j \implies v_{i}\neq v_{j}$ (injective walk) on vertices.
- A walk is called a cycle if:: $v_{0}=v_{n}$ and $w^{'}=(v_{0},\dots ,v_{n-1})$ is a path.

There exists a path with endpoints $X$, $Y$ $\iff$ there exists:: a walk with endpoints $X$, $Y$.

A graph $G$ is connected if:: $\forall X,Y \in V$, there exists a path (or walk) with endpoints $X,Y$.

A connected component of $G$ is:: a maximum connect subgraph.

A forest is:: a simple graph without cycles.

A tree is:: a connected forest (no isolation).

A graph $G=(V,E)$ is a tree $\iff$ $\forall X,Y \in V$, there exists:: a unique path with endpoints $X,Y$.

If $T$ is a tree, the distance between two vertices $X,Y$ is:: the length $\text{dist}(X,Y)$ of the unique path between them.

A leaf in a tree $T$ is:: a vertex of degree 1.

A tree with $n \geq 2$ has at least:: one leaf.

If $T$ is a tree with $n$ vertices, then it has:: $(n-1)$ edges. Converse is also true, $G$ has $(n-1)$ edges $\implies$ $G$ is a tree.

Given a graph $G$, a spanning tree of $G$ is:: a subgraph $T \subseteq G$ that is a tree which contains all vertices of $G$.

$G$ is connected $\iff$$G$ has:: a spanning tree.

If $G$ is connected, has $n$ vertices, $(n-1)$ edges, then $G$ is:: a tree.

## Bipartite graphs

A graph $G=(L \cup R, E)$ is bipartite if:
?
1. $L \cap R=\emptyset$
2. There is no edge $XY \in E$ such that $\{X,Y\} \subseteq L$ or $\{X,Y\} \subseteq R$.
Bipartite graphs occur when we try to match objects of two different types.

A $k$-coloring of a graph $G$ is:: a coloring of vertices using $k$ different colors, such that two neighbors never have the same color. $G$ is $k$-colorable if it has a $k$-coloring.

$G$ is bipartite $\iff$ $G$ is:: 2-colorable.

A graph is bipartite (2-colorable) $\iff$ It does not contain:: an odd cycle.

## Planar graphs

Planar graphs are:: graphs that can be drawn on a plane without intersecting edges.

The faces of a planar graph are:: the regions of the plane delimited by edges of the graph.![[Pasted image 20250426225431.png]]


Let $G$ be connected planar graph with $n$ vertices, $e$ and $f$ faces, then $e+2=$::$n+f$. (The number of faces is then independent of how we draw the graph).

1. If $G$ is a connected planar graph with $n \geq 4$ vertices, then $e \leq$::$3n - 6$
2. If $G$ is a connected, planar, **bipartite** graph with $n \geq 6$, then $e\leq$::$2n - 4$.


A graph $H$ is a minor of $G$ denoted $H \leq G$ if you can obtain from $G$ by applying a finite sequence of the follow operations:
?
1. Edge deletion.
2. Vertex deletion (and all edges attached).
3. Edge contraction (remove an edge and merge the two ends together).


If $K_{5}\leq  G$ or $K_{3,3}\leq  G$, then $G$ is:: not planar.

$G$ is not planar $\iff$:: $K_{5} \leq G$ or $K_{3,3}\leq G$.
---
tags:
  - COMP250
---
# Rooted trees

Example of linear and non-linear data structures:
?
- Linear: array, linked list
- Non-linear: tree, graph
<!--SR:!2024-12-07,10,230-->

A tree is a collection of:: nodes (vertexes)
<!--SR:!2024-12-17,24,250-->
The root is:: the top node in a tree
<!--SR:!2024-12-16,23,250-->

A directed edge is:: ordered pair of nodes $(v_{i},~v_{j})$ (from, to).
<!--SR:!2024-11-30,9,210-->
Trees can be undirected or directed. If directed, the edges are:: either all pointing away from the root or all pointing towards the root.
<!--SR:!2024-12-15,17,210-->

- If a (rooted) tree has $n$ nodes, then how many edges does it have?:: $n-1$
<!--SR:!2024-12-08,17,250-->

An internal node is:: a node with at least one child.
<!--SR:!2024-12-13,20,250-->
An leaf (or external node) is:: a node with no children.
<!--SR:!2024-12-17,24,250-->

A path in a tree is:: a sequence of nodes $(v_{1},~v_{2},~\dots ,~v_{k})$ such that $(v_{i},~v_{i+1})$ is an edge.
<!--SR:!2024-12-18,25,250-->
The length of a path is:: the number of edges in the path (number of node in the path - 1)
<!--SR:!2024-12-22,28,250-->
The height of a node is:: the maximum length of a path from that node to a leaf.
<!--SR:!2024-12-20,26,250-->


Preorder vs Postorder traversal (pseudocode)
?
![[image-20241112153652738.png]]
<!--SR:!2024-12-21,27,250-->


Tree traversal using stack (non-recursive) pseudocode
?
![[image-20241112155657702.png]]
<!--SR:!2024-12-05,15,250-->

Traversing a tree using a stack will have a:: reversed preorder.
<!--SR:!2024-12-12,19,250-->

Tree traversal using queue (non-recursive) pseudocode
?
![[image-20241112155853108.png]]
<!--SR:!2024-12-05,15,250-->

Traversing a tree using a queue will have a:: breadth first traversal.
<!--SR:!2024-12-07,16,250-->
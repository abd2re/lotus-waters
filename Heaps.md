---
tags:
  - COMP250
---
# Heaps

## Heap (Binary tree implementation)

A complete binary tree is:
?
Binary tree of height $ℎ$ such that every level less than $ℎ$ is full, and all nodes at level $ℎ$ are as far to the left as possible.
![[image-20241126222136172.png]]
<!--SR:!2024-11-30,3,250-->


A min heap is:: a complete binary tree with unique comparable elements, such that each node’s element (key) is less than its children’s element (key).
<!--SR:!2024-11-30,3,250-->

How will this tree look after we add $c$
![[image-20241126222534678.png]]
?
![[image-20241126222558123.png]]
<!--SR:!2024-11-30,2,230-->



`add()` implementation in heap (upheap):
?
![[image-20241126222737479.png]]
<!--SR:!2024-11-30,3,250-->


How will the heap look like after removing $a$ (`removeMin()`)
![[image-20241126222954238.png]]
?
![[image-20241126223007939.png]]
<!--SR:!2024-11-30,3,250-->



`removeMin()` implementation for heaps (downheap):
?
![[image-20241126223218440.png]]
<!--SR:!2024-11-30,3,250-->



## Heap (Array implementation)

Heap index starts with:: index `1`
<!--SR:!2024-12-01,4,270-->

parent index =:: child index / 2
<!--SR:!2024-11-30,2,230-->
left child index =:: 2 * parent index
<!--SR:!2024-11-29,2,247-->
right child index =:: 2 * parent index + 1
<!--SR:!2024-11-29,2,247-->

An array data structure can be used for any binary tree. But this is uncommon and often inefficient for:: binary trees who are not complete.
<!--SR:!2024-11-30,3,250-->

`add()` implementation:
?
![[image-20241126224149061.png]]
<!--SR:!2024-11-30,3,250-->

`removeMin()` implementation:
?
![[image-20241126224434385.png]]
![[image-20241126224726957.png]]
<!--SR:!2024-11-30,3,250-->



## Build a heap

Suppose there are $𝑛$ elements to add (upHeaping), then in the worst case the number of swaps needed to add all the elements is::$t(n)=\sum\limits_{i=1}^{n}\text{floor}(\log_{2}i)$
<!--SR:!2024-11-28,1,230-->

$t(n)$ (time complexity of building a heap) (upHeaping) is bounded by:: $\frac{1}{2}n\log_{2}n \leq t(n) \leq n\log_{2}n$
<!--SR:!2024-11-29,2,247-->


Fast way to build heap (downHeaping) from list
?
![[image-20241126230757045.png]]
<!--SR:!2024-11-28,1,230-->


upHeaping vs downHeaping time complexity
?
![[image-20241126230811999.png]]
<!--SR:!2024-11-30,3,250-->


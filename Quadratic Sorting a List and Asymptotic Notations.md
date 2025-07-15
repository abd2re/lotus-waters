---
tags:
  - COMP250
---
# Quadratic Sorting a List and Asymptotic Notations

Bubble sort procedure:: repeatedly iterate through the list and swap adjacent elements if they are in the wrong order.
<!--SR:!2024-12-13,42,250-->

Bubble sort algorithm pseudocode
?
```swift
sorted = false
i = 0
while (!sorted) {
	sorted = true
	for j from 0 to list.length - i - 2 {
		if(list[j] > list[j+1]) {
			swap(list[j], list[j+1])
			sorted = false
		}
	}
	i++
}
```
<!--SR:!2024-10-08,3,250-->

Selection sort procedure:: select the smallest element in the unsorted part of the list; swap that element with the element in the initial position of the unsorted array; change where you divide the array from the sorted part to the unsorted part.
<!--SR:!2024-11-30,33,250-->

Selection sort algorithm pseudocode
?
```swift
for delim from 0 to N-2 {
	min = delim
	for i from delim+1 to N-1 {
		if(list[i] < list[min]) {
			min = i
		}
	}
	if(min != delim) {
		swap(list[min], list[delim])
	}
}
```
<!--SR:!2024-10-08,2,230-->

Insertion sort procedure:: select the first element of the unsorted part of the list; insert such element into its correct position in the sorted part of the list; change where you divide the array from the sorted part to the unsorted part.
<!--SR:!2024-12-21,47,250-->

Insertion sort algorithm pseudocode
?
```swift
for i from 0 to N-1 {
	element = list[i]
	k = i
	while(k>0 && element<list[k-1]){
		list[k] = list[k-1]
		k--
	}
	list[k] = element
}
```
<!--SR:!2024-10-08,2,230-->
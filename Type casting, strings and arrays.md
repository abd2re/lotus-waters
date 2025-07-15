---
tags:
  - COMP250
---
# Type casting, strings and arrays
What happens in the following example?
```java
System.out.println( 2 + 3 + "5"); 
System.out.println("5" + 2 + 3);
```
?
```
55 
523
```
<!--SR:!2024-12-08,47,250-->

```java
char first = 'a'; 
char second = (char) (first + 1);
```
What is the value of second?
?
`b`
<!--SR:!2024-12-05,44,250-->

```java
char letter = 'g';
if (letter == 'a') {
    System.out.println("first letter of the alphabet");
} else if (letter == 'z') {
    System.out.println("Last letter of the alphabet");
} else if (letter > 'a' && letter < 'z') {
    System.out.println("Another letter of the alphabet");
} else {
    System.out.println("Not a lower case letter of the alphabet");
}
```
prints?
?
`Another letter of the alphabet`
<!--SR:!2024-12-18,54,250-->

```java
int x = 3;
double y = 4.56;
int n = (int) y + 5;
double m = (double) x;
```
What are the values of `x`, `y`, `n`, and `m`?
?
`x = 3, y = 4.56, n = 9, m = 3.0`
<!--SR:!2025-01-18,75,270-->

```java
int[] x = {1,2,3};
int[] y = {1,2,3};
System.out.println(x==y);
```
What will the program will print?
?
`false`
<!--SR:!2025-02-08,91,270-->

```java
int[] x = {1,2,3};
int[] y = {1,2,3};
System.out.println(x.equals(y));
```
What will the program will print?
?
`false`
<!--SR:!2024-12-13,49,250-->

```java
int[] x = {1,2,3};
int[] y = {1,2,3};
System.out.println(Arrays.equals(x,y));
```
What will the program will print?
?
`true`
<!--SR:!2024-12-14,33,230-->
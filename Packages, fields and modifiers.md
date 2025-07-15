---
tags:
  - COMP250
---
# Packages, fields and modifiers

```java
public static void main(String[] args) {
    int x = 5;
    int y = x;
    x++;
    System.out.println(x + " " + y);
}
```
What prints?
?
`6 5`
<!--SR:!2025-01-09,67,250-->

```java
public static void main(String[] args) {
    int[] x = {1, 2, 3};
    int[] y = x;
    y[0] = 4;
    System.out.println(x[0] + " " + y[0]);
}
```
What prints?
?
`4 4`
<!--SR:!2024-12-17,19,230-->

```java
public static void main(String[] args) {
    int x = 5;
    example(x);
    System.out.println(x);
}

public static void example(int x) {
    x = x * 5;
}
```
What prints?
?
`5`
<!--SR:!2024-12-02,42,250-->

```java
public static void main(String[] args) {
    int[] x = {1, 2, 3};
    example(x);
    System.out.println(x[0]);
}

public static void example(int[] x) {
    x[0] = 4;
}
```
What prints?
?
`4`
<!--SR:!2024-12-29,59,250-->

```java
public static void main(String[] args) {
    int[] x = {1, 2, 3, 4};
    myMethod(x);
    System.out.println(Arrays.toString(x));
}

public static void myMethod(int[] a) {
    for (int i = 0; i < a.length; i++) {
        a[i] = i;
    }
}
```
What prints?
?
`[0, 1, 2, 3]`
<!--SR:!2025-03-02,97,250-->

```java
public static void main(String[] args) {
    String s = "word";
    myMethod(s);
    System.out.println(s);
}

public static void myMethod(String t) {
    t = t + "s";
}
```
What prints?
?
`word`
<!--SR:!2024-12-11,16,210-->

```java
public static void main(String[] args) {
    char[] letters = {'w', 'o', 'r', 'd'};
    for (int i = 0; i < letters.length; i++) {
        if (letters[i] == 'o') {
            letters[i] = 'a';
        }
    }
    System.out.println(Arrays.toString(letters));
}
```
What prints?
?
`[w, a, r, d]`
<!--SR:!2024-12-31,63,250-->

```java
public static void main(String[] args) {
    String s = "word";
    for (int i = 0; i < s.length(); i++) {
        if (s.charAt(i) == 'o') {
            s.charAt(i) = 'a';
        }
    }
    System.out.println(s);
}
```
What prints?
?
```
compile time error: unexpected type. 
Required: variable. Found: value.
```
<!--SR:!2024-12-02,15,230-->


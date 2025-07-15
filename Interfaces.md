---
tags:
  - COMP250
---
# Interfaces


Similarly to classes, interfaces can have fields and methods but the following restrictions apply (2):
?
- All methods are by default public and abstract.
- All fields are by default public, static, and final.
<!--SR:!2024-12-03,13,150-->

Interfaces can be instantiated, true or false ?:: false.
<!--SR:!2025-01-04,42,250-->

We declare an interface using
?
the `interface` keyword.
```java
public interface myInterface { 
	: 
}
```
<!--SR:!2025-01-17,51,250-->

- To use an interface you first need a class that implements it. Interfaces specify what a class must:: do and not how. It is the blueprint of the class.
<!--SR:!2024-12-20,34,250-->
- A class can implement one or more interfaces using:: the keyword `implements`.
<!--SR:!2024-12-07,29,270-->
- If a class implements an interface and does not implement all methods specified by the interface then:: that class must be declared abstract.
<!--SR:!2025-01-18,52,250-->
- It is possible for a Java interface to extend another Java interface, just like classes extend other classes. You specify inheritance using:: the `extends` keyword.
<!--SR:!2024-11-30,23,250-->

From Java 8/9 onwards, interfaces can also contain the following methods (4):: Default methods, Static methods, Private methods, Private Static methods
<!--SR:!2024-11-29,16,210-->

A generic type is:: a class or interface that is parameterized over types. We use angle brackets (`<>`) to specify the type parameter. Ex: ```public class Cage<T>```
<!--SR:!2025-01-02,43,250-->

Sometimes we might want to restrict the types that can be used to create an object, we can do that using:: the keyword `extends`. In this context, extends is used to mean either "extends" (as in classes) or "implements" (as in interfaces). Ex: ```public class Cage<T extends Animal>```. Only objects that implement or extends `Animal` superclass/interface will work. We can also use `Animal` methods inside of our class with our generic type.
<!--SR:!2024-11-29,10,210-->

Interfaces define new data types, so for example can have:
?
```java
List<String> greetings; 
greetings = new ArrayList<String>(); 
greetings.add("Hello"); 
: 
greetings = new LinkedList<String>(); 
greetings.add("Good day!");
```
Whenever an object of type List is required, any instance of any of the classes that implement List can be used. So, in this case, `myMethod()` can be called both with an `ArrayList` or a `LinkedList` as a parameter.
```java
public void myMethod(List<String> list) { 
	: 
	list.add("one more"); 
	: 
	list.remove(3); 
	: 
}
```
<!--SR:!2025-01-15,51,250-->

Can a class (abstract or not) extend more than one class (abstract or not) ?:: No.
<!--SR:!2024-12-03,26,250-->
Can a class (abstract or not) implement multiple interfaces ?:: Yes.
<!--SR:!2024-12-28,39,250-->
Can an interface extend more than one interface ?:: Yes.
<!--SR:!2025-01-02,42,250-->

## `Comparable` interface

`Comparable` is part of `java.lang` package and contains only one method named:: `compareTo(T o)`.
<!--SR:!2024-12-08,30,270-->

Code snippet of `Comparable` interface:
?
```java
public interface Comparable<T>{ 
	int compareTo(T o); 
}
```
<!--SR:!2025-01-06,44,250-->

Code snippet of class that implements `Comparable`:
?
```java
public class T implements Comparable<T>{ 
	public int compareTo(T o) {...} 
}
```
<!--SR:!2024-12-26,36,230-->

## `Iterable` and `Iterator` interfaces

- Objects of type `Iterable` are:: representations of a series of elements that can be iterated over. (e.g. a specific `ArrayList`)
<!--SR:!2024-12-08,10,230-->
- Objects of type `Iterator` allows you to:: iterate through objects that represent a collection (a series of elements).
<!--SR:!2024-11-29,22,250-->
- A class that implements `Iterable` needs to implement:: the `iterator()` method.
<!--SR:!2024-12-01,24,250-->
- The `iterator()` method returns an object of type:: `Iterator` that can then be used to iterate through the elements of this instance.
<!--SR:!2024-12-02,25,250-->
- A class that implements `Iterator` needs to implement:: the methods `hasNext()` and `next()`.
<!--SR:!2024-12-06,28,270-->

Code snippet of `Iterable` and `Iterator` interface:
?
```java
public interface Iterable<T> { 
	public Iterator<T> iterator(); 
}

public interface Iterator<T> { 
	boolean hasNext(); 
	T next();// returns current, 
			 // and advances to next 
	void remove(); // optional, ignore it 
}
```
<!--SR:!2024-11-29,23,250-->

Code snippets for two classes that implement `Iterable` and `Iterator`:
?
```java
public class MyCollection<T> implements Iterable<T> {
    public MyIterator<T> iterator() {
        return new MyIterator<T>(this);
    }
}

public class MyIterator<E> implements Iterator<E> {
    public MyIterator(MyCollection<E> c) {
        :
    }
}
```
<!--SR:!2024-12-18,25,210-->
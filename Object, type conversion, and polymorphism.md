---
tags:
  - COMP250
---
# Object, type conversion, and polymorphism

```java
System.out.println( new Object() );
```
What does this print?
?
`java.lang.Object@7852e922` where `7852e922` is a random hash address.
<!--SR:!2024-12-09,42,228-->

![[image-20240921185118383.png|200]]
```java
public class Test {
    public static void main(String[] args) {
        Dog snoopy = new Beagle();
        snoopy.bark();
    }
}
```
What prints?
?
`aowwwwuuu!` (polymorphism)
<!--SR:!2024-12-26,56,248-->

```java
Dog myDog = new Beagle();
```
Is this allowed?
?
Yes, it is an example of **upcasting** which happens automatically.
<!--SR:!2024-12-10,49,250-->

```java
Dog myDog = new Beagle(); 
Poodle myPoodle = myDog;
```
Is this allowed?
?
Compile-time error. The variable `myDog` is of type `Dog`, and it might not be pointing to a `Poodle`. It requires explicit **downcasting** to compile.
<!--SR:!2024-11-30,40,248-->

```java
Dog myDog = new Beagle(); 
Poodle myPoodle = (Poodle) myDog;
```
Is this allowed?
?
The code compiles, but there will be a run-time error because `myDog` is not pointing to a `Poodle` after all.
<!--SR:!2024-12-18,53,250-->

```java
Dog myDog = new Beagle(); 
myDog.hunt();
```
Is this allowed?
?
Compile-time error. The variable `myDog` is of type `Dog`, and there is no method called hunt inside the Dog `class`.
<!--SR:!2025-02-26,92,246-->

```java
Dog myDog = new Beagle(); 
((Beagle) myDog).hunt();
```
Is this allowed?
?
Yes, this code will compile and run.
<!--SR:!2025-03-03,97,250-->

![[image-20240921185118383.png|200]]
```java
public class Test {
    public static void main(String[] args) {
        Dog snoopy = new Beagle();
        snoopy.bark();
    }
}
```
Which `bark()` will it execute?
?
`aowwwwuuu`
<!--SR:!2025-02-13,96,270-->

![[image-20240921192906314.png|300]]
Which of the following snippets of code raise an error?
A. `Nut n = new Walnut(); n.taste();`
B. `Walnut w = new Walnut(); w.peel();`
C. `Peanut p = new Nut(); p.taste();`
D. `Nut n = new Walnut(); ((Peanut) n).makeButter();`
E. `Peanut p = new Peanut(); Walnut w = new Walnut(); Nut[] nuts = {p, w};`
?
B, C, and D will raise errors.
<!--SR:!2025-02-05,83,246-->

![[image-20240921193315163.png|300]]
```java
Nut n1 = new Peanut();
Walnut w = new Walnut();
Peanut p = new Peanut();
Nut n2 = new Nut();
Nut n3 = (Nut) w;
Nut[] nuts = {n1, w, p, n2, n3};
for (Nut n : nuts){
	n.taste();
}
```
What prints?
?
```
more!! 
walnut 
more!! 
just a nut 
walnut
```
<!--SR:!2024-12-05,39,210-->


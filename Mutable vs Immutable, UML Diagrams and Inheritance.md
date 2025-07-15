---
tags:
  - COMP250
---
# Mutable vs Immutable, UML Diagrams and Inheritance

```java
public class Dog {
    private String name;
    private Person owner;

    public Dog(String aName) {
        this.name = aName;
    }
    public static void main(String[] args) {
        Dog myDog = new Dog("Snoopy");
        System.out.println(myDog);
    }
}
```
What prints?
?
`Dog@4aeda9d5` where `4aeda9d5` is a random hash address.
<!--SR:!2025-02-11,91,270-->

```java
public class Dog {
    private String name;
    private Person owner;
    public Dog(String aName) {
        this.name = aName;
    }
    public static void main(String[] args) {
        Dog myDog = new Dog("Snoopy");
        String s = myDog.toString();
        System.out.println(s);
    }
}
```
What prints?
?
`Dog@4aeda9d5` where `4aeda9d5` is a random hash address.
<!--SR:!2024-11-29,34,230-->

```java
public class Dog {
    private String name;
    private Person owner;
    public Dog(String aName) {
        this.name = aName;
    }
    public static void main(String[] args) {
        Dog myDog = new Dog("Snoopy");
        Dog aDog = myDog;
        System.out.println(myDog.equals(aDog));
    }
}
```
What prints?
?
`true`
<!--SR:!2024-12-29,54,230-->

```java
public class Dog {
    private String name;
    private Person owner;
    public Dog(String aName) {
        this.name = aName;
    }
    public static void main(String[] args) {
        Dog myDog = new Dog("Snoopy");
        Dog aDog = new Dog("Snoopy");
        System.out.println(myDog.equals(aDog));
    }
}
```
What prints?
?
`false`
<!--SR:!2024-12-06,39,230-->

![[image-20240921184611347.png|200]]
``` java
public class Test {
    public static void main(String[] args) {
        Beagle snoopy = new Beagle();
        snoopy.bark();
    }
}
```
What prints?
?
`woof!`
<!--SR:!2025-01-27,70,230-->

![[image-20240921184611347.png|200]]
```java
public class Test {
    public static void main(String[] args) {
        Beagle snoopy = new Beagle();
        snoopy.bark(3);
    }
}
```
What prints?
?
`arf arf arf` (method overloading)
<!--SR:!2024-12-09,47,250-->

![[image-20240921185118383.png|200]]
```java
public class Test {
    public static void main(String[] args) {
        Beagle snoopy = new Beagle();
        snoopy.bark();
    }
}
```
What prints?
?
`aowwwuuu` (method overriding)
<!--SR:!2025-01-03,64,250-->

![[image-20240921190117524.png|200]]
```java
public class Test {
    public static void main(String[] args) {
        Beagle snoopy = new Beagle();
        snoopy.talk();
    }
}
```
What prints?
?
`woof!`
<!--SR:!2024-12-15,50,250-->

![[image-20240921191200696.png|200]]
```java
public class Test {
    public static void main(String[] args) {
        Dog myDog = new Dog("Giulia", 6.1.2016);
    }
}
```
Is this allowed? If so, what is created?
?
Yes
<!--SR:!2024-12-11,49,250-->

UML diagram (with abstract)
?
![[image-20240930203540662.png|center]]
![[image-20241009130547297.png|center]]
<!--SR:!2024-12-08,13,206-->


<!--SR:!2024-10-21,13,229-->














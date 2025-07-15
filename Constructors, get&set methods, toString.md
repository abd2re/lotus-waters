---
tags:
  - COMP250
---
# Constructors, get&set methods, toString

animals/Dog.java
```java
package animals; 
public class Dog { 
	⋮ 
}
```
buildings/Farm.java
```java
package buildings; 
import animals.Dog; 
public class Farm { 
	Dog d; 
	⋮ 
}
```
Does the compiler allow this?
?
Yes
<!--SR:!2024-12-22,57,250-->

animals/Dog.java
```java
package animals; 
class Dog { 
	⋮ 
}
```
buildings/Farm.java
```java
package buildings; 
import animals.Dog; 
public class Farm { 
	Dog d; 
	⋮ 
}
```
Does the compiler allow this?
?
No, the class `Dog` is visible only within its package.
<!--SR:!2024-12-26,35,170-->

animals/Dog.java
```java
package animals; 
public class Dog { 
	public String name;
	⋮ 
}
```
buildings/Farm.java
```java
package buildings; 
import animals.Dog; 
public class Farm { 
	Dog d; 
	public void f() { 
		d = new Dog(); 
		d.name = "Jessie"; 
	}
}
```
Does the compiler allow this?
?
Yes (but remember, as a general rule fields should be declared private)
<!--SR:!2024-12-01,44,266-->

animals/Dog.java
```java
package animals; 
public class Dog { 
	String name;
	⋮ 
}
```
buildings/Farm.java
```java
package buildings; 
import animals.Dog; 
public class Farm { 
	Dog d; 
	public void f() { 
		d = new Dog(); 
		d.name = "Jessie"; 
	}
}
```
Does the compiler allow this?
?
Yes, the field `name` is visible within the package `animals`.
<!--SR:!2024-12-31,58,246-->

animals/Dog.java
```java
package animals; 
public class Dog { 
	private String name;
	⋮ 
}
```
buildings/Farm.java
```java
package buildings; 
import animals.Dog; 
public class Farm { 
	Dog d; 
	public void f() { 
		d = new Dog(); 
		d.name = "Jessie"; 
	}
}
```
Does the compiler allow this?
?
No, `name` is visible only within the class `Dog`.
<!--SR:!2025-01-08,58,226-->

```java
public class Hyena {
    private String name;
    public Hyena(String name) {
        ...
    }
    public void laugh() {
        ...
    }
    public static Hyena create(String n) {
        ...
    }
}
```
Which of the following are valid ways to construct a `Hyena` object?
A. `Hyena h1 = new Hyena();`
B. `Hyena h2 = new Hyena("Hello");`
C. `Hyena h3 = new Hyena("Hi", 0);`
D. `Hyena h4;`
E. `Hyena h5 = new Hyena;`
?
B and D are valid.
<!--SR:!2024-12-07,47,250-->

```java
public class Hyena {
    private String name;
    public Hyena(String name) {
        ...
    }
    public void laugh() {
        ...
    }
    public static Hyena create(String n) {
        ...
    }
}
```
Which of the following are valid ways to call the `laugh` method from a class other than `Hyena`?
A. `Hyena.laugh();`
B. `Hyena h = create("haha"); h.laugh();`
C. `Hyena h; h.laugh();`
D. `Hyena h = Hyena.create("lol"); h.laugh();`
E. `Hyena h.laugh();`
?
D is valid.
<!--SR:!2024-11-30,38,230-->
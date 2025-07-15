# Java Exam Cheat Sheet

This cheat sheet focuses on tricky areas and common pitfalls to help you avoid mistakes during your exam.

---

## Primitive vs. Reference Types

### Primitives
- **Types**: `byte`, `short`, `int`, `long`, `float`, `double`, `char`, `boolean`
- **Comparison**: Use `==` to compare values.
- **Default Values**: Numeric types default to `0`; `boolean` defaults to `false`; `char` defaults to `'\u0000'`.

### Reference Types
- **Examples**: Objects, arrays, `String`, custom classes
- **Comparison**:
  - `==` compares references (memory addresses).
  - `.equals()` compares object content (must override `equals()` for custom comparison).
- **HashCode**:
  - When overriding `equals()`, also override `hashCode()`.
  - Equal objects must have equal hash codes.

---

## Mutable vs. Immutable Objects

### Immutable Objects
- **Cannot be modified** after creation.
- **Examples**: `String`, wrapper classes (`Integer`, `Double`, etc.).
- **Behavior**:
  - Modifying methods return a new object.
  - Safe to share across threads.

### Mutable Objects
- **Can be modified** after creation.
- **Examples**: `StringBuilder`, arrays, custom objects with setters.
- **Caution**: Changes affect all references to the object.

---

## Shallow vs. Deep Copy

### Shallow Copy
- **Copies object references**, not the actual objects.
- **Result**: Original and copy share the same referenced objects.
- **Implementation**: Default `clone()` method (unless overridden).

### Deep Copy
- **Copies all objects recursively**, creating new instances.
- **Result**: Original and copy are completely independent.
- **Implementation**: Manually clone mutable fields or use serialization.

---

## Type Casting

### Upcasting
- **From subclass to superclass**.
- **Implicit**: No cast needed.
- **Safe**: Always works.
  ```java
  Animal animal = new Dog(); // Dog is a subclass of Animal
  ```

### Downcasting
- **From superclass to subclass**.
- **Explicit**: Cast required.
- **Risky**: May cause `ClassCastException` at runtime.
  ```java
  Animal animal = new Dog();
  Dog dog = (Dog) animal; // Safe if 'animal' is actually a Dog
  ```
- **Avoid Errors**:
  - Use `instanceof` before casting.
    ```java
    if (animal instanceof Dog) {
        Dog dog = (Dog) animal;
    }
    ```

### Common Errors
- **Compile-time Error**: Incompatible types without a cast.
  ```java
  Dog dog = new Animal(); // Error: Cannot convert Animal to Dog
  ```
- **Runtime Error**: Invalid downcasting.
  ```java
  Animal animal = new Cat();
  Dog dog = (Dog) animal; // Runtime error: ClassCastException
  ```

---

## Modifiers: Access & Non-Access

### Access Modifiers
- **public**: Accessible from anywhere.
- **protected**: Accessible within the same package and subclasses.
- **Default (Package-Private)**: Accessible within the same package.
- **private**: Accessible only within the class.

### Non-Access Modifiers
- **static**:
  - Belongs to the class, not instances.
  - Can access static members without an object.
- **final**:
  - **Class**: Cannot be subclassed.
  - **Method**: Cannot be overridden.
  - **Variable**: Value cannot be changed once assigned.
- **abstract**:
  - **Class**: Cannot be instantiated; may contain abstract methods.
  - **Method**: Declared without an implementation.
- **transient**: Excluded from serialization.
- **volatile**: Indicates variable may be modified by multiple threads.

---

## `this` Keyword

- **Reference to the current object**.
- **Common Uses**:
  - **Disambiguate** between instance variables and parameters.
    ```java
    public class MyClass {
        private int value;
        public MyClass(int value) {
            this.value = value; // 'this.value' refers to the instance variable
        }
    }
    ```
  - **Invoke constructors** within another constructor.
    ```java
    public MyClass() {
        this(0); // Calls MyClass(int value)
    }
    ```

---

## Overloading vs. Overriding

### Overloading
- **Same method name**, different parameter lists.
- **Within the same class**.
- **Compile-time polymorphism**.
  ```java
  public int add(int a, int b) { ... }
  public double add(double a, double b) { ... }
  ```

### Overriding
- **Subclass provides implementation** for a method in its superclass.
- **Same method signature** (name, parameters).
- **Runtime polymorphism**.
- **Rules**:
  - **Access Level**: Cannot be more restrictive.
    - E.g., `public` method cannot be overridden as `protected`.
  - **Return Type**: Must be the same or covariant.
  - **Exceptions**: Cannot throw new or broader checked exceptions.
  - **Final Methods**: Cannot be overridden.
  - **Static Methods**: Cannot be overridden (they are hidden).

---

## Inheritance

### `super` Keyword
- **Access superclass members**.
- **Constructor Call**:
  - Must be the first statement in a subclass constructor.
    ```java
    public class Child extends Parent {
        public Child() {
            super(); // Calls Parent's constructor
        }
    }
    ```
- **Method Call**:
  - Call a method from the superclass.
    ```java
    @Override
    public void display() {
        super.display(); // Calls Parent's display()
        // Additional code
    }
    ```

### What Is Inherited
- **Inherited**:
  - Public and protected members.
  - Default (package-private) members if in the same package.
- **Not Inherited**:
  - Constructors.
  - Private members.
  - Final methods (cannot be overridden).

---

## Polymorphism

- **Ability of a variable to refer to objects of multiple types**.
- **Dynamic Method Dispatch**:
  - Method calls are resolved at runtime based on the object's actual type.
- **Example**:
  ```java
  Animal animal = new Dog();
  animal.makeSound(); // Calls Dog's implementation
  ```

### `instanceof` Operator
- **Checks object type** before casting.
- **Syntax**:
  ```java
  if (object instanceof Type) {
      // Safe to cast
  }
  ```
- **Example**:
  ```java
  if (animal instanceof Dog) {
      Dog dog = (Dog) animal;
      dog.bark();
  }
  ```

---

## Abstract Classes

- **Cannot be instantiated**.
- **May contain abstract methods** (without implementation).
- **Subclasses**:
  - Must implement all abstract methods or be declared abstract.
- **Use Cases**:
  - Provide a common base with shared code.
  - Define a template for subclasses.

---

## Lists and Their Implementations

### Arrays
- **Fixed size**.
- **Access Time**: O(1).
- **Insertion/Deletion**:
  - O(n) for arbitrary positions.
  - Efficient at the end (if size permits).

### Dynamic Arrays (`ArrayList`)
- **Resizable array implementation**.
- **Access Time**: O(1).
- **Insertion/Deletion**:
  - O(n) for arbitrary positions.
  - Amortized O(1) for adding/removing at the end.

### Linked Lists
- **Nodes linked via references**.
- **Types**: Singly, doubly linked.
- **Access Time**: O(n).
- **Insertion/Deletion**:
  - O(1) if the node reference is known.
  - O(n) to find the node.

### Running Time of Methods
- **Adding at End**:
  - **ArrayList**: Amortized O(1).
  - **LinkedList**: O(1).
- **Access by Index**:
  - **ArrayList**: O(1).
  - **LinkedList**: O(n).
- **Insertion at Beginning**:
  - **ArrayList**: O(n).
  - **LinkedList**: O(1).

---

## Sorting Algorithms

### Bubble Sort
- **Concept**: Repeatedly swap adjacent elements if they are in the wrong order.
- **Time Complexity**: O(n²).
- **Code**:
  ```java
  public void bubbleSort(int[] arr) {
      int n = arr.length;
      for (int i = 0; i < n - 1; i++) {
          for (int j = 0; j < n - i - 1; j++) {
              if (arr[j] > arr[j + 1]) {
                  // Swap arr[j] and arr[j+1]
                  int temp = arr[j];
                  arr[j] = arr[j + 1];
                  arr[j + 1] = temp;
              }
          }
      }
  }
  ```

### Selection Sort
- **Concept**: Select the minimum element from the unsorted portion and swap it with the first unsorted element.
- **Time Complexity**: O(n²).
- **Code**:
  ```java
  public void selectionSort(int[] arr) {
      int n = arr.length;
      for (int i = 0; i < n - 1; i++) {
          int minIdx = i;
          for (int j = i + 1; j < n; j++) {
              if (arr[j] < arr[minIdx]) {
                  minIdx = j;
              }
          }
          // Swap arr[minIdx] and arr[i]
          int temp = arr[minIdx];
          arr[minIdx] = arr[i];
          arr[i] = temp;
      }
  }
  ```

### Insertion Sort
- **Concept**: Build the sorted array one item at a time by inserting elements into their correct position.
- **Time Complexity**: O(n²).
- **Code**:
  ```java
  public void insertionSort(int[] arr) {
      int n = arr.length;
      for (int i = 1; i < n; ++i) {
          int key = arr[i];
          int j = i - 1;
          // Move elements greater than key to one position ahead
          while (j >= 0 && arr[j] > key) {
              arr[j + 1] = arr[j];
              j = j - 1;
          }
          arr[j + 1] = key;
      }
  }
  ```

---

## Common Mistakes & Tricky Points

### Access Modifiers
- **Private Methods**: Cannot be overridden.
- **Default Access**: Be cautious when classes are in different packages.

### Overriding Rules
- **Method Signature**: Must match exactly.
- **Return Type**: Can be covariant (return subtype).
- **Access Level**: Cannot be more restrictive.
- **Exceptions**: Subclass method cannot throw broader checked exceptions.

### `static` vs. Instance Context
- **Cannot use `this`** in a static context.
- **Static Methods** cannot access instance variables directly.

### `equals()` and `hashCode()`
- **Contract**: Equal objects must have equal hash codes.
- **Override Both**: When you override one, override the other.

### String Comparison
- **Use `.equals()`** to compare string contents.
  ```java
  String a = new String("test");
  String b = "test";
  if (a.equals(b)) { /* True */ }
  if (a == b) { /* False */ }
  ```

### Exception Handling
- **Order of Catch Blocks**: Catch more specific exceptions before general ones.
  ```java
  try {
      // code
  } catch (IOException e) {
      // handle IOException
  } catch (Exception e) {
      // handle other exceptions
  }
  ```

### Modifying Collections While Iterating
- **Avoid `ConcurrentModificationException`**:
  - Use `Iterator` and its `remove()` method.
    ```java
    Iterator<String> iterator = list.iterator();
    while (iterator.hasNext()) {
        String item = iterator.next();
        if (condition) {
            iterator.remove();
        }
    }
    ```

### Null References
- **Check for `null`** before calling methods on an object.
  ```java
  if (obj != null) {
      obj.doSomething();
  }
  ```

### Casting and Generics
- **Type Erasure**: Generics are erased at runtime.
- **Cannot Instantiate Generic Types**:
  ```java
  List<String> list = new ArrayList<String>();
  // Invalid: List<String> list = new List<String>();
  ```

---

## UML Diagrams

### Class Diagram Notations
- **Classes**:
  - **Class Name**
  - **Attributes**: `-` private, `#` protected, `+` public.
  - **Methods**: Same visibility symbols.
- **Relationships**:
  - **Inheritance**: Solid line with a hollow arrow pointing to the superclass.
  - **Interface Implementation**: Dashed line with a hollow arrow.
  - **Association**: Solid line.
  - **Aggregation**: Line with an unfilled diamond.
  - **Composition**: Line with a filled diamond.

---

## Final Tips

- **Review Overriding vs. Overloading**: Ensure method signatures and understand the difference.
- **Practice Type Casting**: Be cautious with downcasting and always check with `instanceof`.
- **Remember Access Levels**: Especially when dealing with packages.
- **Understand Collection Implementations**: Know when to use `ArrayList` vs. `LinkedList`.
- **Write Clean Code**: Indentation and clarity help prevent mistakes.

Good luck on your exam!
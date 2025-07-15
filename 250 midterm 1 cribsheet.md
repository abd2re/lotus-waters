---
cssclass: "columns"
---
## 1. Primitive vs. Reference Types

- **Comparison**:
  - **Primitives**: Use `==` for value comparison.
  - **References**: Use `equals()` for content comparison, `==` checks for reference equality.
- **HashCode**:
  - Consistent with `equals()`: If `a.equals(b)` is `true`, then `a.hashCode() == b.hashCode()` should be `true`.
  - Override both `equals()` and `hashCode()` when customizing equality logic.

## 2. Mutable vs. Immutable Objects

- **Immutable Objects**:
  - State cannot be changed after creation (e.g., `String`, `Integer`).
  - Advantages: Thread-safe, can be safely shared.
- **Mutable Objects**:
  - State can be changed (e.g., `StringBuilder`, custom objects).
- **Common Pitfall**:
  - Modifying objects while iterating can cause `ConcurrentModificationException`.

## 3. Shallow vs. Deep Copy

- **Shallow Copy**:
  - Copies object references, not the actual objects.
  - Modifications to nested objects affect both copies.
- **Deep Copy**:
  - Creates new instances of nested objects.
  - Use serialization or custom cloning for deep copies.
- **Cloning**:
  - Implement `Cloneable` and override `clone()` method.
  - `clone()` does a shallow copy by default.

## 4. Type Casting

- **Upcasting** (Implicit):
  - Casting a subclass to a superclass.
  - Always safe; no explicit cast needed.
- **Downcasting** (Explicit):
  - Casting a superclass to a subclass.
  - Requires explicit cast; may cause `ClassCastException` at runtime.
- **Compile-time Errors**:
  - Incompatible types that cannot be cast.
- **Runtime Errors**:
  - Casting to incorrect type causes exceptions.

## 5. Modifiers in Classes and Methods

- **Access Modifiers**:
  - `public`: Accessible everywhere.
  - `protected`: Accessible in the same package and subclasses.
  - `default` (no modifier): Accessible in the same package.
  - `private`: Accessible within the class only.
- **Non-Access Modifiers**:
  - `static`: Belongs to the class, not instances.
  - `final`: Cannot be changed or overridden.
  - `abstract`: Must be implemented in a subclass.
- **Common Mistakes**:
  - Overriding `final` methods (compile-time error).
  - Accessing private members from subclasses.

## 6. The `this` Keyword

- **Usage**:
  - Reference the current object.
  - Resolve naming conflicts between instance variables and parameters.
  - Invoke other constructors in the same class: `this(params);`

## 7. Overloading vs. Overriding

- **Overloading**:
  - Same method name, different parameters.
  - Compile-time polymorphism.
- **Overriding**:
  - Subclass method replaces superclass method.
  - Runtime polymorphism.
- **Rules for Overriding**:
  - Method must have the same name, parameters, and return type.
  - Access level can't be more restrictive.
  - Overridden methods cannot throw new or broader checked exceptions.
  - Use `@Override` annotation to avoid mistakes.

## 8. Inheritance and Polymorphism

- **Inheritance**:
  - Use `extends` for classes, `implements` for interfaces.
  - The `super` keyword:
    - Access superclass methods and constructors.
    - Must be the first statement in a constructor.
- **What Is Inherited**:
  - Public and protected members.
  - Constructors are **not** inherited.
- **Polymorphism**:
  - An object can take many forms.
  - Method to handle objects of different classes through a common interface.
- **`instanceof` Operator**:
  - Check object type at runtime.
  - Syntax: `if (obj instanceof ClassName)`

## 9. Abstract Classes

- **Characteristics**:
  - Cannot be instantiated.
  - May contain abstract methods (without implementation).
  - Can have concrete methods.
- **When to Use**:
  - When you have a base class that should not be instantiated.
  - To provide a common template for subclasses.
- **Common Pitfall**:
  - Forgetting to implement all abstract methods in subclasses.

## 10. Sorting Algorithms

- **Bubble Sort**:
  - Repeatedly swap adjacent elements if they are in the wrong order.
  - Time Complexity: O(n²)
- **Selection Sort**:
  - Select the minimum element and swap it with the first unsorted element.
  - Time Complexity: O(n²)
- **Insertion Sort**:
  - Build the sorted array one item at a time.
  - Time Complexity: O(n²), efficient for small or nearly sorted data.
- **Implementation Tips**:
  - Pay attention to loop boundaries.
  - Optimize by stopping early if the array is already sorted.

## 11. Lists and Their Implementations

- **Arrays**:
  - Fixed size.
  - Random access: O(1).
- **Dynamic Arrays (`ArrayList`)**:
  - Resizable array implementation.
  - Adding/removing at the end: O(1) amortized.
  - Insertion/removal at arbitrary positions: O(n).
- **Linked Lists (`LinkedList`)**:
  - Elements linked via nodes.
  - Insertion/removal at the beginning/end: O(1).
  - Access by index: O(n).
- **Common Mistakes**:
  - Ignoring the cost of operations for large datasets.
  - Choosing the wrong data structure for the required operations.

## 12. Additional Exam Tips

- **Static vs. Non-Static Context**:
  - Static methods cannot access non-static members directly.
  - Be cautious of context when accessing class members.
- **Final Keyword**:
  - For variables: value cannot be changed.
  - For methods: cannot be overridden.
  - For classes: cannot be subclassed.
- **Exception Handling**:
  - Checked exceptions must be declared or handled.
  - Overridden methods cannot throw new or broader checked exceptions.
- **UML Diagrams**:
  - Understand class relationships: inheritance (solid line with a hollow arrow), associations, dependencies.
  - Recognize common notation for modifiers:
    - `+`: public
    - `#`: protected
    - `~`: package-private
    - `-`: private


---
---

### Bubble sort
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
  ```

### Selection Sort
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
  ```

### Insertion Sort
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
  ```

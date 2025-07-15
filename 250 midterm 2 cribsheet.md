## **Quicksort**

1. Choose a **pivot** (commonly the last element or median).
2. **Partition**:
   - Rearrange elements such that:
     - Elements \( < \) pivot come before it.
     - Elements \( $\geq$ \) pivot come after it.
3. **Recursively** sort the subarrays before and after the pivot.

```java
void quicksort(int[] arr, int low, int high) {
    if (low < high) {
        int pi = partition(arr, low, high); // Partition index
        quicksort(arr, low, pi - 1); // Sort left part
        quicksort(arr, pi + 1, high); // Sort right part
    }
}

int partition(int[] arr, int low, int high) {
    int pivot = arr[high]; // Pivot element
    int i = low - 1; // Index for smaller elements
    for (int j = low; j < high; j++) {
        if (arr[j] < pivot) {
            i++;
            swap(arr, i, j);
        }
    }
    swap(arr, i + 1, high); // Place pivot in correct position
    return i + 1;
}

void swap(int[] arr, int i, int j) {
    int temp = arr[i];
    arr[i] = arr[j];
    arr[j] = temp;
}
```

- **Best/Average Case**: \( O(n \log n) \) (balanced partitions).
- **Worst Case**: \( O(n^2) \) (poor pivot choice, e.g., sorted array).

---

## **Mergesort**

1. **Divide**:
   - Split the array into two halves recursively until size = 1.
2. **Merge**:
   - Combine sorted halves into a single sorted array.

```java
void mergesort(int[] arr, int l, int r) {
    if (l < r) {
        int mid = l + (r - l) / 2;
        mergesort(arr, l, mid); // Sort left half
        mergesort(arr, mid + 1, r); // Sort right half
        merge(arr, l, mid, r); // Merge sorted halves
    }
}

void merge(int[] arr, int l, int mid, int r) {
    int n1 = mid - l + 1;
    int n2 = r - mid;
    int[] L = new int[n1];
    int[] R = new int[n2];
    
    System.arraycopy(arr, l, L, 0, n1);
    System.arraycopy(arr, mid + 1, R, 0, n2);
    
    int i = 0, j = 0, k = l;
    while (i < n1 && j < n2) {
        if (L[i] <= R[j]) arr[k++] = L[i++];
        else arr[k++] = R[j++];
    }
    while (i < n1) arr[k++] = L[i++];
    while (j < n2) arr[k++] = R[j++];
}
```

- **Best/Worst/Average Case**: \( O(n \log n) \).
- **Space Complexity**: \( O(n) \).

---

## **Binary Search Tree (BST)**

- Left child: Keys \( < \) root.
- Right child: Keys \( > \) root.
### **Deletion**
1. **Case 1**: Node has **no children** (leaf).
   - Directly remove the node.
2. **Case 2**: Node has **one child**.
   - Replace the node with its child.
3. **Case 3**: Node has **two children**.
   - Find the **in-order successor** (smallest value in the right subtree).
   - Replace the node with the in-order successor.
   - Delete the in-order successor from its original position.

```java
Node delete(Node root, int key) {
    if (root == null) return root; // Base case

    if (key < root.val) root.left = delete(root.left, key); // Go left
    else if (key > root.val) root.right = delete(root.right, key); // Go right
    else { // Node to be deleted
        if (root.left == null) return root.right; // One child or no child
        else if (root.right == null) return root.left;

        // Two children: Get in-order successor
        root.val = findMin(root.right).val;
        root.right = delete(root.right, root.val); // Remove successor
    }
    return root;
}

Node findMin(Node root) {
    while (root.left != null) root = root.left;
    return root;
}
```

- **Search/Insert/Delete**:
  - **Average**: \( O(\log n) \).
  - **Worst**: \( O(n) \) (unbalanced tree).

---

## **Rooted Tree**

1. **Root**: The top node.
2. **Parent-Child Relationship**:
   - Each node has one parent (except the root).
   - A node can have zero or more children.
3. **Depth**:
   - Number of edges from root to node.
4. **Height**:
   - Number of edges on the longest path from root to a leaf.

1. **Pre-order**: Visit root → Traverse left → Traverse right.
2. **Post-order**: Traverse left → Traverse right → Visit root.
3. **Level-order**: Traverse level by level (using a queue).

```java
void preOrder(Node root) {
    if (root == null) return;
    System.out.print(root.val + " ");
    preOrder(root.left);
    preOrder(root.right);
}
```

```java
void levelOrder(Node root) {
    if (root == null) return;
    Queue<Node> queue = new LinkedList<>();
    queue.add(root);
    while (!queue.isEmpty()) {
        Node current = queue.poll();
        System.out.print(current.val + " ");
        if (current.left != null) queue.add(current.left);
        if (current.right != null) queue.add(current.right);
    }
}
```

# Algorithm for Simple Queue Operations
## Insert (Enqueue) Operation
1. **Start**  
2. Check if the queue is full:  
   - If `rear == maxSize - 1`, display "Queue is full" and exit.
3. If the queue is not full:  
   - Increment `rear` by 1: `rear = rear + 1`
   - Insert the element at `queue[rear]`
4. If this is the first element (when `front == -1`):  
   - Set `front = 0`
5. **Stop**
## Delete (Dequeue) Operation
1. **Start**  
2. Check if the queue is empty:  
   - If `front == -1` or `front > rear`, display "Queue is empty" and exit.
3. If the queue is not empty:  
   - Remove the element at `queue[front]`
   - Increment `front` by 1: `front = front + 1`
4. If the queue becomes empty after this operation (when `front > rear`):  
   - Reset `front = -1` and `rear = -1`
5. **Stop**
---
---
---
# Algorithm to Reverse a Linked List
## Input:
A singly linked list with `head` pointing to the first node.
## Output:
The linked list reversed.
1. **Start**
2. Initialize three pointers:  
   - `prev = NULL`  
   - `current = head`  
   - `next = NULL`
3. Repeat the following steps until `current` becomes `NULL`:
   - Set `next = current->next` (store the next node)
   - Update `current->next = prev` (reverse the pointer)
   - Move `prev` to `current`: `prev = current`
   - Move `current` to `next`: `current = next`
4. Update `head = prev` (set the new head of the reversed list)
5. **Stop**
---
---
---
# Tree Traversal Methods  
Tree traversal refers to visiting all nodes of a tree systematically. The main methods are:  
### Example:  
**Tree Structure**  
  1  
 / \  
2   3  
/     \
4     5
## 1. **In-order Traversal (Left, Root, Right)**  
### Algorithm:  
1. Traverse the left subtree.  
2. Visit the root node.  
3. Traverse the right subtree.  
**In-order Output:** `4, 2, 5, 1, 3`  
## 2. **Pre-order Traversal (Root, Left, Right)**  
### Algorithm:  
1. Visit the root node.  
2. Traverse the left subtree.  
3. Traverse the right subtree.  
**Pre-order Output:** `1, 2, 4, 5, 3`  
## 3. **Post-order Traversal (Left, Right, Root)**  
### Algorithm:  
1. Traverse the left subtree.  
2. Traverse the right subtree.  
3. Visit the root node.  
**Post-order Output:** `4, 5, 2, 3, 1`  
---
---
---
# Difference Between Stack and Queue  
| **Aspect**         | **Stack**                          | **Queue**                         |
|---------------------|------------------------------------|------------------------------------|
| **Definition**      | A linear data structure that follows the **LIFO** (Last In, First Out) principle. | A linear data structure that follows the **FIFO** (First In, First Out) principle. |
| **Insertion**       | Performed using `push()` at the top of the stack. | Performed using `enqueue()` at the rear of the queue. |
| **Deletion**        | Performed using `pop()` from the top of the stack. | Performed using `dequeue()` from the front of the queue. |
| **Access**          | Only the top element can be accessed. | Only the front element can be accessed. |
| **Example**         | Browser backtracking (undo operations). | Printer job scheduling or ticket booking system. |
| **Operations**      | `Push`, `Pop`, `Peek`             | `Enqueue`, `Dequeue`, `Peek`      |
| **Structure**       | Linear, works like a stack of plates. | Linear, works like a queue in a line. |

---
---
---
# Algorithms for Stack Operations  
## 1. **Push (Insert Element)**  
### Algorithm:  
1. **Start**  
2. Check if the stack is full:  
   - If `top == maxSize - 1`, display "Stack Overflow" and exit.  
3. If not full:  
   - Increment `top = top + 1`.  
   - Insert the element at `stack[top]`.  
4. **Stop**  
## 2. **Pop (Remove Element)**  
### Algorithm:  
1. **Start**  
2. Check if the stack is empty:  
   - If `top == -1`, display "Stack Underflow" and exit.  
3. If not empty:  
   - Retrieve the element at `stack[top]`.  
   - Decrement `top = top - 1`.  
4. **Stop**  
## 3. **Peek (Access Top Element)**  
### Algorithm:  
1. **Start**  
2. Check if the stack is empty:  
   - If `top == -1`, display "Stack is empty" and exit.  
3. If not empty:  
   - Return the element at `stack[top]`.  
4. **Stop**  
## 4. **IsEmpty (Check if Stack is Empty)**  
### Algorithm:  
1. **Start**  
2. If `top == -1`, return **true**.  
3. Otherwise, return **false**.  
4. **Stop**  
## 5. **IsFull (Check if Stack is Full)**  
### Algorithm:  
1. **Start**  
2. If `top == maxSize - 1`, return **true**.  
3. Otherwise, return **false**.  
4. **Stop**  
---
---
---
# Binary Search  
Binary search is an efficient algorithm used to find the position of a target element in a **sorted array**. It works by repeatedly dividing the search interval in half.
## Algorithm:  
1. **Start**  
2. Initialize two pointers:  
   - `low = 0` (starting index)  
   - `high = n - 1` (last index of the array)  
3. Repeat the following steps until `low <= high`:  
   - Calculate the middle index: `mid = (low + high) / 2`.  
   - Compare the target with the element at `arr[mid]`:  
     - If `arr[mid] == target`, return `mid` (element found).  
     - If `arr[mid] < target`, set `low = mid + 1` (search in the right half).  
     - If `arr[mid] > target`, set `high = mid - 1` (search in the left half).  
4. If `low > high`, the target is not present in the array.  
5. **Stop**  
## Example:  
### Problem:  
Find the position of `25` in the sorted array: `[10, 15, 20, 25, 30, 35, 40]`.  
### Steps:  
1. Initial `low = 0`, `high = 6`, and `mid = (0 + 6) / 2 = 3`.  
   - Check `arr[3] = 25`.  
   - `arr[3] == 25`, so the element is found at index `3`.  
### Output:  
The position of `25` is **index 3** in the array.  

---
---
---
# Bubble Sort  
Bubble sort is a simple sorting algorithm that repeatedly compares adjacent elements and swaps them if they are in the wrong order. It continues until the entire list is sorted.
## Algorithm:  
1. **Start**  
2. Let `n` be the number of elements in the array.  
3. Repeat the following steps for `i = 0` to `n - 2`:  
   - For each element `j` from `0` to `n - i - 2`:  
     - If `arr[j] > arr[j + 1]`:  
       - Swap `arr[j]` and `arr[j + 1]`.  
4. If no swaps occur during a pass, the array is already sorted.  
5. **Stop**  
## Example:  
### Problem:  
Sort the array `[5, 3, 8, 4, 2]` using bubble sort.  
### Steps:  
1. **Pass 1**: Compare and swap adjacent elements:  
   `[5, 3, 8, 4, 2] → [3, 5, 8, 4, 2] → [3, 5, 4, 8, 2] → [3, 5, 4, 2, 8]`.  
2. **Pass 2**:  
   `[3, 5, 4, 2, 8] → [3, 4, 5, 2, 8] → [3, 4, 2, 5, 8]`.  
3. **Pass 3**:  
   `[3, 4, 2, 5, 8] → [3, 2, 4, 5, 8]`.  
4. **Pass 4**:  
   `[3, 2, 4, 5, 8] → [2, 3, 4, 5, 8]`.  
### Output:  
The sorted array is `[2, 3, 4, 5, 8]`.  

---
---
---
# What is a Data Structure?
A **data structure** is a way to organize, manage, and store data in a computer so that it can be accessed and modified efficiently. It is used to handle large amounts of data and perform operations like searching, sorting, inserting, deleting, and updating.
# Types of Data Structures  
## 1. **Linear Data Structures**  
In linear data structures, elements are arranged sequentially, and each element is connected to its previous and next element.
### Examples:  
- **Array**: A collection of elements stored at contiguous memory locations.  
- **Stack**: Follows the **LIFO** (Last In, First Out) principle.  
- **Queue**: Follows the **FIFO** (First In, First Out) principle.  
- **Linked List**: A collection of nodes where each node contains data and a reference to the next node.
## 2. **Non-linear Data Structures**  
In non-linear data structures, elements are not arranged sequentially. These are used to represent hierarchical relationships or connections.
### Examples:  
- **Tree**: A hierarchical structure with nodes, where each node can have child nodes (e.g., Binary Tree, Binary Search Tree).  
- **Graph**: Consists of vertices (nodes) and edges (connections) to represent networks.  
## 3. **Dynamic Data Structures**  
These data structures can grow or shrink in size during runtime.
### Examples:  
- **Linked Lists**  
- **Stacks and Queues (Dynamic Implementation)**  
## 4. **Hash-based Data Structures**  
These store data using key-value pairs for quick access.
### Examples:  
- **Hash Table**  
- **Hash Map**  
---
---
---
# Algorithm to Insert a Node at the Beginning of a Singly Linked List  
### Algorithm:
1. **Start**  
2. Create a new node `newNode`.
   - Set `newNode.data = value` (the data to be inserted).
   - Set `newNode.next = NULL`.
3. Check if the linked list is empty (i.e., `head == NULL`):  
   - If `head == NULL`, set `head = newNode` (new node becomes the first node).
4. If the list is not empty:
   - Set `newNode.next = head` (make the new node point to the old first node).
   - Set `head = newNode` (update the head to the new node).
5. **Stop**
### Example:
Consider an initial linked list: `head -> 2 -> 3 -> NULL`
- After inserting `1` at the beginning, the linked list will become: `head -> 1 -> 2 -> 3 -> NULL`
---
---
---
# Algorithm to Insert a Node in a Binary Tree
### Algorithm:
1. **Start**
2. Create a new node `newNode`.
   - Set `newNode.data = value` (the data to be inserted).
   - Set `newNode.left = NULL` and `newNode.right = NULL`.
3. If the tree is empty (i.e., `root == NULL`):
   - Set `root = newNode` (new node becomes the root).
4. If the tree is not empty:
   - Initialize a queue to perform a level-order traversal.
   - Enqueue the `root` node.
   - While the queue is not empty:
     - Dequeue the front node, call it `current`.
     - If `current.left == NULL`:
       - Set `current.left = newNode` (insert the node as the left child).
       - Exit.
     - If `current.right == NULL`:
       - Set `current.right = newNode` (insert the node as the right child).
       - Exit.
     - Otherwise, enqueue the left and right children of `current`.
5. **Stop**
### Example:
Consider a binary tree with the following structure:
  10
 /  \
20   30
- After inserting `40`, the tree will become:
  10
 /  \
20   30
/
40
The new node is inserted as the left child of `20`.

---
---
---
# Sequential Search  
**Sequential Search** is a simple searching algorithm that checks each element of the list sequentially until the target element is found or the entire list has been searched. It works on both sorted and unsorted lists.
### Algorithm for Sequential Search:
1. **Start**
2. Begin from the first element of the list.
3. Compare each element of the list with the target value:
   - If the current element matches the target, return the index of the element.
   - If the current element does not match the target, move to the next element.
4. Repeat step 3 until you reach the end of the list or the target is found.
5. If the target element is not found by the time the end of the list is reached, return `-1` or "Not Found".
6. **Stop**
### Example:
Given the list: `[4, 2, 7, 9, 1]`, find the position of the target value `9`.
- Start from the first element:
  - Compare `4` with `9` → not a match.
  - Compare `2` with `9` → not a match.
  - Compare `7` with `9` → not a match.
  - Compare `9` with `9` → match found.
- The element `9` is found at index `3`.
### Output:
The target `9` is found at index `3`.
### Time Complexity:
- **Best case**: `O(1)` (If the target is the first element in the list).
- **Worst case**: `O(n)` (If the target is at the last position or not in the list).
---
---
---
# Selection Sort  
**Selection Sort** is a simple sorting algorithm that repeatedly selects the smallest (or largest) element from the unsorted portion of the list and swaps it with the first unsorted element. It continues this process until the entire list is sorted.
### Algorithm for Selection Sort:
1. **Start**
2. Loop through the array from the first element to the second last element:
   - Set `min_index = i` (assume the current index is the smallest).
   - Loop through the remaining unsorted elements starting from `i+1` to find the smallest element:
     - If `arr[j] < arr[min_index]`, update `min_index = j`.
   - After finding the minimum element in the remaining unsorted part, swap it with the element at index `i` (i.e., `arr[i]` and `arr[min_index]`).
3. Repeat step 2 until the entire list is sorted.
4. **Stop**
### Example:
Given the array: `[64, 25, 12, 22, 11]`
1. **Pass 1**:  
   - `min_index = 0`, `arr[0] = 64`.  
   - Compare `64` with the rest of the elements:
     - `64 > 25`, so update `min_index = 1`.
     - `25 < 12`, so update `min_index = 2`.
     - `12 < 22`, so update `min_index = 3`.
     - `12 < 11`, so update `min_index = 4`.
   - Swap `arr[0]` and `arr[4]`, resulting in `[11, 25, 12, 22, 64]`.
2. **Pass 2**:  
   - `min_index = 1`, `arr[1] = 25`.  
   - Compare `25` with the rest of the elements:
     - `25 > 12`, so update `min_index = 2`.
     - `12 < 22`, so `min_index` remains `2`.
   - Swap `arr[1]` and `arr[2]`, resulting in `[11, 12, 25, 22, 64]`.
3. **Pass 3**:  
   - `min_index = 2`, `arr[2] = 25`.  
   - Compare `25` with `22`:
     - `25 > 22`, so update `min_index = 3`.
   - Swap `arr[2]` and `arr[3]`, resulting in `[11, 12, 22, 25, 64]`.
4. **Pass 4**:  
   - `min_index = 3`, `arr[3] = 25`.  
   - No changes needed as `25 < 64`.
   - Array remains `[11, 12, 22, 25, 64]`.
### Output:
The sorted array is `[11, 12, 22, 25, 64]`.
### Time Complexity:
- **Best case**: `O(n^2)`
- **Worst case**: `O(n^2)`
- **Average case**: `O(n^2)`
---
---
---
# Insertion Sort  
**Insertion Sort** is a simple sorting algorithm that builds the final sorted array one element at a time. It is much like sorting playing cards in your hands. The array is divided into two parts: a sorted part and an unsorted part. The algorithm repeatedly picks the first element from the unsorted part and inserts it into the correct position in the sorted part.
### Algorithm for Insertion Sort:
1. **Start**
2. Loop through the array from the second element to the last element:
   - Set the current element as `key = arr[i]` where `i` is the current index.
   - Compare the `key` with the elements before it (from `i-1` to `0`):
     - If `arr[j] > key`, move `arr[j]` one position to the right.
     - Repeat this until you find the correct position for `key`.
   - Insert `key` at the correct position.
3. Repeat step 2 until the entire array is sorted.
4. **Stop**
### Example:
Given the array: `[12, 11, 13, 5, 6]`
1. **Pass 1**:  
   - `key = 11`, compare with `12`. Since `11 < 12`, move `12` to the right.  
   - Insert `11` in the first position. Array becomes: `[11, 12, 13, 5, 6]`.
2. **Pass 2**:  
   - `key = 13`, compare with `12`. Since `13 > 12`, no changes needed. Array remains: `[11, 12, 13, 5, 6]`.
3. **Pass 3**:  
   - `key = 5`, compare with `13`, `12`, and `11`. Move `13`, `12`, and `11` one position to the right.  
   - Insert `5` at the first position. Array becomes: `[5, 11, 12, 13, 6]`.
4. **Pass 4**:  
   - `key = 6`, compare with `13`, `12`, and `11`. Move `13`, `12`, and `11` one position to the right.  
   - Insert `6` at the second position. Array becomes: `[5, 6, 11, 12, 13]`.
### Output:
The sorted array is `[5, 6, 11, 12, 13]`.
### Time Complexity:
- **Best case**: `O(n)` (If the array is already sorted).
- **Worst case**: `O(n^2)` (If the array is sorted in reverse order).
- **Average case**: `O(n^2)`
---
---
---
# Bubble Sort  
**Bubble Sort** is a simple comparison-based sorting algorithm. It repeatedly steps through the list, compares adjacent elements, and swaps them if they are in the wrong order. The process is repeated until the list is sorted. The algorithm gets its name from the way smaller elements "bubble" to the top (beginning of the list).
### Algorithm for Bubble Sort:
1. **Start**
2. Loop through the array from the first element to the second last element:
   - Compare each pair of adjacent elements (`arr[i]` and `arr[i+1]`).
   - If `arr[i] > arr[i+1]`, swap the elements.
3. After each pass through the array, the largest element moves to the end (bubbles up).
4. Repeat step 2 for the entire array, reducing the size of the unsorted portion after each pass.
5. Continue until no swaps are needed, which means the array is sorted.
6. **Stop**
### Example:
Given the array: `[64, 34, 25, 12, 22, 11, 90]`
1. **Pass 1**:  
   - Compare `64` and `34`, swap them → `[34, 64, 25, 12, 22, 11, 90]`
   - Compare `64` and `25`, swap them → `[34, 25, 64, 12, 22, 11, 90]`
   - Compare `64` and `12`, swap them → `[34, 25, 12, 64, 22, 11, 90]`
   - Compare `64` and `22`, swap them → `[34, 25, 12, 22, 64, 11, 90]`
   - Compare `64` and `11`, swap them → `[34, 25, 12, 22, 11, 64, 90]`
   - Compare `64` and `90`, no swap needed → `[34, 25, 12, 22, 11, 64, 90]`
   - After the first pass, the largest element `90` is correctly placed at the end.
2. **Pass 2**:  
   - Compare `34` and `25`, swap them → `[25, 34, 12, 22, 11, 64, 90]`
   - Compare `34` and `12`, swap them → `[25, 12, 34, 22, 11, 64, 90]`
   - Compare `34` and `22`, swap them → `[25, 12, 22, 34, 11, 64, 90]`
   - Compare `34` and `11`, swap them → `[25, 12, 22, 11, 34, 64, 90]`
   - Compare `34` and `64`, no swap needed → `[25, 12, 22, 11, 34, 64, 90]`
   - After the second pass, the second largest element `64` is placed in the correct position.
3. **Pass 3**:  
   - Compare `25` and `12`, swap them → `[12, 25, 22, 11, 34, 64, 90]`
   - Compare `25` and `22`, swap them → `[12, 22, 25, 11, 34, 64, 90]`
   - Compare `25` and `11`, swap them → `[12, 22, 11, 25, 34, 64, 90]`
   - Compare `25` and `34`, no swap needed → `[12, 22, 11, 25, 34, 64, 90]`
   - After the third pass, the third largest element `34` is in the correct position.
4. **Pass 4**:  
   - Compare `12` and `22`, no swap needed → `[12, 22, 11, 25, 34, 64, 90]`
   - Compare `22` and `11`, swap them → `[12, 11, 22, 25, 34, 64, 90]`
   - Compare `22` and `25`, no swap needed → `[12, 11, 22, 25, 34, 64, 90]`
   - After the fourth pass, the fourth largest element `25` is in the correct position.
5. **Pass 5**:  
   - Compare `12` and `11`, swap them → `[11, 12, 22, 25, 34, 64, 90]`
   - After the fifth pass, the list is fully sorted: `[11, 12, 22, 25, 34, 64, 90]`.
### Output:
The sorted array is `[11, 12, 22, 25, 34, 64, 90]`.
### Time Complexity:
- **Best case**: `O(n)` (If the array is already sorted, only one pass is needed).
- **Worst case**: `O(n^2)` (If the array is sorted in reverse order).
- **Average case**: `O(n^2)`
---
---
---
# Difference Between Primitive and Non-Primitive Data Types
| Feature                 | Primitive Data Types      | Non-Primitive Data Types     |
|-------------------------|----------------------------|------------------------------|
| **Definition**           | Basic data types provided by the language. | Complex types built from primitive types or other non-primitive types. |
| **Size**                 | Fixed size.                | Varies depending on the type or structure. |
| **Memory Allocation**    | Direct memory allocation (stack). | Dynamic memory allocation (heap). |
| **Storage**              | Stored directly in memory. | Stored as references or pointers. |
| **Examples**             | `int`, `char`, `boolean`.  | Arrays, Objects, Strings. |
| **Mutability**           | Immutable.                 | Mutable. |
| **Operations**           | Basic operations (e.g., arithmetic). | Complex operations (e.g., manipulation of objects or collections). |

---
---
---
# Algorithms for Stack Operations
A **stack** is a linear data structure that follows the **Last In First Out (LIFO)** principle. It supports operations such as push, pop, peek, and isEmpty.
## 1. **Push Operation** (To add an element to the stack)
### Algorithm for Push:
1. **Start**
2. Check if the stack is full (optional, depending on whether the stack is implemented with a fixed size).
   - If full, return "Stack Overflow" and stop.
3. Increment the top pointer (`top = top + 1`).
4. Add the element at the new position (`stack[top] = element`).
5. **Stop**
### Example:
If the stack is `top = -1` and `stack = []`:
- Push `5`: `top = 0`, `stack = [5]`
- Push `10`: `top = 1`, `stack = [5, 10]`
## 2. **Pop Operation** (To remove an element from the stack)
### Algorithm for Pop:
1. **Start**
2. Check if the stack is empty.
   - If empty, return "Stack Underflow" and stop.
3. Retrieve the element at the top of the stack (`element = stack[top]`).
4. Decrement the top pointer (`top = top - 1`).
5. Return the popped element.
6. **Stop**
### Example:
If the stack is `top = 1` and `stack = [5, 10]`:
- Pop: Return `10`, `top = 0`, `stack = [5]`
## 3. **Peek Operation** (To view the top element without removing it)
### Algorithm for Peek:
1. **Start**
2. Check if the stack is empty.
   - If empty, return "Stack is Empty" and stop.
3. Return the element at the top of the stack (`stack[top]`).
4. **Stop**
### Example:
If the stack is `top = 1` and `stack = [5, 10]`:
- Peek: Return `10`, stack remains `[5, 10]`
## 4. **isEmpty Operation** (To check if the stack is empty)
### Algorithm for isEmpty:
1. **Start**
2. Check if `top == -1` (indicating an empty stack).
   - If true, return `true` (stack is empty).
   - Else, return `false` (stack is not empty).
3. **Stop**
### Example:
If the stack is `top = -1` and `stack = []`:
- isEmpty: Return `true`
If the stack is `top = 0` and `stack = [5]`:
- isEmpty: Return `false`
## 5. **isFull Operation** (To check if the stack is full, applicable in fixed-size stacks)
### Algorithm for isFull:
1. **Start**
2. Check if `top == maxSize - 1` (indicating the stack is full).
   - If true, return `true` (stack is full).
   - Else, return `false` (stack is not full).
3. **Stop**
### Example:
If the stack has `maxSize = 5` and `top = 4`:
- isFull: Return `true`
If `top = 3`, `maxSize = 5`:
- isFull: Return `false`
---
---
---
# Circular Queue
A **Circular Queue** is a linear data structure that follows the **First In First Out (FIFO)** principle. Unlike a regular queue, the last position is connected to the first position to form a circle. When the queue is full and an element is dequeued, the front pointer moves to the beginning of the queue, making space for new elements. This efficient use of space avoids the "wasting" of space that occurs in a regular queue.
### Features:
- **Fixed size**: The size of the circular queue is fixed.
- **Front and Rear pointers**: The queue uses two pointers, `front` (points to the front element) and `rear` (points to the last element).
- **Full condition**: The queue is considered full if the next position of `rear` (i.e., `(rear + 1) % size`) equals `front`.
### Circular Queue Operations:
1. **Insert (Enqueue)**: Adds an element to the queue.
2. **Delete (Dequeue)**: Removes an element from the queue.
## 1. **Insert (Enqueue) Operation for Circular Queue**
### Algorithm for Insert:
1. **Start**
2. Check if the queue is full:
   - If `(rear + 1) % size == front`, return "Queue is Full".
3. If the queue is not full:
   - If the queue is empty (`front == -1`), set both `front = 0` and `rear = 0`.
   - Else, set `rear = (rear + 1) % size`.
   - Insert the element at `queue[rear]`.
4. **Stop**
### Example:
Given a circular queue of size 5:
- Initially: `front = -1`, `rear = -1`, `queue = [_, _, _, _, _]`.
- Insert 10: `front = 0`, `rear = 0`, `queue = [10, _, _, _, _]`.
- Insert 20: `front = 0`, `rear = 1`, `queue = [10, 20, _, _, _]`.
- Insert 30: `front = 0`, `rear = 2`, `queue = [10, 20, 30, _, _]`.
## 2. **Delete (Dequeue) Operation for Circular Queue**
### Algorithm for Delete:
1. **Start**
2. Check if the queue is empty:
   - If `front == -1`, return "Queue is Empty".
3. If the queue is not empty:
   - Retrieve the element at `queue[front]` and store it.
   - If `front == rear`, set both `front = -1` and `rear = -1` (queue becomes empty).
   - Else, set `front = (front + 1) % size`.
4. **Stop**
### Example:
Given a circular queue of size 5:
- Initially: `front = 0`, `rear = 2`, `queue = [10, 20, 30, _, _]`.
- Delete: `front = 1`, `rear = 2`, `queue = [_, 20, 30, _, _]` (returns 10).
- Delete: `front = 2`, `rear = 2`, `queue = [_, _, 30, _, _]` (returns 20).
- Delete: `front = -1`, `rear = -1`, `queue = [_, _, _, _, _]` (returns 30 and makes the queue empty).
### Time Complexity:
- **Insertion**: `O(1)`
- **Deletion**: `O(1)`
---
---
---
# Comparison of Simple Queue, Double Ended Queue (Deque), and Circular Queue
| Feature                    | Simple Queue                     | Circular Queue                  | Double Ended Queue (Deque)      |
|----------------------------|-----------------------------------|----------------------------------|---------------------------------|
| **Definition**              | A queue where elements are added at the rear and removed from the front. | A queue where the last position is connected to the first, forming a circular structure. | A queue where elements can be added or removed from both ends. |
| **Direction of Operation**  | FIFO (First In First Out)         | FIFO, but allows wrapping around the rear to the front. | Both FIFO and LIFO (Last In First Out) depending on the operation. |
| **Insertion**               | At the rear end.                  | At the rear end, but wraps around if full. | At both ends (front or rear). |
| **Deletion**                | From the front end.               | From the front end, but wraps around if front exceeds rear. | From both ends (front or rear). |
| **Overflow Condition**      | When rear exceeds the size of the queue. | When rear + 1 is equal to the front (full condition). | When both front and rear pointers overlap. |
| **Underflow Condition**     | When front exceeds rear (empty).  | When front equals rear (empty). | When both front and rear pointers are invalid. |
| **Memory Usage**            | Fixed size (static or dynamic).   | Fixed size but makes better use of space. | Dynamic memory usage. |
| **Applications**            | Basic queue operations.           | Used in buffering and circular buffers. | Used in problems requiring insertion and deletion from both ends (e.g., sliding window problems). |

---
---
---
# Comparison of Sequential Search and Binary Search
| Feature                          | Sequential Search                                                                        | Binary Search                                                                                                       |
| -------------------------------- | ---------------------------------------------------------------------------------------- | ------------------------------------------------------------------------------------------------------------------- |
| **Definition**                   | A linear search algorithm that checks each element one by one until the target is found. | A divide-and-conquer search algorithm that repeatedly divides the search interval in half, requiring a sorted list. |
| **Data Requirement**             | No sorting required.                                                                     | Requires a sorted array.                                                                                            |
| **Search Method**                | Checks elements one by one.                                                              | Divides the search space in half each time.                                                                         |
| **Time Complexity (Best Case)**  | O(1) (If the element is found at the first position).                                    | O(1) (If the target is the middle element).                                                                         |
| **Time Complexity (Worst Case)** | O(n) (If the element is at the last position or not found).                              | O(log n) (If the element is at the extreme ends or not found).                                                      |
| **Space Complexity**             | O(1) (Constant space).                                                                   | O(1) (Constant space).                                                                                              |
| **Efficiency**                   | Less efficient for large lists.                                                          | More efficient for large lists.                                                                                     |
| **Use Cases**                    | Suitable for unsorted data or small lists.                                               | Efficient for searching in large sorted datasets.                                                                   |
| **Comparison Operations**        | O(n)                                                                                     | O(log n)                                                                                                            |
| **Example**                     | Searching for an element in an unsorted list. | Searching for an element in a sorted list. |

---
---
---
# Comparison of Stack and Queue
| Feature                        | Stack                           | Queue                           |
|---------------------------------|---------------------------------|---------------------------------|
| **Definition**                  | A linear data structure that follows the Last In First Out (LIFO) principle. | A linear data structure that follows the First In First Out (FIFO) principle. |
| **Direction of Operation**      | Elements are added and removed from the same end, called the top. | Elements are added at the rear and removed from the front. |
| **Insertion**                   | Push operation (adds element to the top). | Enqueue operation (adds element to the rear). |
| **Deletion**                    | Pop operation (removes element from the top). | Dequeue operation (removes element from the front). |
| **Access to Elements**          | Only the top element can be accessed. | Only the front element can be accessed. |
| **Overflow Condition**          | When the stack is full (in case of fixed-size stack). | When the queue is full (in case of fixed-size queue). |
| **Underflow Condition**         | When the stack is empty.        | When the queue is empty.        |
| **Time Complexity (Insert/Remove)** | O(1)                             | O(1)                             |
| **Applications**                | Function calls, undo operations, expression evaluation, etc. | Task scheduling, buffering, data transfer, etc. |
| **Example**                     | A stack of plates or books.     | A line of people waiting for a ticket. |

---
---
---
# Infix to Prefix Conversion with Examples
To convert an infix expression to a prefix expression, follow these steps:
1. **Reverse** the given infix expression.
2. **Replace** parentheses. Convert opening parentheses `(` to closing parentheses `)` and vice versa.
3. **Apply** the infix to postfix conversion on the reversed expression.
4. **Reverse** the resultant postfix expression to get the prefix expression.
### Example 1: 
Infix Expression: `(A + B) * (C - D)`
#### Step 1: Reverse the expression.
Reversed Infix Expression: `)D - C( * )B + A(`
#### Step 2: Replace parentheses.
Replaced Expression: `(D - C) * (B + A)`
#### Step 3: Apply infix to postfix conversion.
Postfix Expression: `DC-BA+*`
#### Step 4: Reverse the postfix expression.
Prefix Expression: `*+AB-CD`
### Final Result:
The prefix expression for `(A + B) * (C - D)` is `*+AB-CD`.
### Example 2: 
Infix Expression: `A + B * C`
#### Step 1: Reverse the expression.
Reversed Infix Expression: `C * B + A`
#### Step 2: Replace parentheses.
There are no parentheses, so this step is skipped.
#### Step 3: Apply infix to postfix conversion.
Postfix Expression: `ABC*+`
#### Step 4: Reverse the postfix expression.
Prefix Expression: `+A*BC`
### Final Result:
The prefix expression for `A + B * C` is `+A*BC`.
### Example 3:
Infix Expression: `(A + B) * (C + D)`
#### Step 1: Reverse the expression.
Reversed Infix Expression: `)D + C( * )B + A(`p 2: Replace parentheses.
Replaced Expression: `(D + C) * (B + A)`
#### Step 3: Apply infix to postfix conversion.
Postfix Expression: `DC+BA+*`
#### Step 4: Reverse the postfix expression.
Prefix Expression: `*+AB+CD`
### Final Result:
The prefix expression for `(A + B) * (C + D)` is `*+AB+CD`.

---
---
---

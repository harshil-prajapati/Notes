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


# Tree Traversal Methods  
Tree traversal refers to visiting all nodes of a tree systematically. The main methods are:  
### Example:  
**Tree Structure**  
  1  
 / \  
2   3  
/     \
4    5
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


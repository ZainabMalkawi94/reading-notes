## Stacks and Queues
Cheat Sheet: Stacks and Queues

---
### Stacks:
- A stack is a linear data structure that follows the Last-In-First-Out (LIFO) principle.
- Elements are added and removed from only one end of the stack, known as the top.
- WHY: Stacks are useful in situations where the order of data processing is important and needs to be reversed.

### Operations on a stack:
- Push: Adds an element to the top of the stack.
- Pop: Removes the top element from the stack.
- Peek: Returns the top element without removing it.
- isEmpty: Checks if the stack is empty.
- Size: Returns the number of elements in the stack.

### Implementation of a stack:
- Stacks can be implemented using arrays or linked lists.
- Arrays provide efficient memory allocation but have a fixed size.
- Linked lists allow dynamic memory allocation but have a slightly higher overhead.
---
### Queues:
- A queue is a linear data structure that follows the First-In-First-Out (FIFO) principle.
- Elements are added to the rear end of the queue and removed from the front end.
- WHY: Queues are useful in scenarios where the order of data processing needs to be maintained, similar to waiting in a queue.

### Operations on a queue:
- Enqueue: Adds an element to the rear end of the queue.
- Dequeue: Removes the front element from the queue.
- Front: Returns the front element without removing it.
- Rear: Returns the rear element without removing it.
- isEmpty: Checks if the queue is empty.
- Size: Returns the number of elements in the queue.

### Implementation of a queue:
- Queues can be implemented using arrays or linked lists.
- Circular arrays are often used to efficiently utilize memory and avoid shifting elements.
- Linked lists provide dynamic memory allocation but have a slightly higher overhead.
---
### Cheat Sheet Summary:
- Stacks follow the Last-In-First-Out (LIFO) or Fisrt-In-Last-out (FILO) principle, while queues follow the First-In-First-Out (FIFO) principle.
- Stacks are useful for reversing the order of data processing, while queues maintain the order.
- Stacks and queues can be implemented using arrays or linked lists.
- Arrays provide efficient memory allocation but have a fixed size, while linked lists allow dynamic memory allocation.

[Diagram]
Below is a visualization of the implementation of stacks and queues using linked lists:

Stack:
------
| 4  |
|----|
| 3  |
|----|
| 2  |
|----|
| 1  |
------

Queue:
------ Rear
| 1  |
|----|
| 2  |
|----|
| 3  |
|----|
| 4  |
------ Front

[Quiz]
1. What is the main difference between stacks and queues?

   a. Stacks follow LIFO, queues follow FIFO.

   b.  Stacks follow FIFO, queues follow LIFO.

   c.  Stacks and queues have the same principle.

   d.  Stacks and queues are unrelated.

2. Which operation adds an element to the top of a stack?

   a.  Enqueue

   b.  Push

   c. Pop

   d. Dequeue

3. In a queue, which end is used to add elements?

   a. Front

   b. Rear

   c. Top

   d. Bottom

4. Which data structure can have a fixed size when implemented using arrays?

   a. Stack

   b. Queue

   c. Both stack and queue

   d. Neither stack nor queue

[Answers]
1. a. Stacks follow LIFO, queues follow FIFO.
2. b. Push
3. b. Rear
4. c. Both stack and queue

---
### The pseudo code for basic operations on stacks and queues using array:

### Stacks:

```
Stack:
- Initialize an empty stack: stack = []

Push(element):
- Add element to the top of the stack: stack.push(element)

Pop():
- Remove and return the top element from the stack: return stack.pop()

Peek():
- Return the top element without removing it: return stack[top]

isEmpty():
- Check if the stack is empty: return (length of stack == 0)

Size():
- Return the number of elements in the stack: return length of stack
```

### Queues:

```
Queue:
- Initialize an empty queue: queue = []

Enqueue(element):
- Add element to the rear of the queue: queue.enqueue(element)

Dequeue():
- Remove and return the front element from the queue: return queue.dequeue()

Front():
- Return the front element without removing it: return queue[front]

Rear():
- Return the rear element without removing it: return queue[rear]

isEmpty():
- Check if the queue is empty: return (length of queue == 0)

Size():
- Return the number of elements in the queue: return length of queue
```

Note: The pseudo code assumes that the stack and queue are implemented using arrays. If you are using a linked list implementation, the operations might differ slightly.


---
 ### The pseudo code for implementing stacks and queues using linked lists:

### Stacks:

```
Node:
- Define a class for the node with a value and a reference to the next node.

Stack:
- Initialize an empty stack: stack.top = null

Push(element):
- Create a new node with the given element: newNode = Node(element)
- Set the next reference of newNode to the current top node: newNode.next = stack.top
- Set the top reference of the stack to newNode: stack.top = newNode

Pop():
- If the stack is empty (stack.top is null), return an error or throw an exception.
- Store the value of the top node: value = stack.top.value
- Set the top reference to the next node: stack.top = stack.top.next
- Return the stored value

Peek():
- If the stack is empty, return an error or throw an exception.
- Return the value of the top node: return stack.top.value

isEmpty():
- Return true if stack.top is null, indicating an empty stack. Otherwise, return false.

Size():
- Initialize a counter variable to 0: count = 0
- Start from the top node and traverse the linked list until reaching the end.
- For each node encountered, increment the counter by 1.
- Return the final count as the size of the stack.
```

### Queues:

```
Node:
- Define a class for the node with a value and a reference to the next node.

Queue:
- Initialize an empty queue: queue.front = null, queue.rear = null

Enqueue(element):
- Create a new node with the given element: newNode = Node(element)
- If the queue is empty (queue.front is null), set both front and rear references to newNode.
- Otherwise, set the next reference of the current rear node to newNode and update the rear reference to newNode.

Dequeue():
- If the queue is empty (queue.front is null), return an error or throw an exception.
- Store the value of the front node: value = queue.front.value
- Set the front reference to the next node: queue.front = queue.front.next
- If the front reference is now null, update the rear reference to null as well.
- Return the stored value

Front():
- If the queue is empty, return an error or throw an exception.
- Return the value of the front node: return queue.front.value

Rear():
- If the queue is empty, return an error or throw an exception.
- Return the value of the rear node: return queue.rear.value

isEmpty():
- Return true if both queue.front and queue.rear are null, indicating an empty queue. Otherwise, return false.

Size():
- Initialize a counter variable to 0: count = 0
- Start from the front node and traverse the linked list until reaching the end.
- For each node encountered, increment the counter by 1.
- Return the final count as the size of the queue.
```

Please note that the pseudo code provided assumes the existence of basic linked list operations such as creating nodes and updating next references.

---
### The implementation of stacks and queues using linked lists in JavaScript:

```javascript
class Node {
  constructor(value) {
    this.value = value;
    this.next = null;
  }
}

class Stack {
  constructor() {
    this.top = null;
  }

  push(element) {
    const newNode = new Node(element);
    newNode.next = this.top;
    this.top = newNode;
  }

  pop() {
    if (this.isEmpty()) {
      throw new Error("Stack is empty");
    }
    const value = this.top.value;
    this.top = this.top.next;
    return value;
  }

  peek() {
    if (this.isEmpty()) {
      throw new Error("Stack is empty");
    }
    return this.top.value;
  }

  isEmpty() {
    return this.top === null;
  }

  size() {
    let count = 0;
    let current = this.top;
    while (current) {
      count++;
      current = current.next;
    }
    return count;
  }
}

class Queue {
  constructor() {
    this.front = null;
    this.rear = null;
  }

  enqueue(element) {
    const newNode = new Node(element);
    if (this.isEmpty()) {
      this.front = newNode;
      this.rear = newNode;
    } else {
      this.rear.next = newNode;
      this.rear = newNode;
    }
  }

  dequeue() {
    if (this.isEmpty()) {
      throw new Error("Queue is empty");
    }
    const value = this.front.value;
    this.front = this.front.next;
    if (this.front === null) {
      this.rear = null;
    }
    return value;
  }

  front() {
    if (this.isEmpty()) {
      throw new Error("Queue is empty");
    }
    return this.front.value;
  }

  rear() {
    if (this.isEmpty()) {
      throw new Error("Queue is empty");
    }
    return this.rear.value;
  }

  isEmpty() {
    return this.front === null && this.rear === null;
  }

  size() {
    let count = 0;
    let current = this.front;
    while (current) {
      count++;
      current = current.next;
    }
    return count;
  }
}

// Example usage
const stack = new Stack();
stack.push(1);
stack.push(2);
stack.push(3);
console.log(stack.pop()); // Output: 3
console.log(stack.peek()); // Output: 2
console.log(stack.isEmpty()); // Output: false
console.log(stack.size()); // Output: 2

const queue = new Queue();
queue.enqueue(1);
queue.enqueue(2);
queue.enqueue(3);
console.log(queue.dequeue()); // Output: 1
console.log(queue.front()); // Output: 2
console.log(queue.rear()); // Output: 3
console.log(queue.isEmpty()); // Output: false
console.log(queue.size()); // Output: 2
```

In the above code, we define a `Node` class to represent each node in the linked list. Then, we define the `Stack` and `Queue` classes that use linked lists for their implementation.

The methods for each class are implemented according to the pseudo code provided earlier. The stack uses the `top` reference to keep track of the topmost node, and the queue uses the `front` and `rear` references to maintain the front and rear nodes, respectively.

-------------------------------------------------------------------------------------------------------------
return to [Main Reading File](./README.md)
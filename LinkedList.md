# Linked Lists - An Overview
## Introduction:
Linked lists are a fundamental data structure used in computer science and programming. They provide a dynamic way to store and organize data. In this teaching, we will explore the basics of linked lists, including what they are, how they work, and their advantages and disadvantages compared to other data structures.

## What is a Linked List?
A linked list is a linear data structure consisting of nodes, where each node contains a value and a reference to the next node in the sequence. Unlike arrays, linked lists do not require contiguous memory allocation. Instead, each node is dynamically allocated and connected through pointers or references.

## Anatomy of a Linked List:
1. Node: A node is an individual element or unit of data in a linked list. It consists of two components:

    - Data: The value or payload stored in the node.
    - Next: A reference or pointer that points to the next node in the list.
2. Head: The head is the first node in a linked list. It serves as the entry point to access the list.

3. Tail: The tail is the last node in a linked list. Its "next" reference is typically set to null or a sentinel value to indicate the end of the list.

## Types of Linked Lists:
1.  Singly Linked List: Each node points to the next node in the sequence.
2.  Doubly Linked List: Each node has references to both the next and previous nodes.
3.  Circular Linked List: The last node points back to the first node, forming a loop.

## Operations on Linked Lists:
1.  Insertion:
- Insertion at the beginning: Create a new node, update the "next" reference to the current head, and set the new node as the head.
- Insertion at the end: Traverse the list until reaching the last node, then create a new node and update the "next" reference of the last node.
- Insertion in the middle: Locate the desired position, create a new node, update the "next" references to connect the new node.

2.  Deletion:
- Deletion at the beginning: Update the head to the next node, and free the memory of the removed node.
- Deletion at the end: Traverse the list until reaching the second-to-last node, update its "next" reference to null or a sentinel value, and free the memory of the removed node.
- Deletion in the middle: Locate the node to be deleted, update the "next" reference of the previous node to skip the node to be deleted, and free its memory.
3.  Searching: 

    Traverse the linked list, comparing the data of each node with the target value until a match is found or the end of the list is reached.

4.  Traversal: 

    Visit each node in the linked list, usually from the head to the tail, and perform desired operations.
## Advantages of Linked Lists:

1. Dynamic Size: Linked lists can grow or shrink dynamically during program execution, making them suitable for scenarios where the size of the data may change.

2. Efficient Insertion and Deletion: Insertion and deletion operations can be performed in constant time complexity (O(1)) at the beginning or end of the linked list, given the appropriate references.

##  Disadvantages of Linked Lists:

1. Sequential Access: Unlike arrays, linked lists do not provide direct access to arbitrary elements. To access an element, the list must be traversed sequentially from the head node.

2. Additional Memory: Linked lists require extra memory to store the references or pointers, increasing the overall memory overhead compared to arrays.

## Diagram/Visualization:
![Linked List](https://miro.medium.com/v2/resize:fit:1200/0*0XVK02Guco9xJMJL.png)

## How linked lists can be used in real-life applications
Linked lists have various real-life applications and are commonly used in computer science and software development. Some of the areas where linked lists are utilized include:

1. Implementing Data Structures: Linked lists serve as fundamental building blocks for implementing more complex data structures such as stacks, queues, graphs, and hash tables.

2. File Systems: File systems often use linked lists to manage the blocks of data on storage devices. Each block contains a reference to the next block, allowing efficient traversal and allocation of disk space.

3. Music and Video Playlists: Linked lists are frequently used to represent playlists in music and video players. Each node contains information about the media item and a reference to the next item in the playlist.

4. Undo/Redo Functionality: Applications that require undo/redo functionality can utilize linked lists to maintain a sequence of actions. Each node in the list represents an action, and the list allows efficient navigation and reversal of actions.

5. Browser History: Web browsers store the browsing history using a linked list structure. Each page visited is represented by a node, allowing users to navigate back and forth through the visited pages.

6. Polynomial Representation: In mathematics and computer science, linked lists can be used to represent polynomials efficiently. Each node contains the coefficient and exponent of a term in the polynomial.

7. Job Scheduling: Linked lists can be used to implement job scheduling algorithms. Each job can be represented as a node, and the list allows efficient insertion and removal of jobs based on priority or scheduling criteria.

8. Symbol Table in Compilers: Compilers use symbol tables to store information about variables, functions, and other program entities. Linked lists can be employed to implement symbol tables efficiently.


## Example Quiz:

1. What is a linked list?

    1. A data structure with contiguous memory allocation
    2.  A data structure consisting of nodes with references to other nodes
    3. A data structure for binary search operations

2. Which type of linked list allows traversal in both directions?
    1.  Singly linked list
    2.  Doubly linked list
    3.  Circular linked list

3. How can you insert a new node at the beginning of a linked list?
    1.  Update the "next" reference of the last node
    2.  Update the head and set the new node as the head
    3.  Locate the desired position and connect the new node

4. What is the time complexity of insertion and deletion operations at the beginning or end of a linked list?
   1.  O(1)
    2.  O(n)
    3. O(log n)

5. What is one disadvantage of linked lists compared to arrays?
1.  Linked lists provide direct access to arbitrary elements.
2.  Linked lists require contiguous memory allocation.
3.  Linked lists have slower insertion and deletion operations.

        (Note: Answers: 1 - 2, 2 - 2, 3 - 2, 4 - 1, 5 - 3)

---
return to [Main Reading File](./README.md)
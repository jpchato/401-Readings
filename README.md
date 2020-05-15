# 401-Readings
## Linked Lists
* A linked list is a sequence of nodes that are connected to each other. Each node references the next node in the list.
* Two types of linked lists: singly and doubly
  * Singly refers to the number of references the node has. The reference points to the next node in the list.
  * Doubly refers to two references within the node. Reference to previous and next node. 
 * Nodes are individual items that live in a linked list. Nodes contain the data for each link.
 * Next allows us to traverse linked lists. Not able to use foreach or for loop. 
 * while() is the best way to traverse a linked list.
 * set the current to the head to start form the beginning of a linked list
 * Big O of time for using includes is O(n), for space it's O(1)
 * To add a node set the current equal to head. newNode.next is then set to head.
 * use print() to print out the nodes
 
## What’s a Linked List, Anyway? [Part 1]
* We use data structures to organize our data. Variables, arrays, and objects are all types of data structures
* Linked lists are linear data structures(hop-scotch). Needs to be traversed sequentially in order. Order matters@!
* Memory management is a big difference between arrays and linked lists. 
* Memory allocation for linked lists can be scattered. Contrary to arrays which need a contiguous allocation of memory. 
* Linked lists are dynamic data strucutres. Contrary to arrays which are static data structures. 
* Linked lists are made up of nodes. The starting point of a linked list is refered to as the head. The final node isn't a node exactly, but a node that points to a null value. 
* Nodes have two parts: data and a reference to the next node. 
* Singly linked lists have a single track we can traverse it with. Can only go from head node to final (null) node
* Doubly linked lists refer to previous and next nodes. 
* Circular linked list does not end with a node pointing to a null value. 
 * useful for adding things to the list
 

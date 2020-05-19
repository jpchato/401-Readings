# 401-Readings

## Python Scope - Global and Local Keywords
* Global scope - Variables available to all the code
* Local scope - Variables only available within a code block
* If you can access a variable it is `in scope` if you can't it is `out of scope`
* global statement
  * defines a list of names that are going to be treated as global names
  * Generally speaking, bad practive to use the global statement
* nonlocal statement
  * defines a list of names that are going to be treated as nonlocal
* Scope defines visibility throughout code

## Don't be CONFUSED by BIG O notation anymore!
* A measure of how long an algorithm takes to do something. 
* Time complexity-time reqired
* Space complexity-space required
* A way of measuring how an algorithm will respond to an increasing amount of data that it will have to process
* Big O notation will usually give you the worst case scenario
  * You don't want to know the best case scenario
* Different levels of complexity
* O(1) - constant running time
* O(log n) - logarithmic running time
* O(n) - linear running time
* O(n logn) - Log-linear running time
* O(n^k) - Polynomial running time


## How to Use Random Module
* The random module provides access to functions that support various operations, including the generation of random numbers
* randinit generates a random integer based on two parameters: a low and a high number
* To generate a larger number, multiply it
* random.choice([x, y, z]) generates a random value from a sequence
* random.shuffle() shuffles elements in a list
* random.randrange(start, stop[, step]) generates a random element from the range
* [Reference!](https://www.pythonforbeginners.com/random/how-to-use-the-random-module-in-python)

## What is Dependency Injection
* Transferring the task of creating the object to something else and directly using the dependency
* DI can be thought of as the middle man. Dependencies can be injected at run time as opposed to compile time
* 3 Types of Dependency Injection:
 1. constructor injection - dependencies provided through a class constructor
 1. setter injection - setter method that the injector uses to set the dependency
 1. interface injection - ??? 
* Classes should concentrate on fulfilling their responsibilities, not on creating objects required to meet those responsibilities.
* DI Benefits
 * Helps unit testing
 * Reduces boiler plate coede
 * Extending the app becomes easier
 * enables loose coupling (idk what this means)
* DI Flaws
 * Complex to learn and can cause problems if overused
 * Compile errors become run time errors
* [Reference!](https://www.freecodecamp.org/news/a-quick-intro-to-dependency-injection-what-it-is-and-when-to-use-it-7578c84fa88f/)

## Big O Notation
* Pigeon is constant time O(1) :smile:
* Constant time beats linear if sufficiently large
* Big O describes how the run time scales with input variables
* 4 Big O Rules
 1. Different steps get added
 1. Drop constants
 1. Different inputs require different variables to represent them
 1. Drop non-dominant terms
* [Reference!](https://www.youtube.com/watch?v=v4cd1O4zkGw)


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
 
## What’s a Linked List, Anyway? [Part 2]
* Big O notation is a way of evaluating the performance of an algorithm
 * How much time it requires at runtime and how much space it needs
* O(1)
 * Constant time. Always takes the same amount of memory and time to process
* O(n)
 * Linear. As our output grows, our space/time requirements also grow linearly.
* O(n^2)
 * Exponential. Avoid. As our output grows, our space/time requirements grow exponentially.
* Rearrange our pointers to grow a linked list. 
* a linked list is usefulfor adding and removing  elements, but is slow for searching and finding elements.

# 401-Readings

## How to Web Scrape with Python
* automatically access and extract a large amount of data from a website
* Important notes
     * most websites prevent the use of their data for commercial purposes
     * don't download too much -- you might crash the website
* need to be familiar with html for web scraping to work
     * identify where in the html the files you want are located
## Web Scraping Wiki
* extracting data from websites
* legal issues
* some websites prevent web scraping, so sophisticated bots are developed to counter the counter-measures


## Data visualization
### Matplot lib
* Mostused python library for 2d graphics
* simple plots, figures, subplots, axes, and ticks
* animation
* regular plot, scatter plot, bar plot, contour plot, imshow, quiver plot, piechart, grid, multiplot, polar axis, 3d plots, text

### Bokeh
* Interactive visualization library that targets modern web browsers
* 




## Trees
### Common Terminology
* Node - individual item/data that makes up data structure
* root- first/top node in tree
* left child - node positioned to the left of a root/node
* right child - node positioned to the right of a root/node
* edge - link between parent and child node
* leaf - node that does not contain children
* height - determined by number of edges from root to bottommost node
### Traversals 
* Traversing trees allows us to search for a node, and do things with the node
* Two types of traversals:
      * depth first
      * Breadth first
 #### Depth First
 * Prioritizes going through the depth/height of the tree first.
 * Multiple ways to carry out the traversal. Each method chnages the order i nwhich the root is searched/printed
      * Three methods for traversal
            * pre-order: root --> left ---> right
            * in-order: left --> root --> right
            * post-order: left --> right --> root
            
  ### Breadth First
  * Goes through each level of the tree node-by-node
  * Uses a queue to traverse the width/breadth of the tree
  
  ## Binary Trees
  * Binary trees restrict the number of children to two
  
  ### Adding a Node
  * It doesn't matter where new nodes get placed in a binary tree because there are no structural rules for where nodes are supposed to go
  * Fill child spots from top --> down utilizing breadth first traversal
  
  ### Big O
  * Time complexity for inserting a new node is O(n)
  * Searching for a specific node is O(n)
  * Worst case scenario is O(n) 
  * Space complexity for node instertion is O(W) where is the largest width of the tree. 
  
  ## Binary Search Trees
  * Structured tree where all values smaller than the root are placed to the left and values larger than the root are to the right
  * Best way to approach bst is whit a while loop
  
  ### Big O
  * O(h) where h is the height of the tree - time complexity
  * O(1) - space complexity
 
 


## Linear Regressions
* Import required libraries into python notebook
* Convert data into dataframe using pandas
* LinearRegression.
* Regression searches for relationship among variables
* Used when you need to determine if one variable influences another
* R^2 --- strong relationship\
* scikit-learn and statsmodels needed to implement linear regression
* DO IT:
    * Import the packages and classes you need
    * Provide data to work with and eventually do appropriate transformations
    * Create a regression model and fit it with existing data
    * Check the results of model fitting to know whether the model is satisfactory
    * Apply the model for predictions

## Pandas
* Database management tool??
* Object Creation
* Viewing Data
* Selection
   * Getting
   * Selection by label
   * Selection by position
   * Boolean indexing
   * setting
 * Missing Data
 * Operations
   * Stats
   * Apply
   * Histogramming
   * String Methods
 * Merge
   * Concat
   * Join
 * Grouping
 * Reshaping
   * Stack
   * Pivot Tables
 * Time Series
 * Categoricals
 * Plotting
 * Getting Data In/Out
   * CSV
   * HDF5
   * Excel
 
 * At a glance, seems very reminiscent of JMP
   

## Data Science in a Nutshell
* Attempting to make sense of data by identifying patterns and applying algorithms 
* Unstructured data - Does not have a predefined data model
* Structured data - mostly available in text formats from databases
* Data analytics - processing data
* raw data --> data visualization
 * --> Human decision
 * --> machine learning - identifying patterns in data
 * --> AI - machine makes decisions on its own
 
 ## Jupyterlab
 * Work with data and code together
 * Video goes into markdown syntax
 * $ to create equations
 * Allows the arranging of multiple different documents and activities in the same program
 
 ## NumPy
 * Data Analysis Package
 * 



## Stacks and Queues
* A stack is a data structure that consists of nodes. Each node references the next node in the stack but not the previosu (like a linked list???)
* Terminology
  * Push - nodes/items pushed to stack
  * Pop - When you remove an item from the stack it is being popped. You cannot remove items from an empty stack because (an exception will be raised).
  * Top - top of stack
  * Peek - peeking will show the value from the top of the stack. Cannot peek an empty stack(exception will be raised)
  * isEmpty - returns true when stack is empty
* FILO - first in last out
* LIFO - last in first out
* Pushing a node into a stack is an O(1) operation
* use isEmpty before doing a pop
* use isEmpty before conducting a peek
* Queue terminology
  * enqueue - nodes or items that are added to the queue
  * dequeue - nodes/items removed from queue
  * front - front/first node of queue
  * rear - rear/last node of queue
  * peek - shows value of front of queue
  * isEmpty - returns true when queue is empty
* FIFO - first in first out - first item in queue will be first out
  * opposite of stack
* LILO - last in last out - last item in queue will be last out
  * opposite of stack
* 


## Statistics in Python
* Probability - "What is the chance of an event happening?"
  * An event is defined as an outcome of interest
* sample space - the set of all possible events that can happen
  * an example would be a coin flip where it can land on heads or tails
* normal distribution refers to a phenomenon in tprobability and statistics with a unique symmetry and shape
* Central Limit Theorem
  * Peak of normal distribution lines up with the mean
* Three Sigma Rule
  * How many observations fall within a certain distance of the mean
  * 68% of your observations will fall within 1 stdev of the mean
  * rarity of extreme values
* Z-score
  * How many stdev from the mean for a given data point?
  * When compared against it a z-table it provides cumulative probability
    * cumulative probability - the sum of the probabilities of all values occurring, up until a given point
    
## Intro to Statistics Video
* Statistical features like bias, variance, and many others help us explore a dataset to gain valuable insights
* Probability distributions define the percent chance that some event will occur, and we can use them to understand the spread of data
* Bayesian statistics expresses probability as a degree of belief in an event which can change as new information is gathered rather than a fixed values based on frequency
  

## List Comprehensions
* A concise way to create lists
* List comprehension always returns a list
* `new_list = [expression(i) for i in old_list if filter(i)]`
* Create a new list from a list you iterate through

## Primer on Generators
* a function that takes another function and extends the behavior of the latter function without explicitly modifying it.
* Functions are first-class arguments in python --- that means functions can be passed around and used as arguments
* Functions defind in other functions are called in inner functions

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

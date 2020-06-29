# 401-Readings

# DSA Review
* Communicate
 * Restate the question
 * ask about edge cases
 * ask about test cases
 * write pseudocode and ask if it makes sense
 * write the actual code and ask if it looks good
 * ask for help if stuck
* 7 tips
 1. take a few minutes to think through the problem without talking
  * don't force yourself to fill the silence immediately, think through it but communicate why you're silent
 2. write down the steps of the solution
  * write down general steps of how you will solve the problem
 3. write pseudocode first
  * write the pseudocode before the actual code
 4. don't sweat the small stuff
  * don't sweat syntax, big picture is more important here - problem solving, communiation, humanity
 5. sit down be humble
  * accept criticism gracefully
 6. come prepared
  * practice practice practice
 7. review your work
  * algorithmic efficency
  * correctness

# Graphs
* graph is a non-linear data structure that is a collection of vertices(nodes) connected by line segments called edges
* vertex- a data object tha can have zero or more adjacent vertices, also called a node
* an edge is a connection between two nodes
* the neighbors of a node are its adjacent nodes(connected via an edge)
* the degree of a vertex is the number edges connected to that vertex
* an undirected graph is a graph where each edge is undirectional or bidirectional. This means the undirected graph does not move in any direction
* a directed graph(digraph) is a graph where ever edge is directed. Each node is directed at another node with a specific requriement of what node should be referenced next
* a complete graph is when all nodes are connected to other nodes
* a connected graph is when all vertices have at least one edge
* a disconnected graph(DAG) is where some vertices may not have edges
* an acyclic graph is a directed graph without cycles. A cycle is when a node can be traversed through and potentially end up back at itself
* cyclic graphs are graphs that have cycles. A cycle is a path of a positive length that starts and ends at the same vertix
* graphs are represented through adjacency matrix and adjacency list
* an adjacency matrix is represented through a 2-d array
* adjacency list - most common way to represent graphs. A collection of linked lists or array that lists all of the other vertices that are connected
* weighted graphs - numbers assigned to its edges. the numbers are called weights
* 

## SSH Tutorial
* remote administration protocol that allows users to control and modify their remote servers over the Internet
* Secure Shell
* Symmetric encryption is a form of encryption where a secret key is used for both encryption and decryption of a message by both the client and the host
* asymmetrical encryption uses two separate keys for encryption and decryption
* hashing generates a unique value of a fixed length for each input that shows no clear trend which can exploited which makes it impossible to reverse
* SSH works by making use of a client-server model to allow for authentication of two remote systems and encryption of the data that passes between them

## Django Configurations
* Keep settings in environment variables
* Write default values for production configuration (excluding secret keys and tokens)
* Don’t hardcode sensitive settings, and don’t put them in VCS
* Split settings into groups: Django, third-party, project
* Follow naming conventions for custom (project) settings

## JSON Web Tokens and DRF JWT
* JWT - JSON web token is a compact and self-contained way for transmitting information The information can be verified and trusted because it is digitally signed
* jwt should be used for authorization and information exchange
* jwt format -  `xxx.yyy.zzz` - header.payload.signature
* jst has an access and a refresh token
* the access token is short-lived and the refresh token last about 24 hours
* They are received when correct username and pw are supplied
* `poetry add djangorestframework_simplejwt`
* update urls.py with 
  * '''
   from django.urls import path
from rest_framework_simplejwt import views as jwt_views

urlpatterns = [
    path('api/token/', jwt_views.TokenObtainPairView.as_view(), name='token_obtain_pair'),
    path('api/token/refresh/', jwt_views.TokenRefreshView.as_view(), name='token_refresh'),
]
'''
* the refresh token is necesary to ensure the user still has the correct permissions
* 

## Permissions
* permissions determine whether a request should be granted or denied access
* permission checks are run at the start of the view before other code has proceeded
* permissions grant or deny access for different classes of users to different parts of the api
* permission policy is in settings under `REST_FRAMEWORK`
* 


## Docker
* A way to isolate and run entire applications
* No need for virtual environments with docker
* Docker is a way to implement linux containers which are a type of virtualization
* python venvs are limited compared to docker containres
* dockerfile is a list of instructions for creating an image
* images are made up of one or more layers
* containers are a running instance of an image

## Django APIs
* Django REST Framework works alongside Django web framework to create web APIs
* Added after django has been installed and configured
* Djnago creates websites containing webpages while Django REST Framework creates web APIs which are a collection of URL endpoints containing available HTTP verbs that return JSON
* django rest frame work added to INSTALLED_APPS as `'rest_framework'` after `poetry add djangorestframeowrk==3.11.0`
* 

## Hash Table
* Two main components: key and value
* Used to store data
* Way to implement an associative array
* Hash function takes a key value and output is an index number
* Create a linked list off of index values if a key has shares an index
* hash- a hash is the result of some algorithm taking an incoming string and converting it int oa value that could be used for either security or some other purpose. In the case of a hashtable, it is used to determine the index of the array.
* buckets - a bucket is what is contained in each index of the array of the hashtable. Each index is a bucket. An idnexcould potentially contain multiple key/value pairs if a collision occurs
* collisions - a collision is what happens when more than one key gets hashed to the same location of the hashtable

## Django Custom User Model
* Always use a custom user model for new django projects
* create a directory for users
* DO NOT MIGRATE, YET
* in settings.py create a new CustomUser model
* create new UserCreation and UserChangeForm
* Custom user model allows you to add aditional fields at any time

## Django Forms
* Collect information from a user for submission to a server
* flexible tool for collecting info from user because it can collect diferent types of data
* relatively secure way of sharing data with server because it sends data in a `POST` request with cross-site forgery protection
* django provides a framework that lets you define fields programatically 
* 



## Django: Using Models
* database models
* Django allows you to define relationships that are one to one (OneToOneField), one to many (ForeignKey) and many to many (ManyToManyField).
* defined in modelys.py file
* example of a field `my_field_name = models.CharField(max_length=20, help_text='Enter field documentation')`
  * A model can have any amount of fields, of any type — each field represents a column we want to store in our database 
* In every model the method __str__() should be defined 

## Django Admin
* Admin application allows you to update parts of website using models (CRUD)
* Create a superuser `python3 manage.py createsuperuser`
* log in using the admin url `/admin URL (e.g. http://127.0.0.1:8000/admin)`
* CRUD access in Django GUI
* Add new column to website with add, update fields as necessary
* Instances of an item are unique from the main category but are based on the main category.


## Getting Started with Django
* Object-relational mapper
   * Write data models in Python, or use SQL if needed
* URLs and Views
   * import path to create url paths for web page
* Templates
   * Can template like we did in JS. That is write code directly into an HTML file
* Forms
   * validate user data and convert it to Python types
* Authentication 
   * Users can create accounts to safely log in and out
* Admin
   * Helps manage content on site for developers
* Internationalization
   * Translate!!
* Security 
 * Provides protection against clickjacking, cross-site scripting,cross site request forgery (CSRF), SQL injection, remote code execution

## How Django Works Behind the Scenes
* Python based web-framework
* open-source
* DSF supports and maintains Django - Django Software Foundation

## Python RegEx
* Identify if a pattern exists in a given set of characters
* Help manipulate textual data
* Import re at top of python page to use regex library
* When a special character matches as much of the search string as possible, it is said to be a "Greedy Match"
* non-greedy matches as little text as possible
* The jist of it - helps you find chunks of code that you might want to filter out???

## shutil - High Level File Operations
* copy files
* copy file metadata
* work with tree directories
* find files
* archives
* file system space

## Caesar Cipher
* simple and widely known encryption technique
* letter is shifted 3 to the left
    * a --> x
* deciphering is done in reverse with a right shift of 3
    * x --> a
    
## Cryptography Video
* defense in depth
    * various layers of defense
* cryptography
* secret writing
* cipher - an algorithm that turns plain text into cipher text
* encryption and decryption
* Caesar cipher is an example of substituion cipher which replaces every letter ina message wtih something else according to a translation
* permutation ciphers - grid transformation
* enigma - substitution cipher used by nazis
* data encryption standard - binary keys
* advanced encryption standard - makes brute force attacks harder
    * balances performance and security
* key exchange
    * an algorithm that lets two computers agree on a key without sending one
    * mixed paints example
* diffie helman key exchange
    * base and modulus are public values
    * public key lets you encrypt, not decrypt
* rsa

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

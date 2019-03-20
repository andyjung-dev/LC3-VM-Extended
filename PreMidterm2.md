
## Arrays and Lists
Arrays have O(1) access

List methods:
* `get(i)` - Returns the i-th element (but doesn't remove it)
* `set(i,e)` - Replaces the i-th element with e
* `add(i,e)` - Inserts element e into the i-th position
* `remove(i)` - Removes the i-th element from list
* `remove(e)` - Removes first occurrence of element e from the list (if it exists)
* `clear()` - Empties the list
* `isEmpty()` - Returns true if empty, false if not empty
* `size()` - Returns number of elements in the list

### ArrayList
* Use an array to store the elements of the list
* Keep track of how many elements we have inserted in the list (internal field/property usually called size)
* When implementing ArrayList/others in Java, throw `IndexOutOfBoundsException()` for nonexistent index position
* `resize()` is a private method that resizes the array
* Java ArrayList resizes by 50% when array is full


### Linked List
* Composed of nodes, which have an element and a pointer to next node
* Singly Linked List has a head and tail
* What is the pseudocode for each operation?
* Doubly Linked List contains two references, `prev` and `next`
* Dummy nodes are placed at the head and tail to avoid cases of too small a size for the list
* Using get(i) on a linked list and looping over every element requires O(N^2) time

array lists uses the traditional `[]` syntax


|method|array list|Single Linked list|  Doubly Linked List
| :--: |:--------:|:---------:| :--:| 
|`addFirst()`|O(N)|O(1)| O(1)|
|`removeFirst()`|O(N)|O(1)|
|`addLast()`|O(1)*|O(1)
|`removeLast()`|O(1)|O(1)|
|`getLast()`|O(1)|O(N)|
*if the array is not full


Doubly linked list - cannot create dnodes unless inside the private class

Other list operations
* get(i)
* set(i,e)

dummy node implementation: what is it?  
dummy nodes don't count as elements inside the list
dummy nodes are used even if the list is not empty

in arraylist would have taken n^2  
O(N^2) -> there is a faster way to iterate through elements in a java linked list  

Space complexity:  
All three data structures use space O(N) for a list of size N
But linked lists 2x single or 3xdouble linked lists
Java uses a doubly linked list for linked list which includes:
* addFirst()
* removeFirst()
* addLast()
* removeLast()

## Interfaces , Generics, Iterable, and Iterator

#### Interfaces
`interface` in Java can be public or package-private

Inheritance is not covered for this course

For interface you can treat it as an object but place any clas that implements that interface in its stead  

When using a list, you can also use a class that implements that list such as `ArrayList` or `LinkedList`

#### Generics  
We use the syntax `<T>` to denote an object of type `T`  
When we instantiate this class, we can then specify the type of object to be used  
**How do you create a generic class?**  
* Replace the Object labels with some T in the class and in the header

What might cause a compile-time error when using generics?
* When

#### Iterable and Iterator
Essentially an enhanced for loop that iterates through a list of iterable elements  
What is the difference between iterable and iterator?  
`Iterable`  
contains an object of class/type `Iterator`  
`Iterator`  
implements two methods:  
`hasNext()`  
`next()`  

after traversing a collection, a new `Iterator` is needed because of the way that `hasNext()` and `next()` are implemented. Why?

Iterators iterate over nodes, not the objects  
Each instance of the iterator is separate  
Using an iterator can reduce (linear) traversal but limits knowledge of the index position 

## Quadratic Sorting a List
how to sort a list:
* selection O(N^2)
* bubble O(N^2)
* insertion O (N^2)
* heap sort
* merge sort 
* quick sort

How does each one operate?  
What are their strengths and wekanesses?  
What is their runtime?  
Which scenario prompts the usage of which one?  

## Stacks
How are they used in the Tower of Hanoi problem?  
Stacks in Palindrome verification  
Stacks in parenthesis matching  
## Queue 
What is the difference between queue and stack?
Runtime of queue operations?  
what are the different types of queue? (3 ADTs)  
Interface extension and what is a Deck  
## Induction  
What is indcution?  
What are some uses of induction  
How can we use induction to show O time  

Recursion vs iteration  

## Recursion and Binary Search  
Example: Decimal to Binary function, iterative vs recursion  

When I call a recursive function, how many times will it run?  

What is binary search?  
## Merge Sort and Quick Sort  
Time complexity (running time)   
Which algorithms have which complexities?  

how are they implemented?  


## Rooted Trees  
Rooted tree is a tree with a root  
How do you compute the depth of a node?  
How is a node implemented in Java

DFT
difference between pre order an dpost order trversal

visitng nodes - what doe i t mean?

## Trees II

Tree traversal

### Midterm Review
Queues vs Stacks
FIFO vs LIFO
A queue using stack? How would that work? Important to keep in mind


## CSUS Midterm 2 Review
Topics covered previously:  
* Programming conventions (Style)
* Binary numbers
* Aliasing
* Recursion vs. Iteration
* Strings 
* Regex
* Linked Lists
* Encapsulation and Polymorphism  

### Topics covered Midterm 2 (page 39/152):
* Stacks
* Queues
* Mathematical Induction
* Recursion
* Sort Functions/Algos
* Rooted Trees, Binary Trees and Tree Traversal
* Heaps

Also includes practice questions  

Some material will be cumulative, some topics might not be covered in the midterm (ie. regex)  

### Recap: Linked Lists
Know runtime (memorize)
How to implement operations (add,remove,insert at specific location)  
What is the dummy node used for (to avoid null)  

### What is an interface?
Essentially a template with protoype methods (like C) that are by default public and abstract 
Fields in an interface are by default public static and final  

### What is a Generic?

Generic type uses a placeholder term to denote an object that has not been initialized or specified 
Some conventional terms for generics:
* E - Element
* T - Type
* K - Key
* V - Value


### What is iterable and iterator

Iterable: some kind of iterable data structure and is also an interface  
Iterator: can be an interface but essentially contains methods that allow for iterating through a given object/data structure 

Note: Iterator should be implemented specifcially (since it is an interface)

Note: should not use primitive data types for Java `ArrayList`

**Using Iterator vs a for loop:**   
In a for loop using the get() function requires traversing through the list again and again (continuously) whereas a for each loop saves the list traversal position


### Stack 
What are the stack methods?  
* `empty()`
* `peek()`
* `pop()`
* `push()`  
Specific usage of stack in the following scenarios:
* Tower of Hanoi
* Palindrome Verification
* Parentheses Matching
* Recrusive Programs
* DFS  
Stack is a java class that provides built-in methods 

### Queue
How are queues implemented in an array?  
What are the queue methods/operations and their runtime complexity?  
* dequeue
* enqueue  
Queue is an interface: must be implemented completely depending on the data type/object  
Do we bound a queue? why?  
How do linked lists use dequeue?  


### Induction

How do you create an inductive proof?  
Weak induction: prove k, then k+1  
Strong induction: prove base, then k, then k+1  
How do you prove a function is recursive via induction?

### Recursion/Iteration
How do you find runtime complexity for a recursive function?  
Requires a base case (that is valid)  
Look at and go through the reverse list function  
No tail recursion

**Recursion vs Iteration:**  
* Iteration is easier and faster as recursion introduces complexity (and the runtime stack)
* Recursion can be elegant and simpler if the problem lends itself easily to it   

Know how to implement a recursive funciton in java or pseudocode
### Sorting Algorithms

**Bubble Sort**
* Uses two nested loops to do individual swaps for each element 

**Insertion Sort**  
* Uses two nested loops but splits into subsections
* know the pseudocode or java implementation
* Inserts a temporary value into a shifted position  

**Selection Sort**
* Uses two nested loops that separates between sorted and unsorted  
* Utilizes a delimiter to split the array
* Can use recursion   

Know difference between these algos  
What is the time complexity for these algos?    
Worst case: sorted in reverse order

### Binary Search, Time Complexity and Big O 
Binary Search: What is the algo?  
How to binary search recurisvely vs iteratively?  
What is time complexity for binary search?  
What is the time needed for primitive operations?  
How to find time complexity for a given algo?  

### Trees - Introduction
What is the terminology? (root, child, node, leaf, etc)

Rooted tree means there is a root node, the origin in one sense

What is the depth of a tree?  
The depth of the node is the length of the path from that particular node to the root

What is the height of a tree?  
The height of a node is the maximum length of a path from that node to a leaf  

A tree with n nodes has (n-1) edges  
A rooted tree with n nodes has n-1 edges
For n nodes there are n! unique traversals (post or in order)

For a binary tree the maximum number of nodes at any level is 2^n

Trees must be implemented manually in Java  
Non-recursive tree traversal can be done with a stack or queue (what is the pseudocode for it)?  
**Tree Traversal**  
* Pre Order: (root, left, right)
* In Order: (Left, Root, Right)
* Post Order: (Left, Right, Root)
* Breadth: visit the sibling nodes before the leaf/child nodes (can be done with queue) VISITS NODES LEVEL BY LEVEL (Level Order Traversal)
* Depth: Visit the leaf/child nodes before the parent/sibling nodes (can be done with stack)

### Merge Sort and Quick Sort 
Note: What is a divide and conquer algorithm?  
What is the runtime complexity of merge sort?  
What is the pseudocode/java implementation of merge sort?  

What is the runtime complexity of quick sort?  
What is the pseudocode/java implementation of quick sort?  



### Binary Trees and Heaps
Properties of Binary Trees
* minimum number of nodes in a binary tree of height h: n= h+1
* maximum number of nodes in a binary tre of height h: n= 2^(h+1) -1  
Methods for binary trees

Traversing through Binary Trees:

Balancing Binary Trees:

What is a binary search tree?

What are the methods in a binary search tree?  

What is the runtime complexity of a binary search tree?  

What is a min heap?  

What are the methods in a min heap?  

How does a heap work implemented in an array?  


Data Structures, Algorithms, and Programs
Data structure – Organization of data to solve the problem at hand
Algorithm – step-by-step procedure, which defines a set of instructions to be executed in a certain order to get the desired output.
Program – implementation of an algorithm in some programming language


Types of Data Structures
Static data structures(SDS)
are fixed sized (e.g. Arrays), the amount of memory once allocated to them cannot change on run time whereas.
Dynamic data structures(DDS)
(e.g. Linked Lists) have flexible size , they can grow or shrink as needed to contain the data to be stored.

* Algorithms are generally created independent of underlying languages.

Characteristics of an Algorithm
• Unambiguous − Algorithm should be clear and unambiguous. Each of its steps (or phases), and their inputs/outputs should be clear and
must lead to only one meaning.
• Input − An algorithm should have 0 or more well-defined inputs.
• Output − An algorithm should have 1 or more well-defined outputs, and should match the desired output.
• Finiteness − Algorithms must terminate after a finite number of steps.
• Feasibility − Should be feasible with the available resources.
• Independent − An algorithm should have step-by-step directions, which should be independent of any programming code.


Analysis of Algorithm
• Analysis of Algorithms is the determination of the amount of time, storage and/or other resources necessary to execute them.
• Analyzing algorithms is called Asymptotic Analysis.
• Asymptotic Analysis evaluate the performance of an algorithm.

Time Complexity
• Time complexity of an algorithm quantifies the amount of time taken by an algorithm.
• We can have three cases to analyze an algorithm:
        1. Worst Case
        2. Average Case
        3. Best Case


Worst Case Analysis : The case that causes maximum number of operations to be executed.
Average Case Analysis: We take all possible inputs and calculate computing time for all of the inputs.
Best Case Analysis: Calculate lower bound on running time of an algorithm

Most of the times, we do worst case analysis to analyze algorithms
• The average case analysis is not easy to do in most of the practical cases it is rarely done
• The best case analysis is bogus. Guaranteeing a lower bound on an algorithm doesn't provide any information.

Asymptotic Notations
1. Big O Notation: is an Asymptotic notation for the worst case.
2. Ω Notation (omega notation): is an Asymptotic notation for the best case.
3. Θ Notation (theta notation): is an Asymptotic notation for the worst case and the best case.


Linked List - Introduction
• Linked List is a Linear Data Structure represented by nodes.
• It is made of collection of connected, dynamically allocated Nodes
• Each node will have at least two elements
• Element (The data)
• The next node

Why Linked List
• Inserting or Deleting elements into or from list is easy, where it requires extensive data movement if array is used
• Linked List can grow or shrink dynamically based on the size of the list, but in array size is fixed once it is created

Linked List - Types
        Single Linked List
        • Can access the next node only
        • Last Node is set to null
        Doubly Linked List
        • Can access the next and Previous node
        • Last Node is set to null
        • Circular Linked List
        • Similar to Doubly linked List, but Last node points to the first node


Header & Trailer Nodes
• Header Node: A placeholder node at the beginning of list, used to simplify list processing. It doesn't hold any data but satisfies that every node has a previous node.
• Trailer Node: A Placeholder node at the end of list, used to simplify list processing.

Queue
• A collection whose elements are added to the rear of the queue and removed from the front of the queue
• A queue is a FIFO (first in, first out) data structure

Types of Queue
Simple Queue
• It defines the simple operation of queue in which insertion occurs at the rear of the list and 
deletion occurs at the front of the list

Circular Queue
• Insertion and deletion is similar to simple queue but the Last node is connected back to the first node.
• It is an abstract data type and It is also known as Ring buffer

Priority Queue
• Priority Queue contains data items which have some preset priority
• While removing, data item with highest priority is removed first
• Insertion is performed in the order of arrival.

Binary Search

Linear Search
Inserion Search

Maps
• A Map is a type of fast key lookup data structure that offers a flexible means of indexing into its individual elements.
• Also known as:
• table, search table, dictionary, associative array, or associative container
• Keys must be unique, meaning a given key can only represent one value

Sets
• A set is a collection of objects need not to be in particular order.

Lists
• List defines a sequential set of elements to which you can add new elements and remove or change existing ones.
• The list data structure typically has two very distinctive implementations — array list and linked list.
• Array List: It is basically a self-resizing array or, in other words, a dynamic array


Binary Search Tree
• Binary Search Tree is a tree where a node can have maximum of 2 children.

Graph

• A Graph is a non-linear data structure consisting of nodes and edges.
• The nodes are sometimes also referred to as vertices and the edges are  lines or arcs that connect any two nodes in the graph.
• A Graph consists of a finite set of vertices(or nodes) and set of Edges which  connect a pair of nodes.
• Graphs have become a powerful means of modelling and capturing data in  real-world scenarios such as social media networks, web pages and links,  and locations and routes in GPS.
• If you have a set of objects that are related to each other, then you can  represent them using a graph.

Types of graphs
• Weighted Graph
• Unweighted 
• Direct 
• Undirect
• Acyclic
• Cyclic
• Backedge

Cycle detection 
• A cycle is a path in a graph where the first and last vertices are the  same.
• If we start from one vertex, travel along a path and end up at the  starting vertex, then this path is a cycle.
• Cycle detection is the process of detecting these cycles.
Algorithms:
        - Floyd cycle detection algorithm
        - Brent’s algorithm

• Used in distributed message-based algorithms.
• Used to process large-scale graphs using a distributed processing  system on a cluster.
• Used to detect deadlocks in concurrent systems.
• Used in cryptographic applications to determine keys of a message  that can map that message to the same encrypted value.


Minimum spanning tree
• A minimum spanning tree is a subset of the edges of a graph that  connects all the vertices with the minimum sum of edge weights and  consists of no cycles.
Algorithms:
        - Prim’s algorithm
        - Kruskal’s algorithm

• Used to construct trees for broadcasting in computer networks.
• Used in graph-based cluster analysis.
• Used in image segmentation.
• Used in regionalization of socio-geographic areas, where regions are  grouped into contiguous regions.


Topological sorting
• Topological sorting of a graph is a linear ordering of its vertices so  that for each directed edge (u, v) in the ordering, vertex u comes  before v.
• Figure shows an example of a topological ordering of vertices (1, 2, 3,  5, 4, 6, 7, 8). You can see that vertex 5 should come after vertices 2  and 3. Similarly, vertex 6 should come after vertices 4 and 5.
Algorithms:
        - Kahn’s algorithm
        - The algorithm based on depth-first search

Applications
• Used in instruction scheduling.
• Used in data serialization.
• Used to determine the order of compilation tasks to perform in make  files.
• Used to resolve symbol dependencies in linkers.

Maximum flow

• We can model a graph as a flow network with edge weights as flow capacities.
In the maximum flow problem, we have to find a flow path that can obtain the maximum possible flow rate.
Algorithms
        -  Ford-Fulkerson algorithm
        -  Edmonds–Karp algorithm
        -  Dinic’s algorithm

• Used in airline scheduling to schedule flight crews.
• Used in image segmentation to find the background and the  foreground in an image.
• Used to eliminate baseball teams that cannot win enough games to  catch up to the current leader in their division.

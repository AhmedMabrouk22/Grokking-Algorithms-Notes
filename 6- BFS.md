## Introduction to graphs
A graph models a set of connections. Each graph is made up of nodes and edges.
A node can be directly connected to many other nodes. Those nodes are called its *neighbors*. 


## Breadth-first search
Breadth-first search is a different kind of search algorithm: one that runs on graphs. And using to solve *shortest-path problem*

*shortest-path problem You’re always trying to find the shortest something*

It can help answer two types of questions: 

- Question type 1: Is there a path from node A to node B?
- Question type 2: What is the shortest path from node A to node B?

The way breadth-first search works, the search radiates out from the starting point. So you’ll check first-degree connections before second-degree connections. And There’s a data structure for this: it’s called a ***queue***.

The queue is called a FIFO data structure: First In, First Out. In contrast, a stack is a LIFO data structure: Last In, First Out.

### Running time
Breadth-first search takes O(number of nodes + number of edges)


2 ways of traversing Graph.

# 1. BFS
### Pros. Find shortest Path
Given all of configurations and then using BFS to get result.
Applications: Rubik's Cube, Game, pazzles, web crawling

### Implementation:
* Using Queue
* avoid duplicated Vertexes
* record parent vertex

# 2. DFS 
### Pros. Detect circular path. 
Edge classification: Tree edge, forward edge, backward edge, cross edge.
Graph has a cycle if only if DFS has backward edge

### Topological sort
Given a directed acylic Graph. To order vertices so that all edges point from lower order to higher order. i.e. Job scheduling.

### Implementation
* Using recursion(stack) calls
* Reverse the finishing time

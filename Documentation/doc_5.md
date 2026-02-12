# Program 5: Exploring Graphs with BFS and DFS

## The Goal
This program is all about finding our way through an **undirected graph**. We're using an **adjacency matrix** to map it out, and then we're sending in two different explorers: **Breadth First Search (BFS)** and **Depth First Search (DFS)** to see how they visit the nodes.

## Graph Stuff
### Undirected Graph
Think of it like a network of cities where the roads go both ways. If City A connects to City B, then City B connects to City A. Simple.

### Adjacency Matrix
A 2D grid that represents the connections.
- `1` means there's a road.
- `0` means there isn't.
Since it's undirected, the matrix is symmetrical. `adj[i][j]` is the same as `adj[j][i]`.

## Tools We Use
- **Matrix**: The map.
- **Visited Array**: To keep track of where we've already been so we don't go in circles.
- **Queue**: Strictly for BFS.
- **Recursion**: The magic behind DFS.

## The Explorers

### `BFS(int start)`
This technique explores layer by layer. It checks all immediate neighbors first before moving further away. It uses a queue to line up the next spots to visit.

### `DFS(int start)`
This one is more adventurous. It picks a path and goes as deep as possible until it hits a dead end, then backtracks. It uses recursion to dive deep.

## How they work
### BFS
1. Start at a node.
2. Mark it visited, queue it.
3. Dequeue, visit all unvisited neighbors, enqueue them.
4. Repeat loop.

### DFS
1. Start at a node.
2. Mark visited.
3. Pick an unvisited neighbor and dive in (recurse).
4. Backtrack when stuck.

## Example Setup
Vertices: 0, 1, 2, 3
Edges: `0-1`, `0-2`, `1-3`, `2-4` (wait, let's keep it to 4 nodes for the matrix).
Let's say:
- 0 is connected to 1 and 2.
- 1 is connected to 3.
- 2 is connected to 3.

## Sample Run
```
BFS Traversal (starting at 0):
0 1 2 3

DFS Traversal (starting at 0):
0 1 3 2
```
(Note: DFS output depends on the order we check neighbors).
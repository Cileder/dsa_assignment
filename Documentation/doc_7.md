# Dijkstra’s Shortest Path Algorithm

## Introduction
This is an implementation of **Dijkstra's algorithm**. It's the standard way to find the shortest path from a starting point (Source) to every other spot in a weighted graph. Think of it like a GPS finding the quickest route avoiding traffic.

## Data Structures
### Graph
Represented by a **2D adjacency matrix**. `graph[i][j]` is the "cost" or distance between i and j. If it's 0, they aren't directly connected.

### Arrays
- `dist[]`: Holds the current shortest known distance from Source to everyone else.
- `visited[]`: Simple boolean checklist. Once we process a node, we check it off so we don't go back.

## Functions

### `minDistance(...)`
This helper scans the list of unvisited nodes to find the one with the smallest tentative distance. It's how we decide where to go next.

### `dijkstra(...)`
The big boss.
1. Initializes all distances to Infinity (or close to it) and source to 0.
2. In a loop: picks the closest unvisited node.
3. Updates the neighbors: "Hey, is it faster to get to you through me?"
4. Repeat until everyone is visited.

### `printDistances(...)`
Just prints the final `dist[]` array in a readable format.

## Main Flow
1. Define a graph (roads and weights).
2. Pick a starting city (vertex).
3. Run Dijkstra.
4. Print the result.

## Sample Output

```
Vertex   Distance from Source
0        0
1        4
2        12
3        19
4        21
5        11
```
(Based on a sample graph setup in the code)
# Program 3: Linked List Reverse Traversal

## What are we doing?
We're constructing a **Singly Linked List** and then printing it backwards using recursion. It's a classic interview-style problem to test if you understand pointers and the call stack.

## The Structs
- **Node**: A simple container with an `int value` and a specific pointer `next` to the neighbor node.

## Functions

### `makeNode(int val)`
Allocates memory for a new node and sets its value. Pretty distinct.

### `addEnd(Node** head, int val)`
Walks to the very end of the list and tacks on a new node. If the list is empty, the new node becomes the head.

### `printReverse(Node* node)`
This is the cool part. It recursively calls itself *before* printing. This means it goes all the way to the end, prints the last guy, returns, prints the second to last... and so on. It stacks up the calls.

## Main Logic
1. Start with an empty list.
2. Add some numbers: `1, 2, 3, 4, 5`.
3. Call `printReverse`.
4. Clean up memory (always important!).

## Output Example
If we feed it `1, 2, 3, 4, 5`, it spits out:
```
5 4 3 2 1
```

# Program 4: Doubly Linked List Operations

## Overview
This is a comprehensive implementation of a **Doubly Linked List**. Unlike the singly version, these nodes know who is in front *and* who is behind them (`prev` and `next`). It makes navigating back and forth a breeze.

## Functions Definition

### Insertion
- `insertBegin(int value)`: New guy gets cut in line at the very front.
- `insertEnd(int value)`: New guy joins the back of the queue.
- `insertAfterNode(Node* pre, int value)`: Squeezes a new node right after a specific one you point to.

### Deletion
- `deleteBegin()`: Removes the first node. (Sorry, head!)
- `deleteEnd()`: Chops off the tail of the list.

### Display
- `display()`: Just runs through the list from start to finish and prints the numbers so we can see our handiwork.

## Main Execution
We test all the functions in `main()`:
1. Start empty.
2. Insert `100` at start.
3. Insert `200` at end.
4. Insert `150` in the middle.
5. Delete the first and last to see if it breaks.
6. Show what's left.

## Sample Text Output
```
150
```
(Assuming we added 100, 200, inserted 150, then deleted 100 and 200).

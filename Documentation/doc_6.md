# Min Heap and Max Heap Implementation

## Intro
This code builds a **Min Heap** and a **Max Heap** from a messy, unsorted array. It's essentially organizing a group of numbers into a specific tree structure where the boss is either the smallest (Min) or largest (Max) value.

## Implementation Details

### Array Representation
We don't use fancy pointers here. We just use a simple array.
For any node at index `i`:
- Left kid is at `2*i + 1`.
- Right kid is at `2*i + 2`.
It's efficient and fits right in memory.

## The Functions

### `swap(int *a, int *b)`
Basic utility to trade places between two numbers. Essential for fixing the heap order.

### `minHeapify` and `maxHeapify`
These act as the enforcers.
- **MinHeapify**: Ensures the parent is smaller than both kids. If not, it swaps with the smallest kid and checks again further down.
- **MaxHeapify**: Ensures the parent is bigger than both kids. Swaps with the largest kid if needed.

### `buildMinHeap` and `buildMaxHeap`
These functions take an unsorted array and turn it into a valid heap. They start from the bottom (last non-leaf node) and work their way up to the root, calling heapify at each step.

## The Main Event
1. We take a random array.
2. Make copies of it (so we don't look dumb sorting an already sorted list).
3. Build the Min Heap and show it off.
4. Build the Max Heap and show that off too.

## Sample Output

```
Original Array:
5 15 10 20 30

Min Heap:
5 15 10 20 30
(Already close, but logic holds)

Max Heap:
30 20 10 5 15
```

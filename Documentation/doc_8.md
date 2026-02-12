# Program 8: Sorting Algorithms Showdown

## Objective
We're comparing different ways to sort a messy list of numbers. We generate `N` random integers and then let the user pick their poison (algorithm) to sort them. We also count how many times the computer had to compare two numbers or swap them, just for fun stats.

## The Contenders (Algorithms)

### 1. Bubble Sort
The classic. It steps through the list, swapping adjacent elements if they are in the wrong order. It loops through the list until no swaps are needed. Simple but slow.

### 2. Selection Sort
This one divides the list into sorted and unsorted parts. It repeatedly matches the smallest element from the unsorted sublist and moves it to the end of the sorted sublist.

### 3. Insertion Sort
Builds the final sorted array one item at a time. It's like sorting playing cards in your hand. efficient for small lists.

### 4. Merge Sort
The heavyweight. It divides the array in half, sorts each half recursively, and then merges them back together. Fast and stable, but uses a bit more memory.

## Stats Tracking
We use global or pass-by-reference counters to track:
- **Comparisons**: How many times did we ask "is A > B?"
- **Swaps**: How many times did we actually move data?

## Main Logic
1. Ask user for array size `N`.
2. Generate random numbers.
3. Show the mess.
4. User picks an algo (1-4).
5. We sort it and time it (with counters).
6. Print the clean result and the stats.

## Sample Output

```
Enter number of elements: 5
Unsorted array: 42 17 99 1 5

Choose sorting algorithm:
1. Bubble Sort
2. Selection Sort
3. Insertion Sort
4. Merge Sort
Enter choice: 3

Sorted array: 1 5 17 42 99
Total comparisons: 10
Total swaps: 7
```

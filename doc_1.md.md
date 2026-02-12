# Program 1: Checking for Balanced Parentheses

## What works in this code?
So, we're basically building a program to check if a mathematical expression has balanced parentheses. You know, making sure every `(` has a matching `)`. We're using a **stack** for this, which is basically just a fancy array where we only touch the top element. It helps us keep track of what we've seen so far.

## Data Structures
We've got a `Stack` struct. It's got:
- An array to hold the characters (brackets like `(`, `{`, `[`).
- A `top` integer to keep track of where we are.

## The Functions
Here's a breakdown of the helper functions we whipped up:

### 1. `push(Stack *s, char ch)`
This just throws a character onto the top of the stack. If the stack is full, it might print an error, but mostly it just increments `top` and puts the data there.

### 2. `pop(Stack *s)`
Takes the top element off. Simple as that. If the stack is empty (underflow), it returns a null character so we know we hit the bottom.

### 3. `isBalanced(char *exp)`
This is the brains of the operation. It walks through your expression string:
- If it sees an opener `(`, `{`, `[`, it pushes it.
- If it sees a closer `)`, `}`, `]`, it pops the stack and checks if they match.
- If everything matches up by the end and the stack is empty, we're good!

## Running the thing
In `main()`, we just ask the user for a string, feed it to `isBalanced()`, and print the result.

## Sample Output
Here is what it looks like when you run it:

```
Enter an expression: [x + y] * {z - w}
The parentheses are balanced.

Enter an expression: ((a + b) * c
The parentheses are not balanced.
```

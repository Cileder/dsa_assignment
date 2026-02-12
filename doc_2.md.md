# Program 2: Converting Infix to Postfix

## The Lowdown
This program is all about converting "normal" math expressions (Infix) like `A + B` into Postfix notation `A B +`, which is way easier for computers to process. Afterward, it actually interprets the postfix string to calculate a result.

## Data Stuff
We need two stacks for this magic to happen:
1. **Operator Stack (`opStack`)**: Holds things like `+`, `*`, `(` while we wait for their operands to show up.
2. **Value Stack (`valStack`)**: Used later to calculate the final number during evaluation.

## Key Functions

### `push()` and `pop()`
Standard stack operations. You know the drill—put stuff on top, take stuff off. We have separate ones for chars and ints.

### `priority(char op)`
Tells us how important an operator is. `^` is the king (3), `*` and `/` are next (2), and `+` and `-` are the lowest (1). This helps us decide order of operations.

### `toPostfix(char infix[], char postfix[])`
This converts the string. It follows these rules:
- Letters/Numbers? Send 'em straight to the output string.
- `(`? Push it.
- `)`? Pop until we find the matching `(`.
- Operators? Pop higher priority stuff first, then push the new one.

### `evalPostfix(char postfix[])`
Calculates the answer. It reads the postfix string, pushes numbers, and when it hits an operator, it pops the last two numbers, does the math, and pushes the result back.

## Usage
The `main()` function just orchestrates everything: gets input, converts it, prints the postfix, then solves it.

## Sample Run
```
Enter expression: (4+2)*3
Postfix: 42+3*
Result: 18
```

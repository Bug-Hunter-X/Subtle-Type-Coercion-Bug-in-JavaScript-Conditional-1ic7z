# Subtle Type Coercion Bug in JavaScript

This repository demonstrates a subtle bug in a JavaScript conditional statement related to type coercion. The bug arises from unexpected behavior when comparing numeric values with 0 in a conditional statement.

## Bug Description

The provided JavaScript code is supposed to perform the following checks:

1. If the input is `null`, return 0.
2. If the input is negative, return -1.
3. Otherwise (if the input is non-negative), return 1. 

However, due to loose type comparisons in JavaScript, the code returns 1 for 0.  The correct behavior should return 0 for a 0 input.

## How to Reproduce

1. Clone this repository.
2. Open `bug.js` in a JavaScript environment.
3. Run the code. Observe that the result for `foo(0)` is unexpectedly 1 instead of 0.

## Solution

The solution involves explicitly checking for 0 using strict equality (`===`).

## Files

- `bug.js`: The JavaScript code containing the bug.
- `bugSolution.js`: The corrected JavaScript code.
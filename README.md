# Infinite Recursion Bug in JavaScript

This repository demonstrates a common error in JavaScript: infinite recursion. The `foo` function in `bug.js` contains a recursive call without a proper base case, leading to a stack overflow error when called with certain input arguments. The corrected version is presented in `bugSolution.js`.

## How to Reproduce
1. Clone the repository.
2. Open `bug.js` and observe the recursive function `foo`.
3. Run `bug.js` using Node.js.  Observe the stack overflow error.
4. Open `bugSolution.js`.  Observe the corrected version.
5. Run `bugSolution.js` using Node.js.  Observe the correct output.

## Bug Analysis
The bug lies in the recursive nature of the `foo` function. If the initial value of `a` is less than `b`, the function will recursively call itself, incrementing `a` by one each time. However, the condition `a === b` is only met if `a` is initially equal to `b` leading to the infinite loop. 

## Solution
The solution involves ensuring that the base case is correctly defined. We need to stop the recursion under all possible scenarios. In `bugSolution.js`, the conditions are improved to handle the case where `a` might never be equal to `b`. 
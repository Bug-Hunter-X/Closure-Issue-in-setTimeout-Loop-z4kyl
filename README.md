# JavaScript Closure Issue in setTimeout Loop

This repository demonstrates a common JavaScript closure issue that arises when using `setTimeout` within a loop.  The expected behavior is to log the numbers 0 through 9 with a one-second delay between each. However, due to how closures work in JavaScript, the loop completes before the `setTimeout` callbacks execute, resulting in all callbacks logging the final value of `i` (which is 10). 

The `bug.js` file contains the erroneous code, and the `bugSolution.js` file demonstrates a solution using an immediately invoked function expression (IIFE) to create a separate scope for each iteration of the loop.
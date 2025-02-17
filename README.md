# JavaScript Loose Comparison Bug
This repository demonstrates a subtle bug related to JavaScript's loose comparison operator (`==`) when dealing with `NaN` (Not a Number) and positive/negative zero (`+0` and `-0`).

## The Problem
JavaScript's loose equality (`==`) does not follow the standard rules of equality in all cases. Specifically:

* `NaN` is never equal to itself, even using the loose comparison:
  ```javascript
  NaN == NaN; // false
  ```
* `+0` and `-0` are considered equal using loose comparison:
  ```javascript
  +0 == -0; // true
  ```
This behavior can lead to unexpected results and logic errors in your code.  The provided `bug.js` file shows this directly.

## The Solution
To avoid these issues, always use the strict equality operator (`===`) for comparisons.  The `bugSolution.js` file provides a corrected version using strict equality.
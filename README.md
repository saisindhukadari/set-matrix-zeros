# Set Matrix Zeros

## Problem

Given an `m × n` integer matrix, if an element is `0`, set its entire row and column to `0`. The modification must be done in-place.

## Approach

* Create two marker arrays:

  * One to keep track of the rows that contain a `0`.
  * One to keep track of the columns that contain a `0`.
* Traverse the matrix and mark the corresponding row and column whenever a `0` is found.
* Traverse the matrix again.
* If the current cell belongs to a marked row or a marked column, update it to `0`.

## Algorithm

1. Initialize two arrays to mark rows and columns.
2. Traverse the matrix and record all rows and columns containing `0`.
3. Traverse the matrix again.
4. Set every cell to `0` if its row or column is marked.
5. The modified matrix is the required output.

## Time Complexity

* **O(m × n)**

## Space Complexity

* **O(m + n)**

## Key Points

* Uses two extra arrays to store row and column information.
* Prevents newly updated zeros from affecting the traversal.
* Simple and easy-to-understand brute-force solution.
* The optimal approach reduces the extra space to **O(1)** by using the first row and first column as markers.

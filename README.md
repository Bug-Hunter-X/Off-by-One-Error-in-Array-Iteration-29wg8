# Off-by-One Error in Array Iteration

This repository demonstrates a common off-by-one error in Java that can lead to an `ArrayIndexOutOfBoundsException`. The provided code iterates through an array using a for loop, but the loop condition is incorrectly written, causing the index to go out of bounds.

The `BuggyArray.java` file contains the erroneous code, while `FixedArray.java` provides the corrected version.  The README provides a clear explanation of the error and its correction.

## Error Explanation

In Java, array indices are zero-based. This means that the first element has an index of 0, the second has an index of 1, and so on. The last element has an index of `array.length - 1`.  The buggy code attempts to access an index equal to `array.length`, which is beyond the bounds of the array, leading to the exception.

## Solution

The solution is to change the loop condition from `i <= array.length` to `i < array.length`. This ensures that the loop iterates only up to, but not including, the last valid index.
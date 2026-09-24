# Add Digits

LeetCode 258

## Problem Statement

Given an integer `num`, repeatedly add all its digits until the result has only one digit.

Return the final single-digit result.

## Solution

This solution repeatedly separates the digits of the number, adds them together, and continues the process until only one digit remains.

For example, if the number is `38`, first calculate `3 + 8 = 11`. Then calculate `1 + 1 = 2`. Therefore, the final answer is `2`.

## Example

### Input

```text
num = 38
```

### Output

```text
2
```

### Explanation

The process is:

```text
38 → 3 + 8 = 11
11 → 1 + 1 = 2
```

The final single digit is `2`.

## Approach

1. Check whether the number has more than one digit.
2. Extract each digit using the modulo operator.
3. Add all the digits together.
4. Replace the number with the calculated sum.
5. Repeat until the number contains only one digit.
6. Return the final digit.

## Algorithm

1. Start with the given number.
2. While the number is greater than or equal to `10`:

   * Set `total = 0`.
   * Extract each digit using `num % 10`.
   * Add the digit to `total`.
   * Remove the last digit using integer division.
3. Set `num = total`.
4. Continue until `num` is a single digit.
5. Return `num`.

## Complexity

* Time Complexity: O(log n)
* Space Complexity: O(1)

## Author

T. Nandhini

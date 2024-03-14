# Maximum Subarray Sum Using Kadane's Algorithm

Welcome to the detailed guide on implementing Kadane's Algorithm to find the maximum sum of a contiguous subarray within a one-dimensional array of numbers. This powerful algorithm offers an efficient solution, boasting a linear runtime complexity of O(n), which makes it ideal for processing large datasets swiftly.

## Introduction

Kadane's Algorithm, a cornerstone in the field of computer science and dynamic programming, elegantly solves the maximum subarray sum problem. Unlike brute-force approaches that examine all possible subarrays, Kadane's method smartly traverses the array once, updating sums to find the maximum.

### What You Will Learn

- The logic behind Kadane's Algorithm
- Step-by-step Python implementation
- Practical applications and insights

## Getting Started

Before diving into the algorithm, ensure you have a basic understanding of Python and familiarity with concepts like arrays and iteration.

### Prerequisites

- Python 3.x installed on your machine
- A text editor or an IDE (Integrated Development Environment) like PyCharm or Visual Studio Code
- Basic knowledge of Python syntax and loops

## Implementation Details

Kadane's Algorithm hinges on two primary concepts: **local maximum subarray sum** at each array position and **global maximum subarray sum** found so far. Here's how it works:

```python
# Initialize the array
a = [-2, 1, -3, 4, -1, 2, 1, -5, 4]

# Set initial values for the maximum sums
now_max = a[0]  # Current maximum sum
end_max = a[0]  # Maximum sum at the end of the array

# Iterate through the array starting from the second element
for i in a[1:]:
    # Update the end_max to the higher of the current element or the sum of current element and end_max
    end_max = max(i, end_max + i)
    # Update now_max if end_max is higher
    now_max = max(now_max, end_max)

# Output the maximum sum
print(f"Maximum Sum of Contiguous Subarray: {now_max}")

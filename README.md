# Maximum Subarray Sum 

Welcome to the detailed guide on how to resolve this problem with a difficult of O(n)



## Getting Started

Before diving into the algorithm, ensure you have a basic understanding of Python and familiarity with concepts like arrays and iteration.

### Prerequisites

- Python 3.x installed on your machine
- A text editor or an IDE (Integrated Development Environment) like PyCharm or Visual Studio Code
- Basic knowledge of Python syntax and loops

## Implementation Details
 Algorithm hinges on two primary concepts: **local maximum subarray sum** at each array position and **global maximum subarray sum** found so far. Here's how it works:

```python
# The test
a = [-2, 1, -3, 4, -1, 2, 1, -5, 4]

# The validation
now_max = a[0]  
end_max = a[0]  

# The iteration
for i in a[1:]:
    end_max = max(i, end_max + i)
    now_max = max(now_max, end_max)

print(f"Maximum Sum of Contiguous Subarray: {now_max}")

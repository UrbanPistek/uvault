# Example Questions

## Question 1
Given an array, return the number of occurances of each number, in sorted form. 
```python
class Solution:
    # @param A : list of integers
    # @return a list of integers
    def findOccurences(self, a):
        d = defaultdict(int)
        for e in a:
            d[e] += 1
            
        return [v for _, v in sorted(d.items())]

```
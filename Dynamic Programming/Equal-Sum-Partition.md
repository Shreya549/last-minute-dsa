# Equal Sum Partition

> Divide the given array into 2 subsets such that the sum of both the subsets are equal.

> [Link to the question](https://www.geeksforgeeks.org/split-array-two-equal-sum-subarrays/)

> This question is a variation of [Subset Sum Problem](https://github.com/Shreya549/last-minute-dsa/blob/main/Dynamic%20Programming/Subset-Sum.md)
## Input
| Variable Name | Data Type | Use | 
|---- | ----- | ----- |
| arr | int[] | Given array |
| n | int | Number of elements in the array |

## Initial Checks

- If sum of array is odd, we cannot divide the array into 2 equal subsets
```
if (sum(arr)%2 == 1):
  return False
```

- We need to find if a subset whose sum is n/2 exists

```s = n//2```

### Refer [Subset Sum Problem](https://github.com/Shreya549/last-minute-dsa/blob/main/Dynamic%20Programming/Subset-Sum.md) for the code

<p align="center">
	With :heart: by <a href="https://github.com/Shreya549" target="_blank">Shreya Chatterjee</a>
</p>

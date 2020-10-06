# Count Subsets with given Difference

> Divide the array into 2 subsets such that the difference of the sum of these two subsets is equal to the given number. Find the count of such possible subsets.

> [Link to the question](https://www.geeksforgeeks.org/partition-a-set-into-two-subsets-such-that-the-difference-of-subset-sums-is-minimum/)

> This question is a variation of [Count Subsets Problem](https://github.com/Shreya549/last-minute-dsa/blob/main/Dynamic%20Programming/Count-Subsets.md)

## Input
| Variable Name | Data Type | Use | 
|---- | ----- | ----- |
| arr | int[] | Given array |
| n | int | Number of elements in the array |
| d | int | Given difference |

## Initial Calculation

- Find sum of given array
```
sm = sum(arr)
```

- Calculation
```
# s1 = sum(Subset 1)
# s2 = sum(Subset 2)

s1 + s2 = sm
s1 - s2 = d
____________

2s1 = sm + d
s1 = (sm+d)/2

```

- We need to find the count of subsets whose sum is (sm+d)/2

```s = (sm+d)//2```

### Refer [Count Subsets Problem](https://github.com/Shreya549/last-minute-dsa/blob/main/Dynamic%20Programming/Count-Subsets.md) for the code

<p align="center">
	With :heart: by <a href="https://github.com/Shreya549" target="_blank">Shreya Chatterjee</a>
</p>

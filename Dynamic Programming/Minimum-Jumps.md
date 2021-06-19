# Minimum Number of Jumps

> Given an array of N integers arr[] where each element represents the max number of steps that can be made forward from that element. Find the minimum number of jumps to reach the end of the array (starting from the first element). If an element is 0, then you cannot move through that element.

> [Link to the problem](https://practice.geeksforgeeks.org/problems/minimum-number-of-jumps-1587115620/1#)

## Input
| Variable Name | Data Type | Use | 
|---- | ----- | ----- |
| arr | int[] | Array of steps |
| n | int | Length of jump array |

## Other variables
| Variable Name | Data Type | Use | 
|---- | ----- | ----- |
| dp | int[] | DP Array |
| i | int | To access destination cells |
| j | int | To access all cells before destination cells |
| maxi | int | An integer greater than the maximum value of possible minimum number of jumps |

## Top Down Approach

- DP Array is of int type

`dp[n]`

- Initialize array
```
maxi = 10000001
dp = [maxi for i in range(n)]
dp[0] = 0
```

- Filling in the rest of the elements

```
for i in range(1, n):
  for j in range(i):
      if (j + arr[j] >= i):
          if (dp[j] != maxi):
              dp[i] = min(dp[i], dp[j] + 1)
```

- Answer
```
if dp[-1] == maxi:
    return -1

return dp[-1]
```

<p align="center">
	With :heart: by <a href="https://github.com/Shreya549" target="_blank">Shreya Chatterjee</a>
</p>

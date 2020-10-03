# Subset Sum Problem

> [Link to the question](https://www.geeksforgeeks.org/subset-sum-problem-dp-25/)

> This question is a variation of [0-1 Knapsack Problem](https://github.com/Shreya549/last-minute-dsa/blob/main/Dynamic%20Programming/0-1-Knapsack.md)
## Input
| Variable Name | Data Type | Use | 
|---- | ----- | ----- |
| arr | int[] | Given array |
| n | int | Number of elements in the array |
| s | int | Sum |
| dp | bool[][] | DP Matrix |

## Recursive Approach
```	
def subset_sum(arr, n, s):

  if (s == 0):
    return True
    
  if (n==0):
    return False
    
  else:
  
    if (arr[n-1] > s):
      return subset_sum(arr, n-1, s)
      
    else:
      return subset_sum(arr, n-1, s-arr[n-1]) or subset_sum(arr, n-1, s)
```

## Top Down Approach

- DP Matrix is of Boolean type

`dp[n+1][s+1]`

- DP Matrix initialization

```
for j in range(s+1):
  dp[0][j] = True
  
for i in range(1, n+1):
  dp[i][0] = False
```

- Filling in the rest of the elements

```
for i in range (1, n+1):
  for j in range (1, s+1):
  
    if (arr[i-1] > j):
      dp[i][j] = dp[n-1][j]
      
    else:
      dp[i][j] = dp[n-1][s-arr[n-1]] or dp[n-1][s]
```

- Answer

`dp[n][w]`

<p align="center">
	With :heart: by <a href="https://github.com/Shreya549" target="_blank">Shreya Chatterjee</a>
</p>

# Count of Subsets - Sum with a given Sum

> Find the number of subsets whose sum is equal to a given number.

> [Link to the question](https://www.geeksforgeeks.org/count-of-subsets-with-sum-equal-to-x/)

> This question is a variation of [Subset Sum Problem](https://github.com/Shreya549/last-minute-dsa/blob/main/Dynamic%20Programming/Subset-Sum.md)

## Input
| Variable Name | Data Type | Use | 
|---- | ----- | ----- |
| arr | int[] | Given array |
| n | int | Number of elements in the array |
| s | int | Sum |

## Other variables
| Variable Name | Data Type | Use | 
|---- | ----- | ----- |
| dp | int[][] | DP Matrix |
| i | int | To access rows of the matrix |
| j | int | To access columns of the matrix |

## Recursive Approach
```	
def count_subset(arr, n, s):

  if (s == 0):
    return 1
    
  if (n==0):
    return 0
    
  else:
  
    if (arr[n-1] > s):
      return count_subset(arr, n-1, s)
      
    else:
      return count_subset(arr, n-1, s-arr[n-1]) + count_subset(arr, n-1, s)
```

## Top Down Approach

- DP Matrix is of int type

`dp[n+1][s+1]`

- DP Matrix initialization

```
for j in range(s+1):
  dp[0][j] = 0
  
for i in range(n+1):
  dp[i][0] = 1
```

- Filling in the rest of the elements

```
for i in range (1, n+1):
  for j in range (1, s+1):
  
    if (arr[i-1] > j):
      dp[i][j] = dp[n-1][j]
      
    else:
      dp[i][j] = dp[n-1][s-arr[n-1]] + dp[n-1][s]
```

- Answer

`dp[n][s]`


<p align="center">
	With :heart: by <a href="https://github.com/Shreya549" target="_blank">Shreya Chatterjee</a>
</p>

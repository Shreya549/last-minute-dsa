# Matrix Chain Multiplication

> [Link to the question](https://www.geeksforgeeks.org/matrix-chain-multiplication-dp-8/)

## Input
| Variable Name | Data Type | Use | 
|---- | ----- | ----- |
| arr | int[] | Given array |
| n | int | Number of elements in the array |

## Other variables
| Variable Name | Data Type | Use | 
|---- | ----- | ----- |
| dp | bool[][] | DP Matrix |
| i, j, k, L | int | Variables for loop |

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

- DP Matrix is of int type

`dp[n][n]`

- DP Matrix initialization

```
dp = []
for i in range(n):
  dp.append([0]*n)
 
```

- Filling in the rest of the elements

```
for L in range (2, n):

  for i in range (1, n+L-1):
  
    j = i - L + 1
    
    for k in range(i, j):
    
      dp[i][j] = min(dp[i][j], dp[i][k] + dp[k][j] + arr[i-1] * arr[k] * arr[j]
  
```

- Answer

`dp[1][n-1]`

<p align="center">
	With :heart: by <a href="https://github.com/Shreya549" target="_blank">Shreya Chatterjee</a>
</p>

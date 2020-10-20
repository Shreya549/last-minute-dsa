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
    
    dp[i][j] = sys.maxint
    
    for k in range(i, j):
    
      dp[i][j] = min(dp[i][j], dp[i][k] + dp[k+1][j] + arr[i-1] * arr[k] * arr[j])
  
```

- Answer

`dp[1][n-1]`

<p align="center">
	With :heart: by <a href="https://github.com/Shreya549" target="_blank">Shreya Chatterjee</a>
</p>

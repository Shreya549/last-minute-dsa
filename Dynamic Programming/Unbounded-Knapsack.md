# 0-1 Knapsack Problem

> You are given a list of values of items with their respective weights along with the weight of the knapsack. Find the maximum value of the knapsack after filling in the items. Repitition allowed.
> [Link to the question](https://www.geeksforgeeks.org/unbounded-knapsack-repetition-items-allowed/)

> This is a variant of [0-1 Knapsack](https://github.com/Shreya549/last-minute-dsa/blob/main/Dynamic%20Programming/0-1-Knapsack.md)

## Input
| Variable Name | Data Type | Use | 
|---- | ----- | ----- |
| wt | int[] | Weight of items |
| val | int[] | Value of items |
| n | int | Number of items |
| w | int | Weight of knapsack |

## Other Variables
| Variable Name | Data Type | Use | 
|---- | ----- | ----- |
| dp | int[][] | DP Matrix |
| i | int | To access rows of the matrix |
| j | int | To access columns of the matrix |

## Recursive Approach
```	
def knapsack(wt, val, n, w):

  if (w == 0 or n == 0):
    return 0
    
  else:
  
    if (wt[n-1] > w):
      return knapsack(wt, val, n-1, w)
      
    else:
      return max(val[n-1] + knapsack(wt, val, n, w-wt[n-1]), knapsack(wt, val, n-1, w))
```

## Top Down Approach

```
dp[n+1][w+1]

# DP to be initialized with 0

for i in range (1, n+1):
  for j in range (1, w+1):
  
    if (wt[i-1] > j):
      dp[i][j] = dp[n-1][j]
      
    else:
      dp[i][j] = max(val[n-1] +dp[n][w-wt[n-1]], dp[n-1][w])
      
```
- Answer

`dp[n][w]`

<p align="center">
	With :heart: by <a href="https://github.com/Shreya549" target="_blank">Shreya Chatterjee</a>
</p>

# Coin Change Problem

> Given a value N, if we want to make change for N cents, and we have infinite supply of each of S = { S1, S2, .. , Sm} valued coins, how many ways can we make the change? The order of coins doesn’t matter.

> [Link to the problem](https://practice.geeksforgeeks.org/problems/coin-change2448/1)

> This is a variant of [Unbounded Knapsack](https://github.com/Shreya549/last-minute-dsa/blob/main/Dynamic%20Programming/Unbounded-Knapsack.md)

## Input
| Variable Name | Data Type | Use | 
|---- | ----- | ----- |
| coins | int[] | Array of value of coins available |
| n | int | Number of denominations |
| s | int | Sum required |

## Other Variables
| Variable Name | Data Type | Use | 
|---- | ----- | ----- |
| dp | int[][] | DP Matrix |
| i | int | To access rows of the matrix |
| j | int | To access columns of the matrix |

## Approach

- If the nth coin has value <= sum required, then there are 2 options
  - Use the coin and subtract the coin value from the reqd. sum
  - Do not use the coin and move to the (n-1)th coin

- Else, move to the (n-1)th coin

## Recursive Approach
```	
def change(coins, n, s):

  if (n == 0):
    return 0
    
  if (s==0):
    return 1
    
  else:
  
    if (coins[n-1] <= s):
      return change(coins, n, s - coins[n-1]) + change(coins, n-1, s)
      
    else:
      return change(coins, n-1, s) 
```

## Top Down Approach

```
dp[s+1][n+1]

# DP to be initialized with 0
# First row of the matrix to be initialized with 1

for i in range (1, s+1):
  for j in range (1, n+1):
  
    if (arr[j-1] <= i):
       dp[i][j] = dp[i][j-1] + dp[i-arr[j-1]][j]
                    
    else:
       dp[i][j] = dp[i][j-1]
```

## Answer

`dp[-1][-1]`

<p align="center">
	With :heart: by <a href="https://github.com/Shreya549" target="_blank">Shreya Chatterjee</a>
</p>

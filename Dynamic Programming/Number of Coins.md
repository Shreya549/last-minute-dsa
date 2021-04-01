# Number of Coins

> Given a value V and array coins[] of size M, the task is to make the change for V cents, given that you have an infinite supply of each of coins{coins1, coins2, ..., coinsm} valued coins. Find the minimum number of coins to make the change. If not possible to make change then output -1

> [Link to the problem](https://practice.geeksforgeeks.org/problems/number-of-coins1824/1)

## Input
| Variable Name | Data Type | Use | 
|---- | ----- | ----- |
| coins | int[] | Array of value of coins available |
| n | int | Number of denominations |
| s | int | Sum required |

## Other Variables
| Variable Name | Data Type | Use | 
|---- | ----- | ----- |
| dp | int[][] | DP List |
| i | int | To access elements of the list |

## Initialization
```
for i in range(s+1):
  dp.append(maxsize)

dp[0] = 0
```

## Top Down Approach
```	
for i in range(1, s+1):
  for j in range(n):
  
    if coins[j] <= i:
      ans = dp[i-coins[j]]
      
      if (not ans == maxsize) and ans + 1 < dp[i]:
		    dp[i] = ans + 1
```

## Answer
```
if (dp[-1] == maxsize):
  return -1
  
return (dp[-1])
```

<p align="center">
	With :heart: by <a href="https://github.com/Shreya549" target="_blank">Shreya Chatterjee</a>
</p>



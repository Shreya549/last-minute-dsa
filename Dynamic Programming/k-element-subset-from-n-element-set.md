# k-Element subsets from n-element set

> Find the number of ways that k objects can be chosen from among n objects.

> The number k-element subsets that can be made from n-element sets.

> Write a function that takes two parameters n and k and returns the value of Binomial Coefficient C(n, k).

> Binomial Coefficients `C(n, k)` - coefficient of x^k in the expansion of (1 + x)^n.

> [Link to the question](https://www.geeksforgeeks.org/binomial-coefficient-dp-9/)

## Input
| Variable Name | Data Type |
|---- | ----- | 
| n | int | 
| k | int |

## Other variables
| Variable Name | Data Type | Use | 
|---- | ----- | ----- |
| dp | int[][] | DP Matrix |
| i | int | To access rows of the matrix |
| j | int | To access columns of the matrix |

## Formula 

```
C(n, k) = C(n-1,k) + C(n-1, k-1)
C(n, 0) = C(n, n) = 1
```

## Initialization

- `dp[k+1][n+1]`

- Initialize complete matrix with 1
  ```
  for i in range(k+1):
    dp.append([1 for j in range(n+1)])
  ```
  
- Initialize first column with 0
  ```
    for i in range(k+1): 
      dp[i][0] = 0
    ```
    
## Top Down Approach

```
for i in range(1, k+1):
    for j in range(1, n+1):
      if (i==j):
        dp[i][j] = 1
        
      else:
        dp[i][j] = dp[i][j-1] + dp[i-1][j-1]
 ```
 
## Answer
`dp[-1][-1]`

<p align="center">
	With :heart: by <a href="https://github.com/Shreya549" target="_blank">Shreya Chatterjee</a>
</p>
  

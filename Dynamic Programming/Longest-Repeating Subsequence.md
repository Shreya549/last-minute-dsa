# Longest Repeating Subsequence

> Given a string, find the length of the longest repeating subsequence

> [Link to the question](https://leetcode.com/problems/longest-common-subsequence/)

> This question is similar to [Longest Common Subsequence](https://github.com/Shreya549/last-minute-dsa/blob/main/Dynamic%20Programming/Longest-Common-Subsequence.md)

## Input
| Variable Name | Data Type | Use | 
|---- | ----- | ----- |
| s | String | First String |
| n | int | Length of first String |

## Other variables
| Variable Name | Data Type | Use | 
|---- | ----- | ----- |
| dp | int[][] | DP Matrix |
| i | int | To access rows of the matrix |
| j | int | To access columns of the matrix |


## Top Down Approach

- The second string is considered to be **s** itself
```
s1 = s
s2 = s
```
- DP Matrix is of int type

`dp[n+1][n+1]`

- Initialize matrix with 0


- Filling in the rest of the elements

```
for i in range (1, n+1):
  for j in range (1, n+1):
  
    if (s1[i-1] == s2[j-1] and not i == j): 
      dp[i][j] = 1 + dp[i-1][j-1]
      
    else:
      dp[i][j] = max(dp[i-1][j], dp[i][j-1])
```

- Answer

`dp[n][n]`

<p align="center">
	With :heart: by <a href="https://github.com/Shreya549" target="_blank">Shreya Chatterjee</a>
</p>

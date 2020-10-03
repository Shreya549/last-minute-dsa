# Longest Common Subsequence

> Given 2 strings, find the length of the longest common subsequence

> [Link to the question](https://leetcode.com/problems/longest-common-subsequence/)

## Input
| Variable Name | Data Type | Use | 
|---- | ----- | ----- |
| s1 | String | First String |
| n | int | Length of first String |
| s2 | String | Second String |
| n2 | int | Length of second String |

## Other variables
| Variable Name | Data Type | Use | 
|---- | ----- | ----- |
| dp | int[][] | DP Matrix |
| i | int | To access rows of the matrix |
| j | int | To access columns of the matrix |

## Recursive Approach
```	
def lcs(s1, s2, n1, n2):

  if (n1 == 0 or n2 == 0):
    return 0
    
  else:
  
    if (s1[n1-1] == s2[n2-1]):
      return 1 + lcs(s1, s2, n1-1, n2-1)
      
    else:
      return max(lcs(s1, s2, n1-1, n2), lcs(s1, s2, n1, n2-1))
```

## Top Down Approach

- DP Matrix is of int type

`dp[n1+1][n2+1]`

- Initialize matrix with 0


- Filling in the rest of the elements

```
for i in range (1, n1+1):
  for j in range (1, n2+1):
  
    if (s1[i-1] == s2[j-1]):
      dp[i][j] = 1 + dp[i-1][j-1]
      
    else:
      dp[i][j] = max(dp[i-1][j], dp[i][j-1])
```

- Answer

`dp[n1][n2]`

<p align="center">
	With :heart: by <a href="https://github.com/Shreya549" target="_blank">Shreya Chatterjee</a>
</p>

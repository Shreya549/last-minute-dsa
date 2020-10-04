# Printing Longest Common Subsequence

> Given 2 strings, print the longest common subsequence

> [Link to the question](https://leetcode.com/problems/longest-common-subsequence/)

> This question is a variant of [Longest Common Subsequence](https://github.com/Shreya549/last-minute-dsa/blob/main/Dynamic%20Programming/Longest-Common-Subsequence.md)

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
| s | String | Longest Common Subsequence |

## Refer [Longest Common Subsequence](https://github.com/Shreya549/last-minute-dsa/blob/main/Dynamic%20Programming/Longest-Common-Subsequence.md) to generate the DP matrix.

## Further steps

- DP Matrix is of int type

`dp[n1+1][n2+1]`

- Initialize the variables

```
i = n1
j = n2
s = ""
```

- Traversing the matrix

```
while (i > 0 and j > 0):
  if (s1[i] == s2[j]):
    s += s1[i]
    i-=1
    j-=1
    
  else:
    if (dp[i-1][j] > dp[i][j-1]):
      i-=1
    else:
      j-=1
```

- Answer

`s[::-1]`

<p align="center">
	With :heart: by <a href="https://github.com/Shreya549" target="_blank">Shreya Chatterjee</a>
</p>

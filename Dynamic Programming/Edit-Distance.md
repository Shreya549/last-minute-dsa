# Edit Distance

> Given two strings s and t. Find the minimum number of operations that need to be performed on str1 to convert it to str2. The possible operations are: Insert, Remove and Replace

> [Link to the question](https://practice.geeksforgeeks.org/problems/edit-distance3702/1#)

> This question is similar to [Longest Common Subsequence](https://github.com/Shreya549/last-minute-dsa/blob/main/Dynamic%20Programming/Longest-Common-Subsequence.md)

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
def ed(s1, s2, n1, n2):

  if n1 == 0:
    return n2
    
  if n2 == 0:
    return n1
    
  else:
  
    if (s1[n1-1] == s2[n2-1]):
      return ed(s1, s2, n1-1, n2-1)
      
    else:
      return 1 + min(ed(s1, s2, n1-1, n2), ed(s1, s2, n1, n2-1), ed(s1, s2, n1-1, n2-1))
```

## Top Down Approach

- DP Matrix is of int type

`dp[n1+1][n2+1]`

- Initialize matrix
```
for i in range(n1+1):
    dp.append([0] * (n2+1))

for j in range(n2+1):
    dp[0][j] = j

for i in range(n1+1):
    dp[i][0] = i
```

- Filling in the rest of the elements

```
for i in range (1, n1+1):
  for j in range (1, n2+1):
  
    if (s1[i-1] == s2[j-1]):
      dp[i][j] = dp[i-1][j-1]
      
    else:
      dp[i][j] = 1 + min(dp[i-1][j], dp[i][j-1], dp[i-1][j-1])
```

- Answer

`dp[n1][n2]`

<p align="center">
	With :heart: by <a href="https://github.com/Shreya549" target="_blank">Shreya Chatterjee</a>
</p>



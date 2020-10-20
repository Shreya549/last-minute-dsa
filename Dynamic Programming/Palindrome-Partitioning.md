# Palindrome Partitioning

> Given a string, find the minimum number of cuts required to divide the string into palindromic substrings

> [Link to the question](https://practice.geeksforgeeks.org/problems/palindromic-patitioning4845/1)

> This question is a type of [Matrix Chain Multiplication](https://github.com/Shreya549/last-minute-dsa/blob/main/Dynamic%20Programming/Matrix-Chain-Multiplication.md)

## Input
| Variable Name | Data Type | Use | 
|---- | ----- | ----- |
| s | String | Given string |
| n | int | Length of the string |

## Other variables
| Variable Name | Data Type | Use | 
|---- | ----- | ----- |
| P | bool[][] | DP Matrix to store if the substring is palindrome or not |
| C | int[][] | DP Matrix to store the number of cuts required |
| L | int | Length of substring |
| i, j | int | Looping variables |


## Top Down Approach

- P Matrix is of Boolean type

`P[n][n]`

- C Matrix is of int type

`C[n][n]`

- DP Matrix initialization

```
for i in range(n):

  C.append([0]*n)
  
  P.append([False]*n)

for i in range(n):
  P[i][i] = True
 
```

- Filling in the rest of the elements

```
for L in range (2, n):

  for i in range (1, n+L-1):
  
    j = i - L + 1
    
    if (L==2):
      P[i][j] = s[i]==s[j]
     
    else:
      P[i][j] = s[i]==s[j] and P[i+1][j-1]
    
    if P[i][j] == True:
      C[i][j] = 0
    
    else:
      C[i][j] = sys.maxint
      for k in range(i, j):

        C[i][j] = min(C[i][j], dp[i][k] + dp[k+1][j] + 1)
  
```

- Answer

`C[0][n-1]`

<p align="center">
	With :heart: by <a href="https://github.com/Shreya549" target="_blank">Shreya Chatterjee</a>
</p>

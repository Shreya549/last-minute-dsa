# Minimum Deletion for Palindrome

> Given a string, find the minimum number of deletions required to make it palindrome

> [Link to the question](https://www.geeksforgeeks.org/minimum-number-deletions-make-string-palindrome/)

> This question is a variant of [Longest Palindromic Subsequence](https://github.com/Shreya549/last-minute-dsa/blob/main/Dynamic%20Programming/Longest-Palindromic-Subsequence.md)

## Input
| Variable Name | Data Type | Use | 
|---- | ----- | ----- |
| s | String | String |
| n | int | Length of String |

## Other variables
| Variable Name | Data Type | Use | 
|---- | ----- | ----- |
| dp | int[][] | DP Matrix |
| i | int | To access rows of the matrix |
| j | int | To access columns of the matrix |

## Top Down Approach

- Refer [Longest Palindromic Subsequence](https://github.com/Shreya549/last-minute-dsa/blob/main/Dynamic%20Programming/Longest-Palindromic-Subsequence.md) to get the length of the longest Palindromic Subsequence

```
lps = dp[n][n]
```
- Answer
```
n-lps
```

<p align="center">
	With :heart: by <a href="https://github.com/Shreya549" target="_blank">Shreya Chatterjee</a>
</p>

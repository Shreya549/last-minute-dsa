# Longest Palindromic Subsequence

> Given a string, find the longest palindromic subsequence

> [Link to the question](https://www.geeksforgeeks.org/print-longest-palindromic-subsequence/)

> This question is a similar to [Longest Common Subsequence](https://github.com/Shreya549/last-minute-dsa/blob/main/Dynamic%20Programming/Longest-Common-Subsequence.md)

## Input
| Variable Name | Data Type | Use | 
|---- | ----- | ----- |
| s1 | String | First String |
| n | int | Length of first String |

## Other variables
| Variable Name | Data Type | Use | 
|---- | ----- | ----- |
| dp | int[][] | DP Matrix |
| i | int | To access rows of the matrix |
| j | int | To access columns of the matrix |

## Top Down Approach

- We need to find the LCS of String s and reverse of String s
 ```
 lcs(s, s[::-1])
 ```
- Refer [Longest Common Subsequence](https://github.com/Shreya549/last-minute-dsa/blob/main/Dynamic%20Programming/Longest-Common-Subsequence.md) for the code



<p align="center">
	With :heart: by <a href="https://github.com/Shreya549" target="_blank">Shreya Chatterjee</a>
</p>

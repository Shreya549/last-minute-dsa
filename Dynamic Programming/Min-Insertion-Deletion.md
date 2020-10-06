# Minimum Insertion Deletion

> Given 2 strings, find the minimum number of Insertion and Deletion required to transform one string into another.

> [Link to the question](https://www.geeksforgeeks.org/minimum-number-deletions-insertions-transform-one-string-another/)

> This question is a similar to [Longest Common Subsequence](https://github.com/Shreya549/last-minute-dsa/blob/main/Dynamic%20Programming/Longest-Common-Subsequence.md)

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

## Top Down Approach

- Refer [Longest Common Subsequence](https://github.com/Shreya549/last-minute-dsa/blob/main/Dynamic%20Programming/Longest-Common-Subsequence.md)
 to get the length of the longest common subsequence
 ```
 lcs = dp[n1][n2]
 ```

- Deletion required

`n1 - lcs`

- Insertion required

`n2 - lcs`

<p align="center">
	With :heart: by <a href="https://github.com/Shreya549" target="_blank">Shreya Chatterjee</a>
</p>

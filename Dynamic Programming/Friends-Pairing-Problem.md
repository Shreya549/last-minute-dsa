# Friends Pairing Problem

> Given n friends, each one can remain single or can be paired up with some other friend. Each friend can be paired only once. Find out the total number of ways in which friends can remain single or can be paired up.

> [Link to the question](https://practice.geeksforgeeks.org/problems/friends-pairing-problem5425/1)

## Input
| Variable Name | Data Type | Use | 
|---- | ----- | ----- |
| n | int | Number of friends |

## Approach
- If the nth friend decides to stay single then number of ways are `f(n-1)`
- If the nth friend decides to pair up then he has `n-1` options, i.e number of ways = `(n-1)*f(n-2)`
- Therefore `f(n) = f(n-1) + (n-1) * f(n-2)`

## Other variables
| Variable Name | Data Type | Use | 
|---- | ----- | ----- |
| dp | int[][] | DP Matrix |
| i | int | To access rows of the matrix |
| j | int | To access columns of the matrix |
| result | int | To store the ans |

## Top Down Approach
 ```
 dp[n]
 # Initialize dp with i+1
 
 for i in range(2, n):
     dp[i] = dp[i-1] + i*dp[i-2]
 ```
 
 ## Answer
 `dp[-1]`
 
 <p align="center">
	With :heart: by <a href="https://github.com/Shreya549" target="_blank">Shreya Chatterjee</a>
</p>

# Minimum cost to fill given weight in a bag 

> Given an array cost[] of positive integers of size N and an integer W, cost[i] represents the cost of ‘i’ kg packet of oranges, the task is to find the minimum cost to buy W kgs of oranges. If it is not possible to buy exactly W kg oranges then the output will be -1

> [Link to the question](https://practice.geeksforgeeks.org/problems/minimum-cost-to-fill-given-weight-in-a-bag1956/1#)

> This question is similar to [Unbounded Knapsack](https://github.com/Shreya549/last-minute-dsa/blob/main/Dynamic%20Programming/Unbounded-Knapsack.md)

## Input
| Variable Name | Data Type | Use | 
|---- | ----- | ----- |
| cost | int[] | Cost of 'i' kg packet |
| N | int | Maximum weight packet available |
| W | int | Weight of oranges to buy |

## Other Variables
| Variable Name | Data Type | Use | 
|---- | ----- | ----- |
| dp | int[][] | DP Matrix |
| i | int | To access rows of the matrix |
| j | int | To access columns of the matrix |

## Recursive Approach

```
def minimumCost(self, cost, N, W):
  if W==0:
      return 0
  if N==1:
      return cost[N-1] + self.minimumCost(cost, 1, W-1)
  if N<=W:
      return min(cost[N-1] + self.minimumCost(cost, N, W-N), self.minimumCost(cost, N-1, W))
  else:
      return self.minimumCost(cost, N-1, W)
 ```

## Top Down Approach

- DP Array is of int type
`dp[N+1][W+1]`

- Initialize DP with max int
```
for i in range(N+1):
    dp.append([10**7 + 7] * (W+1))

for i in range(N+1):
    dp[i][0] = 0

for j in range(W+1):
    if cost[0] > -1:
        dp[1][j] = cost[0] * j      
```
- Filling in the rest of the elements
```
for i in range(2, N+1):
  for j in range(1, W+1):
      if i<=j and cost[i-1] > -1:
          dp[i][j] = min(cost[i-1] +  dp[i][j-i], dp[i-1][j])

      else:
          dp[i][j] = dp[i-1][j]
```
- Answer
```
if dp[-1][-1] ==  10**7 + 7:
    return -1
return dp[-1][-1]
```

<p align="center">
	With :heart: by <a href="https://github.com/Shreya549" target="_blank">Shreya Chatterjee</a>
</p>

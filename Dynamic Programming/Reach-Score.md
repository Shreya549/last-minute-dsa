# Reach a given Score

> Consider a game where a player can score 3 or 5 or 10 points in a move. Given a total score n, find number of distinct combinations to reach the given score.

> [Link to the question](https://practice.geeksforgeeks.org/problems/reach-a-given-score-1587115621/1#)

## Input
| Variable Name | Data Type | Use | 
|---- | ----- | ----- |
| n | int | Target Score |

## Other variables
| Variable Name | Data Type | Use | 
|---- | ----- | ----- |
| dp | int[] | DP Array |

## Top Down Approach

- DP Array is of int type

`dp[n+1]`

- Initialization of DP Array

```
Arrays.fill(dp, 0);
dp[0] = 1;
```

- Filling up the remaining elements
```
for (int i = 3; i<=n; i++){
    dp[i] += dp[i-3];
}

for (int i = 5; i<=n; i++){
    dp[i] += dp[i-5];
}

for (int i = 10; i<=n; i++){
    dp[i] += dp[i-10];
}
```

- Answer
`dp[n]`

<p align="center">
	With :heart: by <a href="https://github.com/Shreya549" target="_blank">Shreya Chatterjee</a>
</p>

# Number of ways to partition a set - Bell Numbers

> Given a set of elements, find the number of ways to partition the set

> [Link to the question](https://www.geeksforgeeks.org/bell-numbers-number-of-ways-to-partition-a-set/)

## Example

```
Set => {1, 2, 3}
n = 3
 
All partitions -
  {1, 2, 3}
  {1}, {2, 3}
  {1, 2}, {3}
  {1, 3}, {2}
  {1}, {2}, {3}
  
Number of ways to partition - 5
```

## Input
| Variable Name | Data Type | Use | 
|---- | ----- | ----- |
| n | int | Number of elements |

## Approach

- The best approach is to build the [Bell Triangle](https://en.wikipedia.org/wiki/Bell_triangle)
```
1
1 2
2 3 5
5 7 10 15
```
- The first entry of each row is the last bell number
- All other entries are the summation of the previous entry and the entry just above the previous entry
```
1
1 (1+1 = 2)
2 (2+1 = 3) (3+2 = 5)
5 (5+2 = 7) (7+3 = 10) (10+5 = 15)
```
- The last element of each row is the nth Bell Number, where n = row number

## Top Down Approach

```
dp[n][n]
# Initialize matrix with 1

for i in range (1, n):
  for j in range (i+1):
    if j==0:
      # copy the last bell number
      dp[i][j] = dp[i-1][i-1]
      
    else:
      # sum up the previous entry and the entry just above the previous entry
      dp[i][j] = dp[i][j-1] + dp[i-1][j-1]
```

## Answer

` dp[-1][-1]`

<p align="center">
	With :heart: by <a href="https://github.com/Shreya549" target="_blank">Shreya Chatterjee</a>
</p>

     
    
    


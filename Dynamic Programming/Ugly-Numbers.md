# Ugly Numbers

> Ugly Numbers are those whose only prime factors are 2, 3, 5. Find the nth ugly number.
> [Link to the question](https://practice.geeksforgeeks.org/problems/ugly-numbers2254/1#)

> 1, 2, 3, 4, 5, 6, 8, 9 and so on are the first few ugly numbers

## Input
| Variable Name | Data Type | Use | 
|---- | ----- | ----- |
| n | int | To find the nth ugly number |

## Approach
 - Ugly numbers can be divided into 3 streams
 ```
   2 x 1, 2 x 2, 2 x 3, 2 x 4, 2 x 5, 2 x 6, 2 x 8, 2 x 9 ....
   3 x 1, 3 x 2, 3 x 3, 3 x 4, 3 x 5, 3 x 6, 3 x 8, 3 x 9 ....
   5 x 1, 5 x 2, 5 x 3, 5 x 4, 5 x 5, 5 x 6, 5 x 8, 5 x 9 ....
 ```
 
 - So basically, we are multiplying the ugly numbers by 2, 3 and 5 to get the next ugly numbers
 

## Other Variables
| Variable Name | Data Type | Use | 
|---- | ----- | ----- |
| dp | int[] | DP Array |
| i | int | To access the elements of the array|
| i2 | int | Index of multiple of 2|
| i3 | int | Index of multiple of 3|
| i4 | int | Index of multiple of 5|
| nx2 | int | Next multiple of 2|
| nx3 | int | Next multiple of 3|
| nx5 | int | Next multiple of 5|

## Top Down Approach

```
dp[n]

# DP to be initialized with 1

for i in range (1, n):
   dp[i] = min(nx2, nx3, nx5)

   if (dp[i] == nx2):
     i2 += 1
     nx2 = dp[i2] * 2

   if (dp[i] == nx3):
     i3 += 1
     nx3 = dp[i3] * 3

   if (dp[i] == nx5):
     i5 += 1
     nx5 = dp[i5] * 5
      
```

- Answer

`dp[-1]`

<p align="center">
	With :heart: by <a href="https://github.com/Shreya549" target="_blank">Shreya Chatterjee</a>
</p>

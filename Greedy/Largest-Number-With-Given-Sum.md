# Largest number with given sum

> Given N, number of digits and S, sum of digits. Form the maximum number with N digits and S as sum of digits.

> [Link to the question](https://practice.geeksforgeeks.org/problems/largest-number-with-given-sum-1587115620/1#)

## Input
| Variable Name | Data Type | Use | 
|---- | ----- | ----- |
| N | int | Number of digits |
| S | int | Sum of digits |

## Greedy Approach

- To get the maximum number, we need to set the digits from left to right
- If sum of digits is >= 9, we set the digit to 9 and reduce the sum
- Else we set the digit as sum and make sum as 0
- Repeat this N times
- If after N iterations, sum != 0, then return -1
- Else return the number formed

```
num = ""
for i in range(N):

  if S>9:
    num += "9"
    S -= 9
    
  else:
    num += S
    S = 0
    
if S != 0:
  return -1
  
else:
  return int(num)
```
  
<p align="center">
	With :heart: by <a href="https://github.com/Shreya549" target="_blank">Shreya Chatterjee</a>
</p>

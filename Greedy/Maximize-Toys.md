# Maximize Toys

> Given the cost of N toys and K depicting the amount with you. Your task is to find maximum number of toys you can buy with K amount. 

> [Link to the question](https://practice.geeksforgeeks.org/problems/maximize-toys0331/1#)

## Input
| Variable Name | Data Type | Use | 
|---- | ----- | ----- |
| N | int | Number of coins |
| arr[] | int Array | List of cost of N toys |
| K | int | Total Amount |
                         
## Greedy Approach
- Sort the cost array in ascending order
- Count the number of toys whose sum of costs <= K

```
A.sort()
cnt = 0
												 
for i in A:
	if i<=K:
		K -= i
		cnt += 1										 
	else:
		break

return cnt
```

<p align="center">
	With :heart: by <a href="https://github.com/Shreya549" target="_blank">Shreya Chatterjee</a>
</p>

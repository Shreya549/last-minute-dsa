# N meetings in one room 

> There is one meeting room in a firm. There are N meetings to be held. What is the maximum number of meetings that can be accommodated in the meeting room when only one meeting can be held in the meeting room at a particular time?

> [Link to the question](https://practice.geeksforgeeks.org/problems/n-meetings-in-one-room-1587115620/1)

## Input
| Variable Name | Data Type | Use | 
|---- | ----- | ----- |
| N | int | Number of meeting |
| S[] | int Array | List of start times of all meetings |
| F[] | int Array | List of finish times of all meetings |
                         
## Greedy Approach
- Sort the Meeting Times according to the Finish time

```
meeting = sorted(zip(F, S)) 
last = 0
count = 0
                         
for e,s in meeting:
  if s>last:
    last = e
    count+=1
                         
return (count)
```

<p align="center">
	With :heart: by <a href="https://github.com/Shreya549" target="_blank">Shreya Chatterjee</a>
</p>

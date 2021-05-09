# Reverse Level Order Traversal of a Binary Tree

> Given a tree, find its level order traversal i.e print the level order traversal starting from the innermost level

> [Link to the question](https://practice.geeksforgeeks.org/problems/reverse-level-order-traversal/1)

> This question uses [Level Order Recursive Approach](https://github.com/Shreya549/last-minute-dsa/main/Trees/Level-Order-Traversal.md)


## Input
| Variable Name | Data Type | Use | 
|---- | ----- | ----- |
| root | Node Class | Head node |

## Other variables
| Variable Name | Data Type | Use | 
|---- | ----- | ----- |
| q[] | Queue | Queue |
| st[] | Stack | Stack to store final nodes |

## Iterative Approach

- Enter each node into queue
- while queue is not empty
	- Dequeue the queue
	- Enqueue its right and then left child nodes into the queue 
	- Push dequeued node to stack
 - Pop the stack and print its nodes' values

```
q = [root]
st = []

while (q):
	temp = q.dequeue()
	if temp.right:
		q.enqueue(temp.right)
		
	if temp.left:
		q.enqueue(temp.left)
	
	st.append(temp.val)

return (st[::-1]) #reverse list => poping elements from stack
```

<p align="center">
	With :heart: by <a href="https://github.com/Shreya549" target="_blank">Shreya Chatterjee</a>
</p>

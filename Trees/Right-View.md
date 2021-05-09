# Right View of a Tree

> Given a tree, print its right view

> [Link to the question](https://leetcode.com/problems/binary-tree-right-side-view/)

> Uses [Level Order Traversal - Iterative Queue Method](https://github.com/Shreya549/last-minute-dsa/blob/main/Trees/Level-Order-Traversal.md)

> Similar to [Left-View of Tree - Iterative Approach](https://github.com/Shreya549/last-minute-dsa/blob/main/Trees/Left-View.md)


## Input
| Variable Name | Data Type | Use | 
|---- | ----- | ----- |
| root | Node Class (User Defined) | Head node |

## Other variables
| Variable Name | Data Type | Use | 
|---- | ----- | ----- |
| q | Queue | To store the level order traversal |


## Iterative Approach

- We need to print the last root of every level starting from the root node.
- We dequeue the root and check if the next element in the queue is a separator 
  - If it is, then we print the value of the root
- Enqueue its left and right child nodes.
- Using the iterative queue approach, we enqueue a separator (say, -1) to the queue to indicate that a level has been completed.

```
q = [root, -1]
ans = []

while q:
  temp = q.pop(0)

  if temp == -1:
    if not q:
      break
    q.append(-1)

  else:
    if temp:
       if q[0] == -1:
          ans.append(temp.val)

      if temp.left:
          q.append(temp.left)
      
      if temp.right:
          q.append(temp.right)

return ans
    
```




<p align="center">
	With :heart: by <a href="https://github.com/Shreya549" target="_blank">Shreya Chatterjee</a>
</p>

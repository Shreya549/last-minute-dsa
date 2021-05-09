# Left View of a Tree

> Given a tree, print its left view

> [Link to the question](https://practice.geeksforgeeks.org/problems/left-view-of-binary-tree/1)


## Input
| Variable Name | Data Type | Use | 
|---- | ----- | ----- |
| root | Node Class (User Defined) | Head node |

## Other variables
| Variable Name | Data Type | Use | 
|---- | ----- | ----- |
| maxlevel | int[] | Maximum level of the tree |
| level | int | Current level of the tree |


## Recursive Approach

- Calling the recursive function initially

```
def leftview(root):

  maxLevel = [0]
  printView(root, maxLevel, 1)
```


- The recursive function

```
def printView(root, maxLevel, level):

  if not root:
    return 
    
  if maxLevel[0] < level:
    
    print(root.data)
    maxLevel[0] = level
    
  printView(root.left, maxLevel, level + 1)  
  printView(root.right, maxLevel, level + 1)
```

## Iterative Approach
- This uses [Level Order Traversal - Iterative Queue Method](https://github.com/Shreya549/last-minute-dsa/blob/main/Trees/Level-Order-Traversal.md)

- We need to print the first root of every level starting from the root node.
- We dequeue the root and enqueue its left and right child nodes.
- Using the iterative queue approach, we enqueue a separator (say, -1) to the queue to indicate that a level has been completed.
- Upon reaching a separator, we print the value of the next node in the queue.

```
q = [-1, root]
ans = []

while (q):
  temp = q.pop(0)
  
  if temp == -1:
    if not q:
    break

    r = q.pop(0)
    q.append(-1)

    try:
      if r.left:
        q.append(r.left)
    except:
      pass

    try:
      if r.right:
        q.append(r.right)
    except:
      pass

    try:
      ans.append(r.data)
    except:
      pass

  else:
    if temp.left:
      q.append(temp.left)

    if temp.right:
      q.append(temp.right)

return ans
    
```




<p align="center">
	With :heart: by <a href="https://github.com/Shreya549" target="_blank">Shreya Chatterjee</a>
</p>

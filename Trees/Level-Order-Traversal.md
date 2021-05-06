# Level Order Traversal of a Binary Tree

> Given a tree, find its level order traversal

> [Link to the question](https://practice.geeksforgeeks.org/problems/level-order-traversal/1)

> This question uses [Height of a Binary Tree Problem](https://github.com/Shreya549/last-minute-dsa/blob/main/Trees/Height_of_Tree.md)


## Input
| Variable Name | Data Type | Use | 
|---- | ----- | ----- |
| root | Node Class | Head node |

## Other variables - Recursive
| Variable Name | Data Type | Use | 
|---- | ----- | ----- |
| h | int | Height of complete tree |
| i | int | Looping Variable |

## Other variables - Iterative
| Variable Name | Data Type | Use | 
|---- | ----- | ----- |
| q | Queue | Queue |
| ans | List | Level Order Traversal Answer |

## Recursive Approach

- Finding the height of the tree using [Height of a Binary Tree Problem](https://github.com/Shreya549/last-minute-dsa/blob/main/Trees/Height_of_Tree.md) and calling the recursive method

```
def level(root):
  
  h = height(root)
  
  for i in range(1, h+1):
    printRoot(root, i)
```

- Recursive Function

```
def printRoot(root, level):
    
    if not root:
      return
      
    if (level == 1):
      print(root.data)
      
    else:
      
      printRoot(root.left, level-1)
      printRoot(root.right, level-1)
```

## Iterative Approach

- Enter each node into queue
- while queue is not empty
	- Dequeue the queue
	- Enqueue its left and right child nodes into the queue 
	- Print the value of dequeued node

```
q = [root]
ans = []

while (q):
	temp = q.dequeue()
	if temp.left:
		q.enqueue(temp.left)
	if temp.right:
		q.enqueue(temp.right)
	
	ans.append(temp.val)

return (ans)
```

<p align="center">
	With :heart: by <a href="https://github.com/Shreya549" target="_blank">Shreya Chatterjee</a>
</p>

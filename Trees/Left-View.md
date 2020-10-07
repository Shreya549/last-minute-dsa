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
  printView(root.right, maxLevel, level - 1)
```

<p align="center">
	With :heart: by <a href="https://github.com/Shreya549" target="_blank">Shreya Chatterjee</a>
</p>

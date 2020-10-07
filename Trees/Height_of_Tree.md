# Height of a Binary Tree

> Given a tree, find its height

> [Link to the question](https://leetcode.com/problems/scramble-string/)


## Input
| Variable Name | Data Type | Use | 
|---- | ----- | ----- |
| root | Node Class | Head node |

## Other variables
| Variable Name | Data Type | Use | 
|---- | ----- | ----- |
| lheight | int | Height of left subtree |
| rheight | int | Height of right subtree |


## Recursive Approach

- Recursive function returns a boolean value

```
def height(root):

  if not root:
    return 0
  
  lheight = height(root.left)
  rheight = height(root.right)
  
  if (lheight > rheight):
    return lheight + 1
    
  return rheight + 1
```


<p align="center">
	With :heart: by <a href="https://github.com/Shreya549" target="_blank">Shreya Chatterjee</a>
</p>

# Check for BST

> Given a tree, check if it is a Binary Search Tree

> [Link to the question](https://practice.geeksforgeeks.org/problems/check-for-bst/1)


## Input
| Variable Name | Data Type | Use | 
|---- | ----- | ----- |
| root | Node Class (User Defined) | Head node |

## Other variables
| Variable Name | Data Type | Use | 
|---- | ----- | ----- |
| mini | int | Minimum value of a node |
| maxi | int | Maximum value of a node |


## Recursive Approach

- We define a range of values that a node can take, mini and maxi
- If node does not exist then it forms a BST
- If value of the node is not in the range then it is not a BST
- We recursively check this for left and right subtree

- Calling the recursive function initially

```
def checkBST(root):

  mini = -4999999999
  maxi = 4999999999
  return check(root, mini, maxi)
```


- The recursive function

```
def check(root, mini, maxi):

  if not root:
    return True
    
  if root.data < mini or root.data > maxi:
    return False
    
  return check(root.left, mini, root.data - 1) and check(root.right, root.data + 1, maxi)
```

<p align="center">
	With :heart: by <a href="https://github.com/Shreya549" target="_blank">Shreya Chatterjee</a>
</p>

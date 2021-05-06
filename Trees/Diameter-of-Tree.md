# Diameter of a Binary Tree

> Given a tree, find its diameter

> [Link to the question](https://practice.geeksforgeeks.org/problems/diameter-of-binary-tree/1)

> This question uses [Height of a Binary Tree Problem](https://github.com/Shreya549/last-minute-dsa/blob/main/Trees/Height_of_Tree.md)

## Input
| Variable Name | Data Type | Use | 
|---- | ----- | ----- |
| root | Node Class | Head node |

## Recursive Approach
- maximum (height(left_subtree) + height(right_subtree) + 1, diameter(left_subtree), diameter(right_subtree)

```
def diameter(root):

  if root == None:
    return 0
  
  leftHeight = height(root.left)
  rightHeight = height(root.right)
  
  leftDia = diameter(root.left)
  rightDia = diameter(root.right)
  
  return max(leftHeight + rightHeight + 1, leftDia, rightDia)
```

<p align="center">
	With :heart: by <a href="https://github.com/Shreya549" target="_blank">Shreya Chatterjee</a>
</p>

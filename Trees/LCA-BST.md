# Lowest Common Ancestor in a Binary Search Tree

> Given a BST and 2 values of nodes, find the lowest common ancestor of the 2 nodes

> [Link to the question](https://practice.geeksforgeeks.org/problems/lowest-common-ancestor-in-a-bst/1#)

## Input
| Variable Name | Data Type | Use | 
|---- | ----- | ----- |
| root | Node Class (User Defined) | Head node |

## Recursive Approach
- If both the values are less than the given root node, check in the left subtree
- If both the values are more than the given root node, check in the right subtree
- Else return root node

```
if n1>root.data and n2>root.data:
    return LCA(root.right, n1, n2)

elif n1<root.data and n2<root.data:
    return LCA(root.left, n1, n2)

return root
```

<p align="center">
	With :heart: by <a href="https://github.com/Shreya549" target="_blank">Shreya Chatterjee</a>
</p>


# Post-Order Traversal of a Binary Tree

> Given a tree, find its post-order traversal using recursion

> [Link to the question](https://www.geeksforgeeks.org/tree-traversals-inorder-preorder-and-postorder/)

### Algorithm Postorder(tree)
   1. Traverse the left subtree, i.e., call Postorder(left-subtree)
   2. Traverse the right subtree, i.e., call Postorder(right-subtree)
   3. Visit the root.

## Input
| Variable Name | Data Type | Use | 
|---- | ----- | ----- |
| root | Node Class | Head node |

```
def printPostorder(root): 
  
    if root: 
        printPostorder(root.left) 
        printPostorder(root.right) 
        print(root.val)
```

# Pre-Order Traversal of a Binary Tree

> Given a tree, find its pre-order traversal using recursion

> [Link to the question](https://www.geeksforgeeks.org/tree-traversals-inorder-preorder-and-postorder/)

### Algorithm Preorder(tree)
   1. Visit the root.
   2. Traverse the left subtree, i.e., call Preorder(left-subtree)
   3. Traverse the right subtree, i.e., call Preorder(right-subtree)

## Input
| Variable Name | Data Type | Use | 
|---- | ----- | ----- |
| root | Node Class | Head node |

```
def printPreorder(root): 
  
    if root: 
  
        print(root.val), 
  
        printPreorder(root.left) 
  
        printPreorder(root.right) 
```

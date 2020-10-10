# In-Order Traversal of a Binary Tree

> Given a tree, find its in-order traversal using recursion

> [Link to the question](https://www.geeksforgeeks.org/tree-traversals-inorder-preorder-and-postorder/)

### Algorithm Inorder(tree)
   1. Traverse the left subtree, i.e., call Inorder(left-subtree)
   2. Visit the root.
   3. Traverse the right subtree, i.e., call Inorder(right-subtree)
   
## Input
| Variable Name | Data Type | Use | 
|---- | ----- | ----- |
| root | Node Class | Head node |

```
def printInorder(root): 
  
    if root: 
  
        printInorder(root.left) 
  
        print(root.val), 
 
        printInorder(root.right) 
  
```

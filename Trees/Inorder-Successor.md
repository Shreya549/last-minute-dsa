# Inorder Successor of a Binary Search Tree

> Given a binary search tree root containing unique values, and an integer t, return the value of the inorder successor of t. That is, return the smallest value greater than t in the tree.

> [Link to the question](https://binarysearch.com/problems/Inorder-Successor)

## Input
| Variable Name | Data Type | Use | 
|---- | ----- | ----- |
| root | Tree Class (User Defined) | Head node |
| t | int | target |

## Other variables
| Variable Name | Data Type | Use | 
|---- | ----- | ----- |
| prev | Tree Class (User Defined) | To store the next node in Inorder Traversal |

## Solution

- Find the target node while storing the next node in Inorder Traversal
  - Iterate in the tree
    - If the node > target
      - prev = node
      - node = node.left
    - If the node < target
      - node = node.right
    - Else break
- Find the successor of the target node
  - Go to right node
  - Then go to extreme left node
  - return the node
- If returned node is null
  - return prev.val
- Else return returned node.val

```
public Tree find(Tree root){
    if (root == null)
    return null;

    Tree right = root.right;
    if (right ==null)
    return right;

    while (right.left!=null){
        right = right.left;
    }

    return (right);
}

public int solve(Tree root, int t) {

    Tree prev = root, node = root;
    while (node !=null){
        if (node.val > t)
        {
            prev = node;
            node = node.left;
        }

        else if (node.val < t)
        {
            node = node.right;
        }

        else
        break;
    }

    if (node == null)
    return -1;

    Tree succ = find(node);
    if (succ == null)
    return prev.val;
    return (succ.val);
}
```


<p align="center">
	With :heart: by <a href="https://github.com/Shreya549" target="_blank">Shreya Chatterjee</a>
</p>


 

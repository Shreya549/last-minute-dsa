# Connect Nodes at Same Level

> Given a tree, connect the nodes at same level

> [Link to the question](https://practice.geeksforgeeks.org/problems/connect-nodes-at-same-level/1#)

> We will be modifying the [Level Order Traversal](https://github.com/Shreya549/last-minute-dsa/blob/main/Trees/Level-Order-Traversal.md) to solve this.

## Input
| Variable Name | Data Type | Use | 
|---- | ----- | ----- |
| root | Node Class (User Defined) | Head node |

## Other variables
| Variable Name | Data Type | Use | 
|---- | ----- | ----- |
| q | Queue | To store the level order traversal |

## Iterative Method

- Store the level order traversal using a separator
- while traversing, if you encounter a node, check if the next element in the queue is -1:
  - if -1, then make the nextRight pointer as NULL
  - else, make the nextRight pointer as the next element in the queue

```
q = [-1, root]
        
while (q):
    t = q.pop(0)
    if t == -1:
        if not q:
            break
        q.append(-1)

    else:
        if q[0] == -1:
            t.nextRight = None

        else:
            t.nextRight = q[0]

        if t.left:
            q.append(t.left)

        if t.right:
            q.append(t.right)
```

<p align="center">
	With :heart: by <a href="https://github.com/Shreya549" target="_blank">Shreya Chatterjee</a>
</p>

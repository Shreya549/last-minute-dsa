# Bottom View of a Tree

> Given a tree, print its bottom view

> [Link to the question](https://practice.geeksforgeeks.org/problems/bottom-view-of-binary-tree/1#)

> We will be modifying the [Level Order Traversal](https://github.com/Shreya549/last-minute-dsa/blob/main/Trees/Level-Order-Traversal.md) to solve this.


## Input
| Variable Name | Data Type | Use | 
|---- | ----- | ----- |
| root | Node Class (User Defined) | Head node |

## Other variables
| Variable Name | Data Type | Use | 
|---- | ----- | ----- |
| q | Queue | To store the level order traversal |

## Iterative Approach

- Create a tuple of the horizontal distance of the root from the root (0) and enqueue the queue
- Dequeue the queue and enqueue 2 tuples
  - Left Node and distance of the dequeued root - 1
  - Right Node and distance of the dequeued root + 1
- Create a hashmap (or dictionary) of the horizontal distance of the root and its value

```
q = [(root, 0)]

d = {}
d[0] = root.data

while q:
    temp = q.pop(0)
    troot = temp[0]
    tlevel = temp[1]

    if troot.left:
        llevel = tlevel-1
        lroot = troot.left

        q.append((lroot, llevel))
        d[llevel] = lroot.data

    if troot.right:
        rlevel = tlevel + 1
        rroot = troot.right

        q.append((rroot, rlevel))
        d[rlevel] = rroot.data

arr = []
for i in sorted(d.keys()):
    arr.append(d[i])

return arr
```

<p align="center">
	With :heart: by <a href="https://github.com/Shreya549" target="_blank">Shreya Chatterjee</a>
</p>

# Top View of a Tree

> Given a tree, print its top view

> [Link to the question](https://practice.geeksforgeeks.org/problems/top-view-of-binary-tree/1)

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
- If key (horizontal distance) does not exist then create a key and make its values as the node's value

```
q = [(root, 0)]

d = {}
d[0] = root.data

while q:
    temp = q.pop(0)
            
    rt = temp[0]
    lvl = temp[1]

    if rt.left:
        q.append((rt.left, lvl-1))

        if lvl-1 in d.keys():
            pass
        else:
            d[lvl-1] = rt.left.data

    if rt.right:
        q.append((rt.right, lvl+1))

        if lvl+1 in d.keys():
            pass
        else:
            d[lvl+1] = rt.right.data

arr = []
for i in sorted(d.keys()):
    arr.append(d[i])

return arr
```

<p align="center">
	With :heart: by <a href="https://github.com/Shreya549" target="_blank">Shreya Chatterjee</a>
</p>

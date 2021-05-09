# Vertical Traversal of a Tree

> Given a tree, print its vertical traversal

> [Link to the question](https://practice.geeksforgeeks.org/problems/print-a-binary-tree-in-vertical-order/1)

> We will be modifying the [Level Order Traversal](https://github.com/Shreya549/last-minute-dsa/blob/main/Trees/Level-Order-Traversal.md) and [Bottom View](https://github.com/Shreya549/last-minute-dsa/blob/main/Trees/Bottom-View.md) to solve this.


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
- Create a hashmap (or dictionary) of the horizontal distance of the root and list of values at that distance

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
        
        try:
          d[llevel].append(lroot.data)
        except:
          d[llevel] = [lroot.data]
        
    if troot.right:
        rlevel = tlevel + 1
        rroot = troot.right

        q.append((rroot, rlevel))
        d[rlevel] = rroot.data
        
        try:
          d[rlevel].append(rroot.data)
        except:
          d[rlevel] = [rroot.data]

ans = []
for i in sorted(d.keys()):
    for j in d[i]:
      ans.append(j)

return ans
```

<p align="center">
	With :heart: by <a href="https://github.com/Shreya549" target="_blank">Shreya Chatterjee</a>
</p>

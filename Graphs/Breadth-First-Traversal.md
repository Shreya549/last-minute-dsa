# Breadth First Traversal

> Given a graph, find its Breadth First Traversal

> [Link to the question](https://practice.geeksforgeeks.org/problems/bfs-traversal-of-graph/1)

> Uses the concept of queues

## Input Variables
| Variable Name | Data Type | Use | 
|---- | ----- | ----- |
| V | int | Number of Nodes |
| graph| Dictionary | Graph |

## Other Variables
| Variable Name | Data Type | Use | 
|---- | ----- | ----- |
| q[] | Queue | To store the nodes |
| visited[] | Boolean Array | To check if the node has been previously visited or not |

## Iterative Approach

- Enqueue the first node to the queue and mark it as visited
- Traverse in the queue
  - Dequeue the queue
  - Print the node
  - Enqueue its connected nodes to the queue
  - Mark the connected nodes as visited

```
q = []
visited = [False] * V

bfs = []
q.append(0)
visited[0] = True

while q:
  s = q.pop(0)
  bfs.append(s)
  
  for i in graph[s]:
    if visited[i] == False:
        q.append(i)
        visited[i] = True

return bfs
```

<p align="center">
	With :heart: by <a href="https://github.com/Shreya549" target="_blank">Shreya Chatterjee</a>
</p>


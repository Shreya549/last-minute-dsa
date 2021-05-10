# Depth First Traversal

> Given a graph, find its Depth First Traversal

> [Link to the question](https://practice.geeksforgeeks.org/problems/depth-first-traversal-for-a-graph/1)

> Uses the concept of stacks

## Input Variables
| Variable Name | Data Type | Use | 
|---- | ----- | ----- |
| V | int | Number of Nodes |
| graph| Dictionary | Graph |

## Other Variables
| Variable Name | Data Type | Use | 
|---- | ----- | ----- |
| visited() | int set() | To store the set of visited nodes |

## Recursive Approach

- Call a recursive function with the set of visited nodes
- For each node check if the node has been visited
  - if not visited, print the value and check its connected nodes
  - if the connected node is not visited, call the recursive function for the connected node

- Calling the recursive function initially

```
def dfsRoot(V, graph):
  visited = set()
  ans = []
  dfs(0, graph, visited, ans)
  
  return ans
```

- The recursive function

```
def dfs(self, v, graph, visited, ans):

  visited.add(v)
  ans.append(v)

  for i in graph[v]:
      if i not in visited:
          dfs(i, graph, visited, ans)
```

<p align="center">
	With :heart: by <a href="https://github.com/Shreya549" target="_blank">Shreya Chatterjee</a>
</p>

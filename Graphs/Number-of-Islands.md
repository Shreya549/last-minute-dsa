# Number of Islands

> Given a  grid which represents a map of '1's (land) and '0's (water), return the number of islands.

> [Link to the question](https://leetcode.com/problems/number-of-islands/)

> Partial application of [Breadth first Traversal](https://github.com/Shreya549/last-minute-dsa/blob/main/Graphs/Breadth-First-Traversal.md)

## Input Variables
| Variable Name | Data Type | Use | 
|---- | ----- | ----- |
| grid | char[][] | Map of '0' and '1' |
| rows | int | Number of rows of the grid |
| cols| int | Number of columns of the grid |

## Other Variables
| Variable Name | Data Type | Use | 
|---- | ----- | ----- |
| lands[][] | int[][] | List of coordinates of the lands
| q[] | Queue | To store the connected nodes |
| visited[][] | Boolean Grid | To store if the corresponding area in the grid has been visited or not |

## Iterative Approach

- Initialize the visited matrix as False
- Store the coordinates of land in a list
- Iterate in the list
  - If the area has been visited, then continue
  - Else enqueue it to a queue, mark it as visited, and increment the count
  - Iterate over the queue until it is not empty
    - Dequeue the queue
    - Check for all neighbours
    - If they are not visited then mark it as visited and enqueue the queue

## Initializing the visited grid
```
visited = []
for i in range(rows):
    visited.append([False] * cols)
```

## Creating the lands list
```
lands = []
for i in range(rows):
    for j in range(cols):
        if grid[i][j] == '1':
            lands.append((i,j))
```

## Finding the count of the connected islands
```
q = []
count = 0

for land in lands:
    i = land[0]
    j = land[1]
    
    if visited[i][j] == True:
        continue

    # print(land)
    visited[i][j] = True
    count +=1 

    q.append((i,j))

    while q:
        area = q.pop(0)

        i = area[0]
        j = area[1]                

        if i-1>=0:
            if grid[i-1][j] == '1':
                if visited[i-1][j] == False:
                    q.append((i-1, j))
                    visited[i-1][j] = True

        if j-1 >=0:                
            if grid[i][j-1] == '1':
                if visited[i][j-1] == False:
                    q.append((i, j-1))
                    visited[i][j-1] = True

        if j+1 <cols:
            if grid[i][j+1] == '1':
                if visited[i][j+1] == False:
                    q.append((i, j+1))
                    visited[i][j+1] = True

        if i+1<rows:
            if grid[i+1][j] == '1':
                if visited[i+1][j] == False:
                    q.append((i+1, j))
                    visited[i+1][j] = True
return count   
```

<p align="center">
	With :heart: by <a href="https://github.com/Shreya549" target="_blank">Shreya Chatterjee</a>
</p

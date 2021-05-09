# Spiral Level Order Traversal of a Tree

> Given a tree, print its spiral level order traversal

> [Link to the question](https://practice.geeksforgeeks.org/problems/level-order-traversal-in-spiral-form/1#)

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

- Store the level order traversal in a list using a separator for each level

```
q = [-1, root]
ans = []

while q:
    temp = q.pop(0)
    if temp == -1:
        if not q:
            break
        q.append(-1)
        ans.append(-1)

    else:
        try:
            if temp.left:
                q.append(temp.left)
        except:
            pass

        try:  
            if temp.right:
                q.append(temp.right)
        except:
            pass

        try:
            ans.append(temp.data)
        except:
            pass
```

## Printing the list

- Initialize count as 1
- Ignore the first element in the ans list as it is -1
- Append -1 to the end of the list
- If the value is not -1, store it in a temp list
- If value is -1 
  - if count of -1 is odd then reverse the temp list and append in final answer
  - else append the temp list in final answer
  - empty the temp list and increment count
  
```
ans.append(-1) 
st = []
c = 1
arr = []

for i in ans[1:]:
    if i>-1:
        st.append(i)
    else:
        if c%2==0:
            arr+=st
        else:
            arr+=st[::-1]

        st = []
        c +=1
        
return arr
```

<p align="center">
	With :heart: by <a href="https://github.com/Shreya549" target="_blank">Shreya Chatterjee</a>
</p>

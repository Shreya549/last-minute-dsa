# Next Smallest Element Problem

> [Link to the question](https://www.geeksforgeeks.org/next-smaller-element/)

> This question is a variation of [Next-Greater-Element](https://github.com/Shreya549/last-minute-dsa/blob/main/Stacks/Next-Greater-Element.md)

## Input

| Variable Name | Data Type | Use                             |
| ------------- | --------- | ------------------------------- |
| n             | int       | Number of elements in the array |
| s             | int[]     | Elements of array               |

## Other variables

| Variable Name | Data Type | Use                |
| ------------- | --------- | ------------------ |
| st            | int[]     | Temporary stack    |
| ans           | int[]     | Final answer array |

## Stack Approach

```
for i in range(n-1,-1,-1):
    if(len(st)==0):
        ans.append(n)
    elif(st[len(st)-1]<s[i]):
        ans.append(stind[len(stind)-1])
    else:
        while(len(st)>0 and st[len(st)-1]>=s[i]):
            st.pop()
        if(len(st)==0):
            ans.append(n)
        else:
            ans.append(stind[len(stind)-1])
        st.append(s[i])
```

- Answer

`ans[::-1]`

<p align="center">
	With :heart: by <a href="https://github.com/RajatSablok" target="_blank">Rajat Sablok</a>
</p>

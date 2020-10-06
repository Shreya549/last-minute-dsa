# Next Greatest Element Problem

> [Link to the question](https://www.geeksforgeeks.org/next-greater-element/)

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
        ans.append(-1)
    elif(st[len(st)-1]>s[i]):
        ans.append(st[len(st)-1])
    else:
        while(len(st)>0 and st[len(st)-1]<=s[i]):
            st.pop()
        if(len(st)==0):
            ans.append(-1)
        else:
            ans.append(st[len(st)-1])
    st.append(s[i])
```

- Answer

`ans[::-1]`

<p align="center">
	With :heart: by <a href="https://github.com/RajatSablok" target="_blank">Rajat Sablok</a>
</p>

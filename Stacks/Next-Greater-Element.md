# Subset Sum Problem

> [Link to the question](https://www.geeksforgeeks.org/next-greater-element/)

## Input

| Variable Name | Data Type | Use                             |
| ------------- | --------- | ------------------------------- |
| t             | int       | Number of test cases            |
| n             | int       | Number of elements in the array |
| s             | int[]     | Elements of array               |

## Other variables

| Variable Name | Data Type | Use                |
| ------------- | --------- | ------------------ |
| st            | int[]     | Temporary stack    |
| ans           | int[]     | Final answer array |

## Stack Approach

```
t = int(input())
for _ in range(t):
    n = int(input())
    s = input().split()
    s = [int(i) for i in s]
    st = []
    ans = []
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
    ans=ans[::-1]
    for i in ans:
        print(i,end=' ')
    print()
```

<p align="center">
	With :heart: by <a href="https://github.com/Shreya549" target="_blank">Shreya Chatterjee</a>
</p>

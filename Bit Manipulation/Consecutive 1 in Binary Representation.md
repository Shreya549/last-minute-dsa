Length of the Longest Consecutive 1s in Binary Representation

> Example
```
num = 222
binary_equivalent = 1101 1110
ans = 4
```

> Find num<<1
```
mask = 1011 1100
```

> num & (num << 1)
```
num  = 1101 1110
           &
mask = 1011 1100
-----------------
num =  1100 1110
```

> Increment count
> Repeat until num = 0

## Algorithm

```
while (num>0)
  num = num & (num << 1)
  count++
```

<p align="center">
	With :heart: by <a href="https://github.com/Shreya549" target="_blank">Shreya Chatterjee</a>
</p>

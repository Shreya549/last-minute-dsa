# Count number of Set Bits in the binary equivalent of a number

> Example
```
num = 56
binary_equivalent = 0011 1000
ans = 3
```

## Find the right most set bit mask

> Example
```
num  = 0011 1000
mask = 0000 1000
```

> Find 2's complement of the number
```
num  = 0011 1000
~num = 1100 0111
          + 1
2's  = 1100 1000
```

> Find mask
```
num  = 0011 1000
           &
2's  = 1100 1000
-----------------
mask = 0000 1000
```

> `mask = num & (-num)`

## Kernighan's Algorithm

```
num  = 0011 1000
           -
mask = 0000 1000
-----------------
num  = 0011 0000

counter = 1

num  = 0011 0000
           -
mask = 0001 0000
-----------------
num  = 0010 0000

counter = 2

num  = 0010 0000
           -
mask = 0010 0000
-----------------
num  = 0000 0000

counter = 2
```

## Final Solution

```
counter = 0
while (num > 0):
  mask = num & (-num)
  num = num - mask
  counter = counter + 1

return counter
```

<p align="center">
	With :heart: by <a href="https://github.com/Shreya549" target="_blank">Shreya Chatterjee</a>
</p>

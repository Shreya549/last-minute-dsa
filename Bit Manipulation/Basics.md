# Basics of Bit Manipulation

## AND operator - &

- a & 0 : 0
- a & 1 : a

## OR operator - |

- a | 1 : 1
- a | 0 : a

## NOT operator - ~

> Toggles the bit
- 0 : 1
- 1 : 0

## XOR operator - 

- a ^ 0 : a
- a ^ 1 : ~a

## Turn ith bit on

```
i = 4
a    = 1000 1100
           |
mask = 0001 0000
-------------------
ans  = 1001 1100 
```

```
mask = (1<<i)
ans = *a | mask)
```

## Turn ith bit off

```
i = 4
a    = 1001 1100
           &
mask = 1110 1111
-------------------
ans  = 1000 1100 
```

```
mask = (1<<i)
mask = (~mask)
ans = (a & mask)
```

## Toggle ith bit

```
i = 4
a    = 1000 1100
           ^
mask = 0001 0000
-------------------
ans  = 1001 1100 
```

```
mask = 1<<i
ans = a ^ mask
```

## Check if ith bit is on or off

```
i = 4
a    = 1000 1100
           &
mask = 0001 0000
-------------------
ans  = 0000 0000

i = 4
a    = 1001 1100
           &
mask = 0001 0000
-------------------
ans  = 0001 0000
```

```
mask = 1<<i
ans = a & mask

if ans == 0:
    return "ON"
    
else:
    return "OFF
```





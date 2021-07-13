# Given a list of numbers occuring in pairs containing a single unique number, find that number

## Algorithm
- Find the xor of all numbers
- Number occuring in pairs will have their xor = 0
- You will be left with only the unique number

> Solution

```
arr = {1, 3, 2, 4, 2, 3, 1}
int xor = 0;

for (int i = 0; i<7; i++)
{
  xor = xor ^ arr[i];
}

return xor;
```
<p align="center">
	With :heart: by <a href="https://github.com/Shreya549" target="_blank">Shreya Chatterjee</a>
</p> 

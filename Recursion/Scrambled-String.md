# Scrambled String

> Given 2 strings, check if they are scrambled strings of each other

> [Link to the question](https://leetcode.com/problems/scramble-string/)


## Input
| Variable Name | Data Type | Use | 
|---- | ----- | ----- |
| s1 | String | First string |
| n1 | int | Length of first string |
| s2 | String | Second string |
| n2 | int | Length of second string |

## Other variables
| Variable Name | Data Type | Use | 
|---- | ----- | ----- |
| i | int | Looping variables |


## Recursive Approach

- Recursive function returns a boolean value

```
def scrambled(s1, s2)
```

- Before calling the recursive function we would optimize it by using these checks

  - Strings of unequal length cannot be scrambled strings
  ```
  if len(s1) != len(s2):
    return False
  ```
  
   - Null Strings are scrambled strings of each other
   
   ``` 
   if not len(s1):
    return True
   ```
   
   - Equal strings are scrambled strings of each other
   
   ```
   if (s1==s2):
    return True
    ```
    
    - If the two strings are not anagrams of each other, they cannot be scrambled too
    
    ```
    if sorted(s1) != sorted(s1):
      return False
      
    ```
 - Recursive function call
  
```
for i in range (1, n):

  if scrambled(s1[:i], s2[:i]) and scrambled(s1[i:], s2[i:]):
    return True
    
  if scrambled(s1[-1:], s2[:i]) and scrambled(s1[:-1], s2[i:]):
     return True
     
return False
 
```

- Answer

`scrambled(s1, s2)`

<p align="center">
	With :heart: by <a href="https://github.com/Shreya549" target="_blank">Shreya Chatterjee</a>
</p>

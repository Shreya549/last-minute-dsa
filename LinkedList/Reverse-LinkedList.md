# Reverse a Linked List

> Given the head pointer, reverse the Linked List

> [Link to the question](https://leetcode.com/problems/reverse-linked-list/)

## Input Variables
| Variable Name | Data Type | Use | 
|---- | ----- | ----- |
| head | Node | head Node |

## Iterative Approach

```
curr = head
next = null
prev = null

while (curr != null)
  next = curr.next
  curr.next = prev
  prev = curr
  curr = next
  
return (prev)
```

## Recursive Approach

```
def solve(head):
  
  if head == null or head.next == null:
    return null
    
  rest = solve(head.next)
    
  head.next.next = head
  head.next = rest
  
  return (rest)
```

<p align="center">
	With :heart: by <a href="https://github.com/Shreya549" target="_blank">Shreya Chatterjee</a>
</p

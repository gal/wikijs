---
title: Stack
description: 
published: true
date: 2021-01-11T12:48:07.283Z
tags: 
editor: markdown
dateCreated: 2021-01-11T12:18:31.307Z
---

# Stack

LIFO ADT

A stack is a collection of objects where
- we take items from the top
- we add items to the top

Stacks are useful for many things
- Undo in a text editor
- 'back' button on a ui
- languages are implemented using a stack of active function calls
- arithmetic notations without need for brackets like on calculators ( postfix notation )
- reversing a sequence of input ( push everything to stack, pop everything from it )

## Postfix with a Stack

$35 + 2 *$
resolves to
$2 * 5 + 3$

- If you read a number, push it to top of the stack
- If you read an operator, push pop the top of the stack as the 2nd term. Pop the next top off the stack as the 1st term. Compute the result and push to stack

3, 5 get pushed to stack. '+' is read. 5 gets popped off as first operand, 3 gets popped off as second operand. Result 8 is pushed to stack.

2 gets pushed to stack. * is read, 2 is popped off as first operand, 8 is popped off as second operand

```py
class Stack:
	def __init__(self):
  	self.alist = []
  def push(self, ele):	# O(1) on average
  	self.alist.append(ele)
  def pop(self):				# O(1) on average 
  	if len(alist) == 0:
    	return None
    return self.alist.pop()
  def top(self):				# O(1) on average
  	if len(self.alist) == 0:
    	return None
    return self.alist[-1]
  def length(self):			# O(1)
  	return len(self.alist)
```
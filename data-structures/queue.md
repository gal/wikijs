---
title: Queue
description: 
published: true
date: 2021-01-11T12:36:29.703Z
tags: 
editor: markdown
dateCreated: 2021-01-11T12:36:29.703Z
---

# Queue

FIFO ADT

## Examples:
- TCP packets
- i/o buffers are queued
- pathing algorithms maintain a queue of edges to explore
- grid and cloud computing maintain a queue of requests

## Methods

`enqueue` add an item to the queue
`dequeue` remove and return item in the queue waiting the longest
`front` 	return the item in the queue waiting the longest
`length` 	return the length

## Implementation details

- Using a primitive list is inefficient as removing from the front would cause all the following elements to be copied to their previous index

- Instead, maintain a reference to the head of the queue, called `head`
- To dequeue, return the element pointed to by `head` and set that index's element to `None`

- Problem --> will cause a data leak, as will continue allocating memory to increase the list size

Fix:
- When we reach the end of the list, wrap around to the start again, instead of having python allocate more memory by extending the list
- Only expand the list when all cells have been filled
- We now need a `tail` as well as a `head`
- When we do this, we will have to reorder everything, so that the head is at the start of the list and the tail is at the end to maintain cohesion

![queue-reorder.png](/queue-reorder.png)

```py
class Queue:
	def __init__(self):
  	self.body = [None]*STARTING_LEN_OF_LIST
    self.head = 0
    self.tail = 0 # index of next enqueued item
    self.size = 0

def enqueue(self, item):
	if self.size == 0:
  	self.body[0] = item
    self.size = 1
    self.tail = 1
  else:
  	self.body[self.tail] = item
    self.size += 1
    if self.size == len(self.body) # list is now full
    	self.grow()
    elif self.tail == len(self.body) - 1:	# no room at end, but is room at front
    	self.tail = 0
    else:
    	self.tail += 1
  
  def dequeue(self):
  	if self.size == 0:
    	return None
    	
    
    
    
    
    
    
    
```






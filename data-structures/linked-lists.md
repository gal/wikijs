---
title: Linked Lists
description: 
published: true
date: 2021-01-12T14:09:23.753Z
tags: 
editor: markdown
dateCreated: 2021-01-12T13:24:34.769Z
---

# Linked Lists

Non-contiguous list-based data structure
- allows for data to be allocated in smaller chunks, meaning data is stored more efficiently.
- must follow references to memory addresses to iterate through the list, more costly to iterate

## Implementing a Stack
- Singly-linked list behaves like a stack, so its easy to implement a stack using an adt --> insert to front of linked-list, and pop from front too --> no need to iterate through whole linked list
- All these operations would be O(1)

# Doubly-Linked List

- Has a pointer to each node's parent
- To make it easy, add a 'dummy' head and tail that have a 'None' parent or child ( depending on whether they are head or tail )
- 

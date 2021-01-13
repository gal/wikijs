---
title: Map ADT
description: 
published: true
date: 2021-01-13T08:51:00.688Z
tags: 
editor: markdown
dateCreated: 2021-01-13T08:51:00.688Z
---

# Map ADT

- A dictionary or *map* is a key,value store that should have constant ( O(1) ) lookup time
- Unique keys

# How to Implement

| |get(item(k)|contains()|setitem(k,v)|delitem()|build full map|
|-|-|-|-|-|-|
|unsorted list|O(n)|O(n)|O(n)|O(n)|$O(n^2)$|
|sorted list|O(log n)|O(log n)|O(n)|O(n)|$O(n^2)$|
|AVL tree|O(log n)|O(log n)|O(log n)|O(log n)|O(n log n)|
|Hash table|O(1)|O(1)|O(1)|O(1)|O(n)|
|||||||

# Hash Table

## Hash Table

- Builtin `hash()` function converts any object into an integer
- Hash values must remain the same, and the key in the lookup function must be the same as the key in the hashtable

## Compression

Once we have a hash value, we need to decide a location within our list

Suppose our list has N cells:
- our index must be in the range [0, n-1]

Suppose our key has a hash of h

`location(k) = h % N`

Determining this location is O(1) for any list size




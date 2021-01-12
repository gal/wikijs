---
title: Priority Queue
description: 
published: true
date: 2021-01-12T15:14:22.893Z
tags: 
editor: markdown
dateCreated: 2021-01-12T15:14:22.893Z
---

# Priority Queue

- Like a queue, but higher-priority elements are faster to access

![data--structures-priority-queue-methods.png](/data--structures-priority-queue-methods.png)

- Could use sorted/unsorted lists, or doubly-linked lists
	- Unsorted are very innefficient, as the minimum priority `key` is how it's sorted

- Could use an AVL --> very efficient

| |add(k,v)|min()|remove_min()|length()|build full PQ|
|-|-|-|-|-|-|
|unsorted list|O(1) (append)|O(n)|O(n)|O(1)|O(n)|
|unsorted DLL|O(1)|O(n)|O(n)|O(1)|O(n)|
|sorted list|O(n)|O(1)|O(1) (remove end)|O(1)|O($n^2$)|
|sorted DLL|O(n)|O(1)|O(1)|O(1)|O($n^2$)|
|AVL tree|O(log n)|O(log n)|O(log n)|O(1)|O(n log n)|


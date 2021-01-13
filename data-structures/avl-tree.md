---
title: AVL Tree
description: 
published: true
date: 2021-01-13T08:28:57.650Z
tags: 
editor: markdown
dateCreated: 2021-01-12T22:58:14.429Z
---

# AVL Tree

- A binary search tree's height impacts search time, as the complexity is O(m) where m = height of tree
- An AVL is designed so that it keeps the height of the tree as small as possible by rebalancing the tree on every mutation.
- It rebalances through a series of rotations

# How to rotate
![data-structures-avl-rotation.png](/data-structures-avl-rotation.png)

# When to Rotate

	Balance Factor = height(left-subtree) - height(righ-subtree)
If balance factor is not in the range [-1,1], rotate on that node

![datat-structures-avl-when-to-rotate.png](/datat-structures-avl-when-to-rotate.png)

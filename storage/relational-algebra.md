---
title: Relational Algrebra
description: Relational algebra notes
published: true
date: 2021-01-10T21:19:09.209Z
tags: 
editor: markdown
dateCreated: 2021-01-10T21:15:09.085Z
---

# Relational  Algebra

# Operators

- Selection $\sigma$
- Projection $\pi$
- Cross-Product $X$
- Set-Difference $-$
- Union $\cup$
- Rename $\rho$

### Selection

- Select rows that satisfy condition

$^\pi_(sname, rating) (^\sigma rating > 8)$

### Projection

- Slice out columns of table not needed

$^\pi (sname, rating)$

### Union

- Will append R2 to R1

### Intersection

- Will return tuples present in **both** relations

### Set-Difference

- Will return everything in R1 that **is not**  present in R2

### Cross-Product

- Cartesian product --> matches each tuple together n(X) = n(R1) * n(R2)


# Joins

## Conditional-Join

- Fewer tuples than a cross-product, might be able to compute more efficiently
- Sometimes called *theta-join*

## Equi-Join

- Special case of Conditional-Join where the condition contains **only** equalities and ^

## Natural Join

- Equijoin on ***all*** common fields
- Common attributes --> same column. No duplicates

## Nested-Loop Join

- Tuple-based nested loop $R \bowtie S$
```
for each tuple r in R do
	for each tuple s in S do
  	if r and s join then output(r,s)
```
O(n^2)

## Outer Joins

![left-outer-join.png](/left-outer-join.png)
![right-outer-join.png](/right-outer-join.png)

### Examples

![db_example_1.png](/db_example_1.png)

- Find sailors who have reserved boat 103

$\sigma(bid=103) Reserves \bowtie Sailors$


- Find sailors who've reserved a red boat

$\pi sname ((^\sigma color='red'^{Boats}) \bowtie Reserves \bowtie Sailors$














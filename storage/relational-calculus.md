---
title: Relation Calculus
description: Relational calculus notes
published: true
date: 2021-01-10T21:30:06.137Z
tags: 
editor: markdown
dateCreated: 2021-01-10T21:30:06.137Z
---

# Relational Caluculus

- RC is a non-procedural query language, it outlines what to do but doesn't go into detail on implementation

- Element *t* of *r* is a tuple, representing a *row* of a table

## Operators

- AND ^
- OR V
- NOT ¬
- There exists x $\exists x$		-> ( at least once it must be satisfied)
- For all $\forall x$						-> ( every tuple must satisfy this condition)

## Queries

{$t | P(t)$}

P() <-- query condition
P(t) <-- set of all tuples such that P(t) is true for t

## Example

- Find the loan number, branch, amount of loans of greater than or equal to 10,000 amount

![calculus-example-1.png](/calculus-example-1.png)

## Projections

$^\pi LNAME, YEAR(WINNERS)$

{$t | \exists w \in Winners(t[LNAME] = w[LNAME] ^ t[YEAR] = w[YEAR])$}


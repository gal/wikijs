---
title: ER Diagrams
description: ER diagrams notes
published: true
date: 2021-01-10T21:50:27.057Z
tags: 
editor: markdown
dateCreated: 2021-01-10T21:50:27.057Z
---

# ER Diagrams

- Basically set diagrams
- 'Enroll in' is a relation between 'students' and 'courses'

![er-diagram-set-1.png](/er-diagram-set-1.png)

# Entity Relationship Model

- Entities are represented with rectangles
- Relationships between entities are represented with diamonds connecting entities

![entity-relationship-1.png](/entity-relationship-1.png)

![entity-relationship-symbols.png](/entity-relationship-symbols-1.png)

![entity-relationship-symbols-2.png](/entity-relationship-symbols-2.png)

- A single line means a relation is optional, if double, mandatory

## Cardinality

Cardinality is a constraint on a relationship specifying the number of entity instances that a specific entity may be related to via the relationship

![cardinality.png](/entity-relationship-cardinality.png)
AN invoice line will specify **exactly** one product. A product may appear on any number, zero, or more invoice lines.

### 1to1 Relationships

- One-to-One relationships have '1' specified for **both** cardinalities

## Arrow Notation

Arrows imply **one**, a line without an arrow signifies many between the relationship set and the entity set

## Recursive Relationships 

- If an entity has a relationship with another entity of the same entity set, then we have a **recursive** relationship

- Some situations where recursive relationships can be used
	- An employee supervises other employees
  - A person marries another person
  - A person is a child of a person
  - A course is a pre-requisite of another course
  - A team plays against another team
  - Organizational units report to other organizational units
  - A bill-of-materials system, where a part is composed of other parts

### Recursion

- If the same entity set appears more than once in a relationship, the relationship is recursive

![entity-relationship-recurision.png](/entity-relationship-recurision.png)




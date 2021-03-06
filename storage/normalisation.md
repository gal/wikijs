---
title: Normalisation of Data Tables
description: Normalisation of Data Tables notes
published: true
date: 2021-01-11T08:36:34.213Z
tags: 
editor: markdown
dateCreated: 2021-01-10T22:17:07.562Z
---

# Normalisation of Data Tables

## Data Redundancy

- This is when data is backed up somewhere -- common practice for many businesses
- In a database means that some data afields are repeated in the database
- This data repetition may occur if a field is repeated in multiple tables or if the field is repeated in the table

## Data Integrity

- This refers to maintaining and assuring the accuracy and consistency of data and is a critical aspect to the design of any system which stores, processes and/or retrieves data

	- **Physical Integrity** deal with challenges associated with correctly storing and fetching data
  - **Logical Integrity** concerns the correctness and rationality of a piece of data given context. Including topics such as referential integrity and entity integrity in a relational database

- MySQL allows for **constraints** to a table. The primary goal of most constrainsts is data integrity. In other words, their purpose is to improve the validity and consistency of your data

### Disadvantages of Data Redundancy

- Increases the size of the db
- Causes data inconsistency
- Decreases efficiency
- May cause corruption

# Normalisation
- Normalisation is a process for assigning attributes to entities. It reduces data redundancies and helps eliminate data abnormalities
- Probably most valuable as a way of evaluating and correcting design in DBs
- Normalisation works through stages called forms
	- First Normal Form (1NF)
  - Second Normal Form (2NF)
  - Third Normal Form (3NF)
  - Fourth Normal Form (4NF)

- Unnormalised Form (UNF)
	- A table contains one or more repeating groups
  - To create an unnormalised table...
  	- Transform data to table format w/ columns & rows
    
## Redundancy Problems
- Update anomalies
	- If the proj. No. changes, we need to change the proj. No everywhere else required
- Insert anomalies
	- May not be possible to add a new projecft without employees, unless we have employees in the project
- Delete anomalies
	- If all employees that work in a proj. are deleted, then we lose the proj. No


|Normal Form|Characteristic|
|-----------|--------------|
|First Normal Form| Table Format, no repeating groups and PK identified|
|Second Normal Form|1NF and no partial dependencies|
|Third Normal Form|2NF and no transitive dependecies|
|Boyce-Codd Normall Form|Every determinant is a candidate key (special case of 3NF)|
|Fourth Normal Form|3NF and no independent multivalued dependencies|

## Functional Dependencies
- This is a form of constraint and is part of a relation's schema to define a valid instance
- Definition A -> B
- The value of A functionally defines the value of B

- We say B has a functional dependency on another attribute A. If for any two records, which have the same value for A, the nteh values for B in these two records must be the same we illustrate it as:

![normalisation-functional-dependency.png](/normalisation-functional-dependency-1.png)

![normalisation-functional-dependency-2.png](/normalisation-functional-dependency-2.png)

# Keys

![normalisation-keys-1.png](/normalisation-keys-1.png)

# 1st Normal Form

- Two-dimensional table
- No repeating groups --> each row/column intersect only contains one value
- Identify FDs and also primary key

- Problems in 1NF
	- Insert anomalies
  - Update Anomalies
  - Delete anomalies

# 2nd Normal Form

- 1NF
- Every non-primary-key attribute is fully functionally dependent on the primary key

- Problems in 1NF
	- May be transitive dependencies, causing update anomalies

If partial dependencies exist on the primary key remove them by placing them in a new relation along with a copy of their determinant

# 3rd Normal Form

- 2NF
- No primary-key attribute is transitively dependent on a candidate key ( no transitive dependencies A->B->C)

If transitive dependencies exist on the primary key, remove them by placing them in a new relation along with a copy of their dominant

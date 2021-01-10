---
title: Normalisation of Data Tables
description: Normalisation of Data Tables notes
published: true
date: 2021-01-10T22:19:37.549Z
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

## Case of a construction company
- Building project -- Project No., Name, Employees assigned to the project



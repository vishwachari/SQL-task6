# Task - 06 - Subqueries & Nested Queries

## Overview
This task focuses on writing and executing **subqueries** and **nested queries** in MySQL.  
It demonstrates how to use subqueries in different clauses and contexts to extract and filter data.

## Tools Used
- MySQL Workbench  

## Objectives
- Learn and apply different types of subqueries:
  - Scalar subqueries (return a single value)  
  - `IN` subqueries (return a list of values)  
  - `EXISTS` subqueries (check for existence of rows)  
  - Correlated subqueries (depend on outer query)  
  - Subqueries in the `FROM` clause (derived tables)  
  - Nested subqueries with operators (`ANY`, `ALL`)  
- Use subqueries to answer complex questions on the Classic Models dataset.  

## Deliverables
- `task-6-subqueries.sql` (SQL script of subqueries)  
- Screenshots of query results (scalar, IN, EXISTS, correlated, derived table, etc.)  
- Documentation in `README.md`  

## Example Queries
- **Scalar Subquery**: Most expensive product  
- **IN Subquery**: Customers who placed an order  
- **EXISTS Subquery**: Customers with orders  
- **Correlated Subquery**: Customers with orders above average  
- **Derived Table**: Top 5 customers by sales  
- **Nested Subquery**: Products never ordered  

## Key Learnings
- Subqueries can be used in `SELECT`, `FROM`, `WHERE`, and `HAVING` clauses.  
- Correlated subqueries execute once for each outer row.  
- MySQL supports subqueries in most places, but performance may require rewriting as joins for large datasets.  

## Author
Syed Ahmed Ali  

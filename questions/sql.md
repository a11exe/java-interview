# SQL Interview Questions

+ [What is a primary key?](#what-is-a-primary-key)
+ [What is a foreign key?](#what-is-a-foreign-key)
+ [What is a unique key?](#what-is-a-unique-key)
+ [What is the difference between a primary key and a unique key?](#what-is-the-difference-between-a-primary-key-and-a-unique-key)
+ [What is Normalization in a Database?](#what-is-normalization-in-a-database)
+ [What are the disadvantages of not performing database Normalization?](#what-are-the-disadvantages-of-not-performing-database-normalization)
+ [What is Denormalization in a Database?](#what-is-denormalization-in-a-database)
+ [What is a view in SQL?](#what-is-a-view-in-sql)
+ [What is an Index in SQL?](#what-is-an-index-in-sql)
+ [What are the different types of indexes in SQL?](#what-are-the-different-types-of-indexes-in-sql)
+ [What are the different types of joins in SQL?](#what-are-the-different-types-of-joins-in-sql)
+ [What is a "TRIGGER" in SQL?](#what-is-a-trigger-in-sql)
+ [What are the set operators in SQL?](#what-are-the-set-operators-in-sql)
+ [What is the difference between IN and BETWEEN operators?](#what-is-the-difference-between-in-and-between-operators)
+ [How to write an SQL query to find students' names start with 'A'?](#how-to-write-an-sql-query-to-find-students-names-start-with-a)
+ [Write the SQL query to get the third maximum salary of an employee from a table named employees.](#write-the-sql-query-to-get-the-third-maximum-salary-of-an-employee-from-a-table-named-employees)
+ [What is the ACID property in a database?](#what-is-the-acid-property-in-a-database)
+ [How do we use the DISTINCT statement? What is its use?](#how-do-we-use-the-distinct-statement-what-is-its-use)
+ [What is the default ordering of data using the ORDER BY clause? How could it be changed?](#what-is-the-default-ordering-of-data-using-the-order-by-clause-how-could-it-be-changed)
+ [What is the difference between the WHERE and HAVING clauses?](#what-is-the-difference-between-the-where-and-having-clauses)
+ [How many Aggregate functions are available in SQL?](#how-many-aggregate-functions-are-available-in-sql)

## What is a primary key?

A primary key is a field or the combination of fields that uniquely identify each record in the table. 
It is one of a special kind of unique key. If the column contains a primary key, it cannot be null or empty. 
A table can have duplicate columns, but it cannot have more than one primary key. 
It always stores unique values into a column.

```sql
CREATE TABLE Student (    
    roll_number INT PRIMARY KEY,    
    name VARCHAR(45)    
);    
```

## What is a foreign key?

The foreign key is used to link one or more tables together. It is also known as the referencing key. 
A foreign key is specified as a key that is related to the primary key of another table. 
It means a foreign key field in one table refers to the primary key field of the other table. 
It identifies each row of another table uniquely that maintains the referential integrity. 
The primary key-foreign key relationship is a very crucial relationship as it maintains the ACID properties of 
the database sometimes. It also prevents actions that would destroy links between the child and parent tables.

```sql
CONSTRAINT constraint_name]    
    FOREIGN KEY [foreign_key_name] (col_name, ...)    
    REFERENCES parent_tbl_name (col_name,...)   
```

## What is a unique key?

A unique key is a single or combination of fields that ensure all values stores in the column will be unique. 
It means a column cannot stores duplicate values. This key provides uniqueness for the column or set of columns.

```sql
CREATE TABLE table_name(    
    col1 datatype,    
    col2 datatype UNIQUE    
);  
``` 

## What is the difference between a primary key and a unique key?

The primary key and unique key both are essential constraints of the SQL. The main difference among them is that 
the primary key identifies each record in the table. In contrast, the unique key prevents duplicate entries in 
a column except for a NULL value.

## What is Normalization in a Database?

There are some rules of database normalization, which is commonly known as Normal From, and they are:

+ First normal form (1NF)
    + Each table cell should contain a single value.
    + Each record needs to be unique.
+ Second normal form (2NF)
    + Rule 1 - Be in 1NF
    + Rule 2 - All non-key attributes are fully functional dependent on the primary key.
    (foreign key, uniq rows)
+ Third normal form (3NF)
    + Rule 1 - Be in 2NF
    + Rule 2 - Has no transitive functional dependencies
 This is Transitive Dependency. When a non-prime attribute depends on other non-prime attributes rather 
 than depending upon the prime attributes or primary key.
 
## What are the disadvantages of not performing database Normalization?

The major disadvantages are:

The occurrence of redundant terms in the database causes the waste of space in the disk.
Due to redundant terms, inconsistency may also occur. If any change is made in the data of one table but not made 
in the same data of another table, then inconsistency will occur. 
This inconsistency will lead to the maintenance problem and effects the ACID properties as well.

## What is Denormalization in a Database?

Denormalization is a technique used by database administrators to optimize the efficiency of their database infrastructure. 
The denormalization concept is based on Normalization, which is defined as arranging a database into tables correctly 
for a particular purpose. This method allows us to add redundant data into a normalized database to alleviate issues 
with database queries that merge data from several tables into a single table. 
It adds redundant terms into the tables to avoid complex joins and many other complex operations.

Denormalization doesn't mean that normalization will not be done. 
It is an optimization strategy that takes place after the normalization process.

## What is a view in SQL?

A view is a database object that has no values. It is a virtual table that contains a subset of data within a table. 
It looks like an actual table containing rows and columns, but it takes less space because it is not present physically. 
It is operated similarly to the base table but does not contain any data of its own. 
Its name is always unique. A view can have data from one or more tables. If any changes occur in the underlying table, 
the same changes reflected in the views also.

The primary use of a view is to implement the security mechanism. It is the searchable object where we can use a query 
to search the view as we use for the table. It only shows the data returned by the query that was declared when 
the view was created.

```sql
CREATE VIEW view_name AS  
SELECT column_lists FROM table_name  
WHERE condition;  
```

## What is an Index in SQL?

An index is a disc structure associated with a table or view that speeds up row retrieval. 
It reduces the cost of the query because the query's high cost will lead to a fall in its performance. 
It is used to increase the performance and allow faster retrieval of records from the table. 
Indexing reduces the number of data pages we need to visit to find a particular data page. 
It also has a unique value meaning that the index cannot be duplicated. 
An index creates an entry for each value which makes it faster to retrieve data.

## What are the different types of indexes in SQL?

+ Unique Index. UNIQUE INDEX is used to enforce the uniqueness of values in single or multiple columns. 
We can create more than one unique index in a single table. For creating a unique index, the user has to check the data 
in the column because the unique indexes are used when any column of the table has unique values. 
This indexing does not allow the field to have duplicate values if the column is unique indexed. 
A unique index can be applied automatically when a primary key is defined.
```sql
CREATE UNIQUE INDEX index_name    
ON table_name (index_column1, index_column2,...);  
```

+ Clustered Index. A clustered index is actually a table where the data for the rows are stored. 
It determines the order of the table data based on the key values that can sort in only one direction. 
Each table can have only one clustered index. It is the only index, which has been automatically created when 
the primary key is generated. If many data modifications needed to be done in the table, then clustered indexes are preferred.

+ Non-Clustered Index. The indexes other than PRIMARY indexes (clustered indexes) are called non-clustered indexes. 
We know that clustered indexes are created automatically when primary keys are generated, and non-clustered indexes 
are created when multiple joins conditions and various filters are used in the query. 
The non-clustered index and table data are both stored in different places. 
It cannot be able to alter the physical order of the table and maintains the logical order of data.
The non-clustered indexing improves the performance of the queries which use keys without assigning the primary key.

## What are the different types of joins in SQL?

+ INNER JOIN Inner join returns only those records from the tables that match the specified condition and hides other 
rows and columns. In simple words, it fetches rows when there is at least one match of rows between the tables is found.
```sql
SELECT column_lists  
FROM table1    
INNER JOIN table2 ON join_condition1    
INNER JOIN table3 ON join_condition2    
...;    
```
+ SELF JOIN A SELF JOIN is used to join a table with itself. 
This join can be performed using table aliases, which allow us to avoid repeating the same table name in a single sentence.
A SELF JOIN is required when we want to combine data with other data in the same table itself.
```sql
SELECT column_lists    
FROM table1 AS T1, table1 AS T2    
WHERE join_conditions;    
```
+ OUTER JOIN
    + LEFT OUTER JOIN The Left Join is used to fetch all rows from the left-hand table and common records between the specified tables. 
    It returns all the rows from the left-hand side table even though there are no matches on the right-hand side table. 
    + RIGHT OUTER JOIN The Right join is used to retrieve all rows from the right-hand table and only those rows from 
    the other table that fulfilled the join condition.
    ```sql
    SELECT colum_lists    
    FROM table1     
    RIGHT JOIN table2    
    ON join_condition;  
    ```
    + FULL OUTER JOIN The Full Join results from a combination of both left and right join that contains all the records 
    from both tables. It fetches rows when there are matching rows in any one of the tables. 
    This means it returns all the rows from the left-hand side table and all the rows from the right-hand side tables. 
    If a match is not found, it puts NULL value. It is also known as FULL OUTER JOIN.
    ```sql
    SELECT * FROM table1     
    FULL OUTER JOIN table2    
    ON join_condition;  
    ```
+ CROSS JOIN

## What is a "TRIGGER" in SQL?

A trigger is a set of SQL statements that reside in a system catalog. 
It is a special type of stored procedure that is invoked automatically in response to an event. 
It allows us to execute a batch of code when an insert, update or delete command is run against a specific table because 
the trigger is the set of activated actions whenever DML commands are given to the system.

SQL triggers have two main components one is action, and another is an event. When certain actions are taken, 
an event occurs as a result of those actions.

## What are the set operators in SQL?

We use the set operators to merge data from one or more tables of the same kind. 
Although the set operators are like SQL joins, there is a significant distinction. 
SQL joins combine columns from separate tables, whereas SQL set operators combine rows from different queries. 
SQL queries that contain set operations are called compound queries. 
The set operators in SQL are categories into four different types:

+ UNION: It combines two or more results from multiple SELECT queries into a single result set.
```sql
SELECT columns FROM table1    
UNION    
SELECT columns FROM table2;    
```
+ UNION ALL: This operator is similar to the Union operator, 
but it does not remove the duplicate rows from the output of the SELECT statements.
```sql
SELECT columns FROM table1    
UNION  ALL  
SELECT columns FROM table2;    
```

+ INTERSECT: This operator returns the common records from two or more SELECT statements. 
It always retrieves unique records and arranges them in ascending order by default. 
Here, the number of columns and data types should be the same.
```sql
SELECT columns FROM table1    
INTERSECT  
SELECT columns FROM table2;    
``` 

+ MINUS: This operator returns the records from the first query, which is not found in the second query. 
It does not return duplicate values.
```sql
SELECT columns FROM table1    
MINUS  
SELECT columns FROM table2;    
```

## What is the difference between IN and BETWEEN operators?

+ BETWEEN This operator is used to selects the range of data between two values. 
The values can be numbers, text, and dates as well.

+ IN It is a logical operator to determine whether or not a specific value exists within a set of values. 
This operator reduces the use of multiple OR conditions with the query.

## How to write an SQL query to find students' names start with 'A'?

```sql
SELECT * FROM student WHERE stud_name like 'A%';  
```

## Write the SQL query to get the third maximum salary of an employee from a table named employees.

```sql
SELECT * FROM `employees` ORDER BY `salary` DESC LIMIT 1 OFFSET 2  
```

## What is the ACID property in a database?

The ACID properties are meant for the transaction that goes through a different group of tasks. 
A transaction is a single logical order of data. It provides properties to maintain consistency before and after 
the transaction in a database. It also ensures that the data transactions are processed reliably in a database system.

The ACID property is an acronym for Atomicity, Consistency, Isolation, and Durability.

+ Atomicity: It ensures that all statements or operations within the transaction unit must be executed successfully. 
If one part of the transaction fails, the entire transaction fails, and the database state is left unchanged. 
Its main features are COMMIT, ROLLBACK, and AUTO-COMMIT.

+ Consistency: This property ensures that the data must meet all validation rules. 
In simple words, we can say that the database changes state only when a transaction will be committed successfully. 
It also protects data from crashes.

+ Isolation: This property guarantees that the concurrent property of execution in the transaction unit must be operated 
independently. It also ensures that statements are transparent to each other. 
The main goal of providing isolation is to control concurrency in a database.

+ Durability: This property guarantees that once a transaction has been committed, it persists permanently even if 
the system crashes, power loss, or failed.

## How do we use the DISTINCT statement? What is its use?

The DISTINCT keyword is used to ensure that the fetched value always has unique values. 
It does not allow to have duplicate values. The DISTINCT keyword is used with the SELECT statement and retrieves 
different values from the table's column.

```sql
SELECT DISTINCT column_lists FROM table_name WHERE [condition];  
```

## What is the default ordering of data using the ORDER BY clause? How could it be changed?

The ORDER BY clause is used to sort the table data either in ascending or descending order. 
By default, it will sort the table in ascending order. If we want to change its default behavior, we need to use 
the DESC keyword after the column name in the ORDER BY clause.

```sql
SELECT expressions FROM tables    
WHERE conditions    
ORDER BY expression [ASC | DESC];    
```

## What is the difference between the WHERE and HAVING clauses?

The main difference is that the WHERE clause is used to filter records before any groupings are established, 
whereas the HAVING clause is used to filter values from a group.

## How many Aggregate functions are available in SQL? 

SQL provides seven (7) aggregate functions, which are given below:

+ AVG(): This function is used to returns the average value from specified columns.
+ COUNT(): This function is used to returns the number of table rows, including rows with null values.
+ MAX(): This function is used to returns the largest value among the group.
+ MIN(): This function is used to returns the smallest value among the group.
+ SUM(): This function is used to returns the total summed values(non-null) of the specified column.
+ FIRST(): This function is used to returns the first value of an expression.
+ LAST(): This function is used to returns the last value of an expression.
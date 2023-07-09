# Database Optimization
It refers to the process of improving the performance and efficiency of a database system.

**Benefits of Database Optimization**
1. Improved performance
2. Faster turnaround times
3. Remove unwanted loads

**Types of SQL Statements**
1. Data retrieval statements
2. Data change statements

**Best Practices to optimize the SELECT Statements**
1. Target only required columns
2. Avoid using functions in predicate (WHERE clause condition)
3. Avoid leading wildcards in predicates
4. Use INNER JOIN instead of OUTER JOIN
5. Use clauses sparingly

## Optimizing the SELECT queries with the EXPLAIN statement

**Overview of the EXPLAIN statement**

When we run the explain statement, the result will show the 12 columns Lets examine the EXPLAIN statement by its columns.


**EXPLAIN:** Provides information about how MySQL execute statements.


**Column 01: ID**

This column is a sequential identifier for each SELECT statement with in a query.


**Column 02: SELECT_TYPE**

This column displays the type of select query to be executed.

|Value	 			|Description							|
|-----------------------------------------------|----------------------------------------------------------------------------------------------|
|SIMPLE				|Simple select query without any SUBQUERY or JOINS		|
|PRIMARY			|The SELECT is the outmost query in a JOIN				|
|DERIVED			|The first SELECT in a subquery					|
|DEPENDENT SUBQUERY	|The SELECT is subquery dependent on an outer query		|
|UNCACHEABLE SUBQUERY	|Subquery which is not cacheable.					|
|UNION 				|The SELCET query is the second or later statement of a union		|
|DEPENDENT UNION		|The second or later SELECT of UNION is dependent on outer query	|
|UNION RESULT			|The SELECT is the result of a UNION				|

**Column 03: table**

This column displays the name of the table referred into the SELECT query.


**Column 04: Partition**

This column displays the partition in which the data resides (the area of the physical storage that’s scanned).


**Column 05: type**

Scanning the table means performing a search operation or finding matches specified by the SELECT queries.


|Value	|Description|
|------------|---------------|
|system | The table has only one or zero rows. |
|Const | Indicate that the value of the searched column can be treated as a constant. |
|eq_ref | Indicate that the index is clustered and is being used by the operation. |
|ref |Indicate that the indexed column was accessed using an equality operator. |
|full text | The scan uses the table’s FULL TEXT Index |	
|index | The entire index is scanned to find a match for the query. |
|all | The entire table is scanned to find the matching rows. |


**Column 06: possible_keys**

This column shows the key that can be used by MySQL to find the row from the table.


**Column 07: key**

Indicate the actual index used by MySQL.


**Column 08 : Key_len**

This column indicate the length of the index the query optimizer chooses to uses.


**Column 09 : ref **

This column shows which table columns have been compared to the index to perform the search.


**Column 10 : rows**

List the number of record that were examined to produce the output.


**Column 11 : filtered**

This column indicate an approximate percentage of the number of table rows that have been filtered by a specified condition.


**Column 12 : extra**

Contains additional information regarding the query execution plan.


**Note** 
When explain statement is executed, it can return more detailed result but attention need to be paid to the following columns:

1. type
2. possible_keys
3. keys
4. ref,
5. rows
6. extra

## INDEX 

Index is a data structure that improves the speed of data retrieval operations. It works similar to index in a book.


``` 
CREATE INDEX Index_Name
ON Table_Name(Column1, Column2, Column3);
```


```
DROP INDEX index_name 
ON table_name;
```


**Guidelines for Indexes**

1. Automatically create the indexes for primary keys and unique columns.
2. Index columns that you frequently use to retrieve data.
3. Index columns that are used for joins to improve join performance.
4. Avoid column that contains too many NULL values.
5. Small tables do not require indexes.


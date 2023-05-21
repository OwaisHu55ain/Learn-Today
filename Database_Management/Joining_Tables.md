## Joining Tables:

**SQL aliases:** Provide temporary name with in a DB for ease-of-use.

* There are three common situation where the aliases are usefull:
1. **Renaming:** Rename tables or columns.

```
SELECT ColumnName As AliasName From TableName;
```

2. **Function:** Combine column output using concatenation fuction.
```
SELECT CONCAT (Column1, " ", Column2) As NewColumnName FROM TableName;
```

3. **Multiple Tables:** Use an alias to create distinct table names.
```
SELECT x.column1, y.column2, x.column3, y.column4 FROM Table1 as x, Table2 as y WHERE x.column1 > 5 AND y.column2 < 5;
```

**Joins:** Links records of Data bwtween one or multiple tables based on a common column between them.

* **Need of joins:** Find information about relevant activity in DB.

* There are four types of joins:

1. **INNER JOINS:** Return the record of data have matching values in the joined tables.
```
SELECT Table1.ColumnName FROM Table1 INNER JOIN Table2 ON Table1.ColumnName = Table2.ColumnName;
```

2. **LEFT JOINS:**  Returns all the records from the left table regardless of whether there is a match in the right table or not.
```
SELECT customers.customerID, customers.name, orders.amount FROM customers LEFT JOIN orders ON customers.customerID = orders.customerID;
```

3. **RIGHT JOINS:** Returns all the records from the right table regardless of whether there is a match in the left table or not.
```
SELECT customers.customerID, customers.name, orders.amount FROM customers RIGHT JOIN orders ON customers.customerID = orders.customerID;
```

4. **SELF JOINS:**  Join a table with itself to get a specific information.
```
SELECT e1.FullName AS "Line Manager", e2.FullName AS "Employee" FROM Employee AS e1 INNER JOIN Employee AS e2 ON e1.EmployeeID = e2.LineManagerID;
```

**UNION:** Combine results sets from multiple statements in the same query.

* **Best Practices with UNION: **
  - Same numbers of columns in each select statement.
  - All related columns have the similar data types.
  - Columns have the same order.

```
SELECT FullName, Location FROM CurrentClient UNION SELECT FulleName, Location FROM LegacyClients; (This statement will remove the duplicate values)
```
```
SELECT FullName, Location FROM CurrentClient UNION ALL SELECT FulleName, Location FROM LegacyClients; (This statement will not remove the duplicate values)
```


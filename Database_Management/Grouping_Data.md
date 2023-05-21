### GROUPING DATA

* **GROUP BY:** Group Rows that have the same values in one or more column into summary rows.
```
SELECT column1, SUM(column2) FROM TableName GROUP BY column1;
```
* **Aggregate Functions:**
  - SUM(): Add values of given column.
  - AVERAGE(): Average the values of given column.
  - MAX(): Return the maximum value.
  - MIN() Shows the minimum value.
  - COUNT(): Count the number of instances that a given column

* **HAVING:** Specifies a condition for group of rows or aggregates.
```
SELECT department, SUM(OrderTotal) FROM orders GROUP BY department HAVING SUM(OrderTotal) > 2275;
```

* **ANY:** Perform a comparison between a single value and a range of other value.
```
SELECT ColumnName FROM TableName WHERE ColumnName comparison operator ANY (SELECT ColumnName FROM TableName WHERE Condition);
```

* **ALL:** Return TRUE only if ALL the subquery values meet the given condition.
```
SELECT ColumnName FROM TableName WHERE ColumnName operator ALL (SELECT ColumnName FROM TableName WHERE Condition);* ANY:
```

* **REPLACE:** Insert or update data in table by deleting and replacing existing records.
```
REPLACE INTO Orders (OrderID, ClientID, ProductID, Quantity, Cost) VALUES (13, "Cl1", "P1", 10, 5000), (14, "Cl2", "P2", 5, 100);
```
```
REPLACE INTO Orders SET OrderID = 9, ClientID = "Cl1" , ProductID = "P1", Quantity = 10,Cost = 500;
```

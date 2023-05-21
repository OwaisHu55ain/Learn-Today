## Functions in MySQL
A code that performs an operation and return result, often with the use of parameter.

There are five different types of Functions in MySQL:
1. Numeric Functions
2. String Functions
3. Data and Time Functions
4. Comparison Functions
5. Control Flow Functions

### Numeric Functions
* **Numeric Functions:** Can be divided into tow categories.
1. **Aggregate Functions:** Perform task on a set of values.
2. **Math Functions:** Perform basic mathematical task on data.

* **Aggregate Functions:** 
1. **SUM():** Calculates the sum of a column values. 
```
SELECT SUM(CoulmnName) FROM TableName;
```

2. **AVG():** Calculates the average of a column values.
```
SELECT AVG(CoulmnName) FROM TableName;
```

3. **MAX():** Return the maximum value from a specific column.
```
SELECT MAX(CoulmnName) FROM TableName;
```

4. **MIN():** Return the minimum value from a specific column.
```
SELECT MIN(CoulmnName) FROM TableName;
```

5. **COUNT():** Return the number of rows that match the specified condition.
```
SELECT COUNT(CoulmnName) FROM TableName;
```
6. **CEIL():** Round a number up to the nearest integer value.
```
SELECT CEIL(4.5);
```
7. **FLOOR():** Round a number down to the nearest integer value.
```
SELECT FLOOR(4.5);
```


* **Math Functions:**
1. **ROUND():** Round a numeric value to specified number of decimal places.
```
SELECT ROUND(AVG(Cost), 2) FROM TableName;
```

2. **MOD():** Return the remainder of division operation.
```
SELECT MOD(ColumnName, 2) FROM TableName;
```

### String Functions
String functions perform different operation on string values in a database.

1. **UCASE():** Covert a string to upper case.
```
SELECT UCASE(ColumnName) FROM TableName;
```

2. **LCASE():** Convert a string to lower case.
```
SELECT LCASE(ColumnName) FROM TableName;
```

3. **CONCAT():** Concatenate to or more string together.
```
SELECT CONCAT(ColumnName, “ ”, ColumnName) AS NewColumnName FROM TableName;
```
4. **SUBSTR():** Extract a substring from a string based on starting position and length.
```
SELECT SUBSTR(‘Hello World’, 7, 5);
```


### Date Functions
Extract output that contain information on time and data values.

1. **CURRENT_DATE():** Retrieve the current date.
```
SELECT CURRENT_DATE();
```
2. **CURRENT_TIME():** Retrieve the current time.
```
SELECT CURRENT_TIME();
```

3. **DATE_FORMAT():** Format and date and date time.
```
SELECT DATE_FORMAT(date, format);
```

4. **DATEDIFF():** Calculate the difference between two dates.
```
SELECT DATEDIFF(end_date, start_date);
```

5. **FORMAT():** Format a number with a specified number of decimal places and thousand separator.
```
SELECT FORMAT(753.75555, 2);
```

6. *ADDDATE:** Add a specified interval of time to a date.
```
SELECT ADDDATE(OrderDate INTERVAL 30 DAY) AS ExpectedDates FROM mg_orders;
```



###Comparison Functions
Compare values with in a database.

1. **GREATEST():** Retrieve the greatest (maximum) value from the list of expression.
2. **LEAST():** Determine the smallest value among a list of expression.
3. **ISNULL():** Determine the largest value among a list of expression.
```
SELECT ItemID, GREATEST(Q1, Q2, Q3, Q4) AS Highest, LEAST(Q1, Q2, Q3, Q4) AS LOWEST FROM Revenue;
```
``` 
SELECT * FROM WHERE ISNULL(DeliveryDate);
```

4. **IFNULL():** Check if a value is NULL return an alternative value if it is.
```
SELECT IFNULL(DeliveryDate, “N/A”) FROM mg_orders;
```

5. **NULLIF():** Used to handle cases where you want to treat specific value as NULL.
```
SELECT OrderID, NULLIF(OrderStatus,'In Progress') AS status FROM mg_orders;
```

6. ** COALESCE():** Allow you to handle null values and provide a default value when encountering nulls.
```
SELECT OrderID, ItemID, Quantity, Cost,  OrderDate,COALESCE (DeliveryDate,'NOT DELIVERED'), OrderStatus FROM mg_orders;
```


### Control Flow Functions
Evaluate conditions and determine the execution path of a query.

1. **CASE:** Perform different action based on different condition.
```
SELECT ItemID,
CASE
WHEN LEAST(Q1,Q2,Q3,Q4) <= 25000 THEN “Loss” 
ELSE “Profit”
END AS Profit_Loss
FROM Sales_Revenue;
```

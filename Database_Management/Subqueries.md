## Sub-Queries:
----------------

* **SUBQUERIES:** An inner query (Child Query) placed within an outer query (Parent Query).
```
SELECT ColumnName
FROM TableName
WHERE expression operator
(SELECT ColumnName FROM TableName WHERE condition);
```

* **SUBQUERY RESULTS:**

1. **Single Value:** Returns only one value.
```
SELECT product_name, product_price
FROM products
WHERE product_price > (SELECT AVG(product_price) FROM products);
```
```
SELECT customer_name, (SELECT COUNT(*) FROM orders WHERE customer_id = customers.customer_id) AS order_count
FROM customers;
```

2. **Single Row:** Returns only one row.
```
SELECT product_name, product_price
FROM products
WHERE product_price > (SELECT AVG(product_price) FROM products);
```

3. **Single Column:** Return only one column of data.
```
SELECT *
FROM orders
WHERE customer_id IN (SELECT customer_id FROM customers WHERE country = 'USA');
```

4. Multiple Rows: Return multiple rows of data.
```
SELECT *
FROM orders
WHERE customer_id IN (SELECT customer_id FROM customers WHERE country = 'USA');
```
* **Types of Subqueries:**
  - **Sub-queries in the FROM clause:** The result returned from the subquery used as temporary table.
```
SELECT * FROM (SELECT customer_id, COUNT(*) AS order_count FROM orders GROUP BY customer_id) AS customer_orders WHERE order_count > 5;
```
  
  - **Sub-queries in the INSERT statements:** Allow you to insert data into a table based on the result subquery.
```
INSERT INTO table1 SELECT column1,column2,column3 FROM table2 WHERE some_column some_operator(Subquery);
```

  - *Sub-queries in UPDATE statement:** You can use sub-query to filter out the record you want update.
```
UPDATE table1 SET column1 = some_value WHERE some_column some_operator(Sub-query);
```

  - **Sub-queries in DELETE statement:** You can use subquery to filter out the record you want to update.
```
DELETE FROM table1 WHERE some_column some_operator(Subquery);

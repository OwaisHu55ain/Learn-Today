# Stored Procedures and Functions: 
Wrap code within the body of a function or procedure for repeated use.

* **Benefits of Stored Procedures and Functions:**
1. **Consistency:** Code is  standardized.
2. **Organization:** Code is organized.
3. **Reusability:** Code can be used repeatedly.

## Procedures:
Accept both input and output parameters.

```
CREATE PROCEDURE GetOrderDetail(Parameter1 INT, Parameter2 INT)
SELECT *
FROM TableName
WHERE Salary BETWEEN Parameter1 AND Parameter2;
```
```
CALL GetOrderDetail();
```

### Functions:
Accept only input parameters.

```
SELECT MOD(7, 5);
```
```
SELECT ClientID ROUND(AVG(Cost), 2)
FROM Client Orders
GROUP BY ClientID;
```
**Variable:** Store value that can be stored and manipulated.


**SET command:** Assign a value to a variable with in a stored procedure.
```
SET @VariableName = 42;
SELECT *  From TableName WHERE OrderID = @Variable Name;
```
```
DECLARE minimum_order_cost DECIMAL(5, 2) DEFAULT 0;
```


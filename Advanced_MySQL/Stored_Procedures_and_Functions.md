
# Stored Procedures and Functions 
Wrap code within the body of a function or procedure for repeated use.

### Benefits of Stored Procedures and Functions
1. **Consistency:** Code is  standardized.
2. **Organization:** Code is organized.
3. **Reusability:** Code can be used repeatedly.

### Procedures
------------------
A prepared SQL code that you can save, so the code can be reused over and over again. Stored Procedures accept both input and output parameters.

```
CREATE PROCEDURE GetOrderDetail(Parameter1 INT, Parameter2 INT)
SELECT *
FROM TableName
WHERE Salary BETWEEN Parameter1 AND Parameter2;
```
```
CALL GetOrderDetail();
```

```
DELIMITER //
CREATE PROCEDURE StudentResult(IN Marks DECIMAL(5,2), OUT Percentage DECIMAL(5,2), OUT Grade VARCHAR(25))
BEGIN
	IF (Marks >= 54 AND Marks < 63) THEN 
		SET Percentage = (Marks/90)*100, Grade = 'B';
	ELSEIF (Marks >= 63 AND Marks < 72) THEN 
		SET Percentage = (Marks/90)*100, Grade = 'A';
	ELSEIF (Marks > 72) THEN 
		SET Percentage = (Marks/90)*100, Grade = 'A+';
	END IF;
END //
DELIMITER ;
```

```
CALL StudentResult(60, @Percentage, @Grade);
```

```
SELECT @Percentage, @Grade;
```

### Functions
--------------------
A stored function in MySQL is a set of SQL statements that perform some task/operation and return a single value, Stored function accept only input parameters.

```
DELIMITER //
CREATE FUNCTION CustomerRanking(Credit DECIMAL(12, 2))
RETURNS VARCHAR(25) DETERMINISTIC
BEGIN 
	DECLARE Grade VARCHAR(25);
    
	If Credit < 50000 THEN
		SET Grade = 'Silver';
	ELSEIF Credit >= 50000 AND Credit < 75000 THEN
		SET Grade = 'Gold';
	ELSEIF Credit > 75000 THEN
		SET Grade = 'Platinium';
END IF;
RETURN (Grade);
END //
DELIMITER ;
```

```
SELECT CustomerRanking(80000);
```

```
DROP FUNCTION CustomerRanking;
```

```
SHOW FUNCTION STATUS WHERE db = 'trial';
```


### Differences Between Stored Procedure and Function

The key differences between stored procedures and functions are as following:

|S.No. 	|Functions							|Procedures							|
|-------|---------------------------------------------------------------|---------------------------------------------------------------|
|1.	|Created Using CREATE FUNCTION command 				|Created using CREATE PROCEDURE command				|
|2.	|Invoked using the SELECT statement				|Invoked using the CALL statement				|
|3.	|Must return the single value		      			|Output value via OUT parameter					|
|4.	|Takes IN parameters only					|Takes IN, OUT and INOUT parameters				|
|5.	|Typically encapsulate common formulas or generic business rule |Typically used the process, manipulate and modify database	|
|6. 	|Must specify the data type of the return value      		|User must specify the OUT parameter type			|



### Variables
-----------------------
Store and manipulate value with in your SQL statement.

**Declare Variable:**
```
SET @variable_name = value;
```

**Variable inside the SELECT Statement:**
```
SELECT @Max_Order := MAX(Cost) FROM Orders;
```

**Assigning value to variable using SELECT statement:**
```
SELECT Column_Name INTO @Variable_Name FROM Table_Name WHERE Condtion;
```

**Using variable in SQL Statement:**
```
SELECT * FROM Table_Name WHERE Column_Name = @Variable_Name;
```

**Update variable:**
```
SET @Variable_Name = New_Value;
```

**Using Variable in Calculation::**
```
SELECT @Variable_Name1 + @Variable_Name2 As Result;
```

**Declare variable in Stored Procedure:**
```
DECLARE @ Variable_Name DATATYPE DEFAULT Value;
```

**Parameters:** Place holders used in stored procedures and functions to accept values from the calling program and functions.

1. **IN (Input):** Allow you to pass values from the calling program and query into the stored procedures and functions.
```
CREATE PROCEDURE CalculationTax(IN Salary DECIMAL(10, 2) SELECT Salary*0.2 AS Tax;

CALL CalculationTax(10000);
```

2. **OUT (Output):** Parameters is used to return a single value from a stored procedure or functions.
```
CREATE PROCEDURE GetLowestCost(OUT LowestCost INT)
SELECT MIN(Cost) INTO LowestCost FROM Orders;
```

3. **INOUT:** Parameter that combine the behavior of IN and OUT parameter.
```

DELIMITER //
CREATE PROCEDURE SquareNumber(INOUT aNumber INT)
BEGIN
	SET aNumber = aNumber*aNumber;
END //
DELIMITER ;

SET @x_number = 3;

CALL SquareNumber(@x_number);

SELECT @x_number;
```

**DELIMITER:** A specific command used to change the delimiter temporarily when defining stored procedures, functions, triggers or other multi-statement constructs.
```
DELIMITER //
CREATE PROCEDURE myProcedure()
BEGIN
    -- Procedure logic goes here
    -- Statement 1
    -- Statement 2
END //
DELIMITER ;
```

**Variables:** Store and manipulate value with in your SQL statement.
**Declare Variable:**
```
SET @variable_name = value;
```
**Variable inside the SELECT Statement:**
```
SELECT @Max_Order := MAX(Cost) FROM Orders;
```
**Assigning value to variable using SELECT statement:**
```
SELECT Column_Name INTO @Variable_Name FROM Table_Name WHERE Condtion;
```
**Using variable in SQL Statement:**
```
SELECT * FROM Table_Name WHERE Column_Name = @Variable_Name;
```
**Update variable:**
```
SET @Variable_Name = New_Value;
```
**Using Variable in Calculation::**
```
SELECT @Variable_Name1 + @Variable_Name2 As Result;
```
**Declare variable in Stored Procedure:**
```
DECLARE @ Variable_Name DATATYPE DEFAULT Value;
```
**Parameters:** Place holders used in stored procedures and functions to accept values from the calling program and functions.
1. **IN (Input):** Allow you to pass values from the calling program and query into the stored procedures and functions.
```
CREATE PROCEDURE CalculationTax(IN Salary DECIMAL(10, 2) SELECT Salary*0.2 AS Tax;

CALL CalculationTax(10000);
```
2. **OUT (Output):** Parameters is used to return a single value from a stored procedure or functions.
```
CREATE PROCEDURE GetLowestCost(OUT LowestCost INT)
SELECT MIN(Cost) INTO LowestCost FROM Orders;
```
3. **INOUT:** Parameter that combine the behavior of IN and OUT parameter.
```

DELIMITER //
CREATE PROCEDURE SquareNumber(INOUT aNumber INT)
BEGIN
	SET aNumber = aNumber*aNumber;
END //
DELIMITER ;

SET @x_number = 3;

CALL SquareNumber(@x_number);

SELECT @x_number;
```

### Create Functions
-------------------------------

**User-Defined Functions:** Created to perform operations that can’t be completed with built-in functions.

**DETERMINISTIC:** Specifies that the function always produce the same result for the same input values.

**RETURNS:** Indicate the data type that the function will return.

**RETURN:** Specify the value that the function will return. 


```
DELIMITER //
CREATE FUNCTION GetTotalCost(Cost DECIMAL(5,2))
  RETURNS DECIMAL(5,2)
  DETERMINISTIC
BEGIN
  IF (Cost >= 100 AND Cost < 500) THEN
    SET Cost = Cost - (Cost * 0.1);
  ELSEIF (Cost >= 500) THEN
    SET Cost = Cost - (Cost * 0.2);
  END IF;
  SET Cost = ROUND(Cost, 2);
  RETURN Cost;
END//
```
```
SELECT GetTotalCost(600); -- Output: 480.00
SELECT GetTotalCost(250); -- Output: 225.00
```
```
DELIMITER //
CREATE FUNCTION OrderDetail(Cost DECIMAL(6,2))
RETURNS VARCHAR(25) DETERMINISTIC
BEGIN
	DECLARE Grade VARCHAR(25);
	IF (Cost > 500 AND Cost < 800) THEN SET Grade = 'C';
	ELSEIF (Cost > 800 AND Cost < 100) THEN SET Grade = 'B';
	ELSEIF (Cost >= 1000) THEN SET Grade = 'A'; 
	END IF; 
    RETURN(Grade); 
END //
DELIMITER ;
```

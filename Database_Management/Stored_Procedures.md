## Stored Procedures in MySQL
---------------------------------------------
A collection of SQL statements that are group together and saved as a single object.

**Benefits of Stored Procedures:**
1. Reusability
2. Consistency
3. Efficiency

**Stored procedure**
```
CREATE PROCEDURE ProcedureName()
SELECT ColumnName
FROM TableName;
```

**Stored procedure with parameter**
```
CREATE PROCEDURE ProcedureName(Parameter_Value INT)
SELECT ColumnName
FROM TableName;
WHERE Value = Parameter_value;
```

**Call stored procedure**
```
CALL ProcedureName();
```

**Drop stored procedure**
```
DROP PROCEDURE ProcedureName();
```

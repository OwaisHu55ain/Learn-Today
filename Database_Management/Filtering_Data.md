## Filtering Data:
---------------------------
### SQL Logical Operators:

**AND:** Check all the combined condition meet the value of True.

```
SELECT * FROM TableName WHERE City = 'Karachi' AND TOWN = 'Surjani';
```
**OR:** Any of the combined condition meet the value of True.

```
SELECT * FROM TableName WHERE City = 'Karachi' OR Town = 'Surjani';
```
**NOT:** Select a condition to be included, if the condition is not True.

```
SELECT * FROM TableName WHERE NOT (City = 'Karachi' AND Town = 'Surjani');
```
**IN:** Used to match a value against list of values.

```
SELECT * FROM TableName WHERE City IN ('KHI', 'LHR', 'ISB')
```
**BETWEEN:**  Select a value with in a range.

```
SELECT * FROM TableName WHERE Salary BETWEEN 15000 AND 20000;
```
**LIKE:** Used to match data based on pattern matching.

```
SELECT * FROM TableName WHERE ColumnName LIKE 'g__%';
```


## Changing Table Structure:

* **ALTER TABLE:** Make changes to a table in database by altering columns and constraints.
* **MODIFY:** Make changes to a specific column in a table.
* **ADD:** Add a column to a table.
* **DROP:**  Drop a column from a table.

```
ALTER TABLE TableName MODIFY ColumnName VARCHAR(10) NOT NULL;
```
```
ALTER TABLE TableName ADD COLUMN ColumnName INT CHECK(ColumnName>=18);
```
```
ALTER TABLE TableName DROP ColumnName;
```
* Copy Table Process:
  - Identify the database and table to be copied.
  - Determine the column to be copied.
  - Build a new table using CREATE TABLE.
  - Structure the new table with SELECT command.

* Copy table from the same database:
```
CREATE TABLE NewTableName SELECT ColumnName FROM ExistingTableName;
```
* Copy table from the different database:
```
CREATE TABLE DatabaseXNewTableName SELECT Columns FROM DatabaseYExistingTable;
```

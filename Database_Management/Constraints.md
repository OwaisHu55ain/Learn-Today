## MySQL Constraints

* **MySQL Constraints:** Rule that can be applied to a table or a group of columns to enforce certain restriction on the data that can be stored in those columns.

* There are three types of constraints:

  **1. Key Constraints:** Apply rules to key constraints.

  **2. Domain Constraints:** Special rules defined for values that can be stored for a specific columns.

  **3. Referential Integrity Constraints:** Establish rules for referential keys.

    - Referencing Table: This table holds the primary key.
    - Referenced Table: This table contains the foreign key.

* **Common Constraints:** Following constraints ensure the consistency and integrity in Data.

  - **UNIQUE:** Ensures that the value in a column are unique.
  - **Primary Key:** One or more column values must always be unique and they cannot accept a null value.
  - **FOREIGN KEY:** Link between two tables.
  - **NOT NULL:** Column cannot contain null value.
  - **CHECK:** Specifies a condition that must be true for the data in a column.
  - **ON DELETE CASCADE:** When a row is deleted in parent table all the row in child table is also deleted automatically.
  - **ON UPDATE CASCADE:** When a row is updated in parent table all the row in child is also updated automatically.


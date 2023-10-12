In relational database systems, the "ON DELETE" and "ON UPDATE" clauses for foreign keys are used to define how changes to the primary key in a parent table affect the corresponding foreign key values in a child table. These actions ensure data integrity between related tables.


1. **ON DELETE**:
   This clause specifies what should happen when a referenced row in the parent table (i.e., a row containing a primary key value) is deleted.

   - **CASCADE**: If a row in the parent table is deleted, then the corresponding rows in the child table with a matching foreign key will also be deleted.
   - **SET NULL**: If a row in the parent table is deleted, then the foreign key values in the corresponding child table rows are set to NULL. This requires the foreign key column to be nullable.
   - **SET DEFAULT**: If a row in the parent table is deleted, then the foreign key values in the corresponding child table rows are set to their default values.
   - **NO ACTION**: If a row in the parent table is deleted and there are matching rows in the child table, the deletion will be refused. This ensures referential integrity.
   - **RESTRICT**: Similar to NO ACTION, but the check is made immediately, not deferred until the end of the transaction.

2. **ON UPDATE**:
   This clause specifies what should happen when a primary key value in the parent table is updated.

   - **CASCADE**: If a primary key value in the parent table is updated, then the corresponding foreign key values in the child table are also updated to match the new value.
   - **SET NULL**: If a primary key value in the parent table is updated, then the foreign key values in the corresponding child table rows are set to NULL.
   - **SET DEFAULT**: If a primary key value in the parent table is updated, then the foreign key values in the corresponding child table rows are set to their default values.
   - **NO ACTION**: If a primary key value in the parent table is updated and there are matching rows in the child table, the update will be refused. This ensures referential integrity.
   - **RESTRICT**: Similar to NO ACTION, but the check is made immediately, not deferred until the end of the transaction.

The primary goal of these actions is to maintain data integrity across tables. For example, you wouldn't want orphaned rows in a child table that have no corresponding parent, or you might want to ensure that changes to a parent table cascade down to related child tables to keep the data synchronized.
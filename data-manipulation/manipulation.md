## SQL Data Manipulation
- Introduction to CRUD operations

## Data Manipulation Language (DML)
- Makes changes to the data stored within database tables

## COMMON DATA MANIPULATION
- INSERT
- UPDATE
- DELETE

## SELECT 
- Returns a result set of data from the database
## INSERT
- Adds new records to a table
## UPDATE 
- Updates an existing row or set of rows
## DELETE
-Removes an existing row or set of rows

# EXAMPLES

## INSERT
```sql
INSERT INTO tablename(column1, column2, ..)
VALUES (value1, value2)
```
```sql
INSERT INTO Customer(CustomerID, FirstName, ..)
VALUES ('9999', 'Carol')
```
## UPDATE
```sql
UPDATE tablename SET column1 = new_value
WHERE column1 = existing_value
```
```sql
UPDATE Customer SET Phone = '123456789'
WHERE CustomerID = 9999
```

## DELETE
```sql
DELETE FROM tablename
WHERE column1 = existing_value
```
```sql
DELETE FROM Customer
WHERE CustomerID = 9999
```
## SQL TRANSACTIONS
- BEGIN TRANSACTION
- COMMIT 
- ROLLBACK
## Transact-SQL
- Dealing with large transactions
- Referential integrity
- Error handling


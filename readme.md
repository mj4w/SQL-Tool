# SQL_GUIDE -mj4w

## SQL JOINS

<b>INNER JOIN</b> 
- Retrieves records with matching values in both tables
```sql 
   SELECT * FROM A INNER JOIN B ON A.key = B.key
```
<hr/>  
<b>LEFT JOIN</b>
- Retrieves all records from the left table and matching records from the right table

```sql
SELECT * FROM A LEFT JOIN B ON A.key = B.key
```

<hr/>
<b>LEFT JOIN with NULL Check</b>
- Filters only the records where there is no match in the right table (NULL values)

```sql
SELECT * FROM A LEFT JOIN B ON A.key = B.key WHERE B.key IS NULL 
```
<hr/>

<b>RIGHT JOIN</b>
- Retrieves all records from the right table and matching records 

```sql
SELECT * FROM A RIGHT JOIN B ON A.key = B.key 
```
<hr/>

<b>RIGHT JOIN with NULL Check</b>
- Filters only the records where there is no match in the left table (NULL VALUES)

```sql
SELECT * FROM A RIGHT JOIN B ON A.key = B.key WHERE A.key IS NULL 
```
<hr/>

<b>FULL JOIN</b>
- Retrieves all records when there is a match in either the left or right table

```sql
SELECT * FROM A FULL OUTER JOIN B ON A.key = B.key  
```
<hr/>

<b>FULL JOIN with NULL Check</b>
- Filters only the records where there is no match in either the left or right table ( NULL Values in either))

```sql
SELECT * FROM A FULL OUTER JOIN B ON A.key = B.key WHERE A.key IS NULL OR B.key is NULL 
```
<hr/>

## Rollback Retrieve All Deleted Data

```sql
DELETE from Customer where State = 'Texas';
ROLLBACK;
```
## Modify Columns 

```sql
ALTER TABLE new_db.organization MODIFY COLUMN stripe_id VARCHAR(255);
```
## ADD Column

```sql
ALTER TABLE table_name
ADD column_name datatype;
```

## Create Table

```sql
CREATE TABLE Users
(
   UserID int,
   FirstName varchar(100), 
   LastName varchar(100),
   City varchar(100)
);
```

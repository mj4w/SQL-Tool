# SQL_GUIDE 

### written by: Marcel James


- "A <b>database</b> is an organized collection of structured information or data, typically stored electronically in a computer system. <em>-Oracle Website</em>"

- "<b>Database Management System</b> A software application that helps store, load and update data in the database."

- "An <b>entity</b> is single unique object in the real world that is being mastered. <em>Examples of an entity are a single person, single product, or single organization</em> -IBM Website"

## Entities 

- <b>One-to-One</b> One entity directly relates to only other entity
- <b>One-to-Many</b> One entity has a relationship with one or more entities
- <b>Many-to-Many</b> More than one entity has a relationship with one or more other entities

## Entity-Relationship Diagram (ERD)
- An entity-relationship model, also called an entity-relationship diagram (ERD), is a graphical representation of entities and their relationships to each other.
<b>Contains //</b>
#### Primary Key
- Must be unique for each record
- Cannot contain null values
- Can be a composite of multiple fields
### Referential Integrity
- Each foreign key is a reference to a primary key
- Keeps tables in the relationship with each other

## Basic Syntax
- <b>SELECT</b> field_name
- <b>FROM</b> table-name


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

## Data Structure

- A <b>relational database</b> is an organization of related tables
- A <b>table</b> consists of columns and rows
- Each <b>row</b> represents an instance of an entity
- Each <b>column</b> represents an attribute fo the entity instance

> Note!  
>  ALL FIELDS ARE NOT MADE THE SAME!

## Data Type
- The <b>data type</b> of a column defines what values the column can hold

## Common Data Types

- INT
- VARCHAR
- NVARCHAR
- DATE
- DATETIME
- FLOAT
- DOUBLE

## Column Constraints 
- Specify rules for the data at the <b>column</b> level

## Column Constraints 
- <b>NULL</b> or <b>NOT NULL</b> in each column
- <b>UNIQUE</b>
- <b>PRIMARY KEY, FOREIGN KEY</b>
- <b>DEFAULT</b> 

## Data Constraint Example

```sql
CREATE TABLE Customer(
    CustomerID int(4) NOT NULL,
    FirstName nvarchar(50) NOT NULL,
    LastName nvarchar(50) NOT NULL,
    Email nvarchar(50) NULL,
    Phone nvarchar(50) NULL,
    Address nvarchar(50) NOT NULL,
    City nvarchar(50) NOT NULL,
    State nvarchar(50) NOT NULL,
    Zipcode int NOT NULL
)
```

##  Data Types
- <b>Data types</b> ensure that the data is kept consistent


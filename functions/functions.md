## Functions
- Built-in operations in SQL that return a value

## SQL Functions 
- Built into the database management system
- Can take in one or more arguments
- Functionality depends on data type
- Example <b><em>Function(Arg1,Arg2,..)</em></b>

## String Functions
- Modify character - and text-based data

## Common String Functions
- CONCAT()
- UPPER()
- LOWER()
- TRIM()
- REPLACE()

## SUBSTRING()
- Returns a part of a character string SUBSTRING(string,start,length)

```sql
SELECT FirstName, LastName
FROM Customer WHERE SUBSTRING(LastName,1,3) = "Smi"
```
## CONCAT()
- Joins two or more strings together CONCAT(string1,string2, ..., string_n)

```sql
SELECT CONCAT(FirstName, ' ', LastName) AS FULL_NAME
FROM Customer
```
## UPPER()
- Returns uppercase 
```sql
SELECT UPPER(CONCAT(FirstName, ' ', LastName)) AS FULL_NAME
FROM Customer
```

## LOWER()
- Returns lowercase 
```sql
SELECT LOWER(CONCAT(FirstName, ' ', LastName)) AS FULL_NAME
FROM Customer
```
## REPLACE()
- Replaces a substring with another substring REPLACE(string,old_string,new_string)
```sql
SELECT REPLACE(State, 'CA', 'California') AS FULL_STATE
FROM Customer
WHERE State = 'CA'
```
## TRIM()

- Removes specified characters from the start or end of a string TRIM(characters FROM string)

```sql
SELECT TRIM(
    'M'
    FROM ProductCode
) AS TrimmedProductCode
FROM Product
```

## Common Aggregate Functions 
- COUNT()
- AVG()
- MIN()
- MAX()
- SUM()

## COUNT()
- Returns the number of rows
```sql
SELECT COUNT(CustomerID) 
FROM Customer;
```

```sql
SELECT COUNT(DISTINCT(CustomerID)) 
FROM Customer;
```
## GROUP BY
- Groups rows that have the same value together into summary rows
```sql
SELECT State, 
    AVG(TotalDue) AS Avg_Due,
    MIN(TotalDue) AS Min_Due,
    MAX(TotalDue) AS Max_Due,
    SUM(TotalDue) AS Total_Sales
FROM Customer C 
JOIN Orders O ON O.CustomerID = C.CustomerID
GROUP BY State
ORDER BY Avg_Due DESC
```
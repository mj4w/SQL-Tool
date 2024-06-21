## Finding Duplicate Values
- Identify duplicate values in your data and how they can affect the data in your applications using the GROUP BY and HAVING clauses.

## Finding Insight in Aggregate Data
- GROUP BY 
- HAVING

## GROUP BY
- Applying aggregate functions

### Using GROUP BY
- <b>Group</b> rows together that have the same values
- <b>Aggregate</b> functions provide one data value summarized from many records 

## Aggregate Functions
- <b>COUNT()</b>: Number of rows
- <b>SUM()</b>: Sum of values 
- <b>AVG()</b>: Average of values
- <b>MIN()</b>: Minimum of values
- <b>MAX()</b>: Maximum of values

- A <b>duplicate</b> row happens if the record is not unique
- This means there are two or more rows that are exactly the same!

## HAVING Clause
- Additional filtering based on the results of aggregate functions 

### Example Code
```sql
SELECT FirstName, LastName, COUNT(1)
FROM Customer
GROUP BY FirstName, LastName
HAVING COUNT(1) > 1
```
- Retrieve all FirstName, LastName that have duplicate values

## Key Points to Remember 
- <b>WHERE</b> allows you to filter non-aggregate column data
- HAVING allows you to filter aggregate data like SUM() and COUNT()
- Helpful for identifying duplicate values in your data

## Using Aggregate Functions and Identifying Duplicate Records

- Create and summarize your data into groups
- Identify duplicate data
- Improve your data analysis and data applications!

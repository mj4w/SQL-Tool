# SQL-Tool

```SELECT * FROM A INNER JOIN B ON A.key = B.key```  
<b>INNER JOIN -> </b> Retrieves records with matching values in both tables

SELECT * FROM A LEFT JOIN B ON A.key = B.key 
LEFT JOIN -> Retrieves all records from the left table and matching records from the right table

SELECT * FROM A LEFT JOIN B ON A.key = B.key WHERE B.key IS NULL 
LEFT JOIN with NULL Check -> Filters only the records where there is no match in the right table (NULL values)

SELECT * FROM A RIGHT JOIN B ON A.key = B.key
RIGHT JOIN -> Retrieves all records from the right table and matching records from the left table

SELECT * FROM A RIGHT JOIN B ON A.key = B.key WHERE A.key IS NULL 
RIGHT JOIN with NULL Check -> Filters only the records where there is no match in the left table (NULL VALUES)

SELECT * FROM A FULL OUTER JOIN B ON A.key = B.key 
FULL JOIN -> Retrieves all records when there is a match in either the left or right table

SELECT * FROM A FULL OUTER JOIN B ON A.key = B.key WHERE A.key IS NULL OR B.key is NULL 
FULL JOIN with NULL Check -> Filters only the records where there is no match in either the left or right table ( NULL Values in either))

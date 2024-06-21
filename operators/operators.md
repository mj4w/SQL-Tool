## Comparison Operators 
- Compare values and return boolean (true or false)

### Common Comparison Operators
- Equal to (=)
- Not equal to (<>)
- Greater than (>), greater than or equal to <b>(>=)</b>
- Less than (<), less than or equal to (<=)

#### Example Code
```sql
SELECT * FROM
Orders WHERE CreationDate > '6/01/2016'
```


## Logical Operators
- Combine multiple boolean values and return a single boolean output of true or false

### Common Logical Operators
- AND
- OR
- ALL 
- IS 
- NOT
- LIKE
- BETWEEN
- IN 
- EXISTS
- DISTINCT

### Example Code 
```sql
SELECT * FROM Product
WHERE Variety = 'Blueberry'
AND Price < 2.00
```

## Arithmetic Operators
- Perform mathematical operations

### Common Arithmetic Operators
- Addition (+)
- Subtraction (-)
- Multiplication (*)
- Division (/)
- Modulo (%)

### Example Code
```sql
SELECT OrderItem.OrderId,
  Orders.TotalDue,
  SUM(Price * Quantity) as NewTotalDue
FROM OrderItem
  JOIN Product ON OrderItem.ProductID = Product.ProductID
  JOIN Orders ON OrderItem.OrderID = Orders.OrderID
GROUP BY OrderItem.OrderId,
  Orders.TotalDue
```

## Documentation
- A definition of the data in each column
- The source of the data in a column 
- How the data in each column is calculated
- The valid values allowed in a column 
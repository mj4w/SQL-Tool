## MySQL Data Types
- Date 
- DATETIME
- TIMESTAMP
- YEAR

DATE vs DATETIME

### DATE
- YYYY-MM-DD
### Datetime
- YYYY-MM-DD hh:mm:ss[.nnn]

- Separate by Category
```sql
SELECT Year(CreationDate), 
Month(CreationDate), 
Day(CreationDate)
FROM Orders
```

- Capture DateTime.now()
```sql
SELECT NOW() AS RIGHT_NOW
```

## Filtering Data by Dates

```sql
SELECT OrderID,
  CreationDate
FROM Orders
WHERE Month(CreationDate) = 5
  AND Year(CreationDate) = '2016'
```

- Between Keyboard
```sql
SELECT OrderID,
  CreationDate
FROM Orders
WHERE CreationDate BETWEEN '2016-05-01' and '2016-05-31'
ORDER BY CreationDate
```
- DateTime Now
```sql
SELECT OrderID, CreationDate
FROM Orders
Where CreationDate > Now()

```
```sql
SELECT OrderID, CreationDate
FROM Orders
Where Year(CreationDate) > (Year(Now()) - 10);
```
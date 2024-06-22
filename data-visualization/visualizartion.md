## Data  Visualization
- Incorporating SQL into your web app

## Plotly
- Open-source graphing library 
- Explore and manage data
- Provide insights 
- Build data apps in Python with Dash


## SQL FOR Visualization
```sql
SELECT 
DATENAME(month, [DATE]) AS [Order Month],
DATENAME(year, [DATE]) AS [Order Year],
CONCAT([FirstName], ' ', [LastName]) AS [Salesperson Name], 
Count(1) AS [Amount of Orders],
SUM(TotalDue) AS [Total Due]
FROM [V_Orders] O
JOIN [Salesperson] S ON O.SalespersonID = S.SalespersonID
GROUP BY 
DATENAME(month, [Date]),
DATENAME(year,[Date]),
CONCAT([FirstName], '', [LastName])
```
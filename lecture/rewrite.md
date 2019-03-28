# Rewrite SQL Query to Algebra

```sql
SELECT customerName, city, salesRepEmployeeNumber as rep 
FROM classicmodels.customers
WHERE creditLimit > 50000 AND country = 'France'
```

![latex]( https://latex.codecogs.com/svg.latex?\Pi_{customerName,city,rep}(\sigma_{creditLimit>50000\wedge%20country='France'}(\rho_{rep/salesRepEmployeeNumber}(customers)))      )

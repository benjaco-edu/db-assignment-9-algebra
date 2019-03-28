# Rewrite SQL Query to Algebra

## A

```sql
SELECT customerName, city, salesRepEmployeeNumber as rep 
FROM classicmodels.customers
WHERE creditLimit > 50000 AND country = 'France'
```

![latex]( https://latex.codecogs.com/svg.latex?\Pi_{customerName,city,rep}(\sigma_{creditLimit>50000\wedge%20country='France'}(\rho_{rep/salesRepEmployeeNumber}(customers)))      )

## B

Assume we have table A=(a,b,c) and table B=(x,y,z).

Write a join of table A and B where you join those rows where a has the same value y.

You should only use $\Pi,\sigma,\rho,$ and $\times$, that is - not use the join $\bowtie$ directly.


![latex]( https://latex.codecogs.com/svg.latex?\sigma_{a=y}(A\times%20B)   )

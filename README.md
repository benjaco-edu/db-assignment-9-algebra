# Assignment 09 Relational algebra

https://github.com/datsoftlyngby/soft2019spring-databases/blob/master/assignments/assignment9.md

Consider this query from the classic models:

```sql
select customers.customerName, offices.city as office_city
from customers, employees, offices
where 
	customers.salesRepEmployeeNumber = employees.employeeNumber and 
	employees.officeCode = offices.officeCode and
    customers.city = offices.city;
```

1. Rewrite it as an expression in relational algebra + 2. Add row counts to the subexpressions

![latex](https://latex.codecogs.com/svg.latex?\Pi_{customerName,office\_city}(\rho_{office\_city/office.city}(\sigma_{salesRepEmployeeNumber=employeeNumber}(customers^{122}\times%20(employees^{23}\bowtie%20offices^{7})^{23})^{2806})^{14}))


3. Rewrite to a better expression


![latex](https://latex.codecogs.com/svg.latex?\Pi_{customerName,office\_city}(\rho_{office_city/office.city}((\sigma_{salesRepEmployeeNumber=employeeNumber}(customers^{122}\times%20employees^{23}))^{14}\bowtie%20offices^{7})^{14}))

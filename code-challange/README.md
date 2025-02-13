# Code Challenge: Who are your top customers?
![image](https://github.com/user-attachments/assets/3a55b5d1-c8f7-4d35-933e-4ca38348e6d3)
![image](https://github.com/user-attachments/assets/66c145af-2e85-43fb-8d88-aa6f9ee3d48b)
## Task 
![image](https://github.com/user-attachments/assets/b0c542f0-2c86-4f3d-907d-d11f2a3ce63e)
## Queries 
```
select o.CUSTOMERID, c.FIRSTNAME, c.LASTNAME, sum(d.PRICE) as TotalSpend from customers c 
join orders o on c.CUSTOMERID = o.CUSTOMERID
join ordersdishes od on o.orderid = od.orderid
join dishes d on od.DISHID = d.DISHID 
Group BY o.CUSTOMERID
having TotalSpend > 450
order by TotalSpend desc;
```
## Result 
![image](https://github.com/user-attachments/assets/0fe5e028-47d9-416a-9b99-0fe71ba4f5be)

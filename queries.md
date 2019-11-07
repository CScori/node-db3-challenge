# Database Queries

### Display the ProductName and CategoryName for all products in the database. Shows 76 records.
select p.ProductName as Product, c.CategoryName as Compnay
from Product as p
join Category as c 
on p.CategoryId = c.id;
### Display the OrderID and ShipperName for all orders placed before January 9, 1997. Shows 161 records.
select o.Id as [Order_num], s.CompanyName as shipper
from [Order] as o
join Shipper as s
order by ShippedDate less than 1997-09-01
### Display all ProductNames and Quantities placed on order 10251. Sort by ProductName. Shows 3 records.
select p.ProductName as Product, od.Quantity as Number 
from Product as p
join OrderDetail as od
on od.OrderId = od.ProductId
where od.OrderId = 10251
### Display the OrderID, CustomerName and the employee's LastName for every order. All columns should be labeled clearly. Displays 196 records.
select o.Id as ORDER_ID,
c.ContactName as CustomerName,
e.LastName as Employee
from [Order] as o
join Customer as c
on o.CustomerId = c.Id
join Employee as e
on o.EmployeeId = e.Id
### (Stretch)  Displays CategoryName and a new column called Count that shows how many products are in each category. Shows 9 records.

### (Stretch) Display OrderID and a  column called ItemCount that shows the total number of products placed on the order. Shows 196 records. 
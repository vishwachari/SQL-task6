select productcode, productname, buyprice
from products
where buyprice = (select max(buyprice) from products);


select customernumber, customername
from customers
where customernumber in (select distinct customernumber from orders);


select c.customernumber, c.customername
from customers c
where exists (select 1
              from orders o
              where o.customernumber = c.customernumber);


select c.customernumber, c.customername
from customers c
where c.customernumber in (
    select o.customernumber
    from orders o
    where (select avg(quantityordered * priceeach)
           from orderdetails od
           where od.ordernumber = o.ordernumber) > 5000
);


select customernumber, customername, total_sales
from (
    select c.customernumber, c.customername,
           sum(od.quantityordered * od.priceeach) as total_sales
    from customers c
    join orders o on c.customernumber = o.customernumber
    join orderdetails od on o.ordernumber = od.ordernumber
    group by c.customernumber, c.customername
) as sales_summary
order by total_sales desc
limit 5;


select e.employeenumber, e.firstname, e.lastname
from employees e
where e.officecode = (
    select officecode from offices where city = 'boston'
);


select productcode, productname
from products
where productcode not in (
    select distinct productcode
    from orderdetails
);



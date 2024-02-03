## SELECT
```mysql
SELECT col1, col2 FROM table_name WHERE conditions (ans/or) ORDER BY col_name (default:asc/ desc)
SELECT DISTINCT -> unique values only
SLEECT col_name as different_name
```

## ALTER TABLE
- 
## JOINS
- INNER -> common in both
- LEFT -> includes all from left table and common
- RIGHT -> includes all from right table and common
- OUTER -> includes all, left right and common
```mysql
SELECT Orders.OrderID, Customers.CustomerName, Orders.OrderDate
FROM Orders
INNER JOIN Customers ON Orders.CustomerID=Customers.CustomerID;
```
## LENGTH() function
```mysql
SELECT LENGTH(CustomerName) AS LengthOfName
FROM Customers;
```
eg: col-> content and its length should be less than 15
```mysql
SELECT tweet_id FROM Tweets WHERE LENGTH(content)>15
```

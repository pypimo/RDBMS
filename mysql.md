## SELECT
```mysql
SELECT col1, col2 FROM table_name WHERE conditions (ans/or) ORDER BY col_name (default:asc/ desc)
SELECT DISTINCT -> unique values only
SELECT col_name as different_name
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
FROM Orders INNER JOIN Customers
ON Orders.CustomerID=Customers.CustomerID;
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
## col present in one table but not in another
- https://explainextended.com/2009/09/18/not-in-vs-not-exists-vs-left-join-is-null-mysql/
- and also count such entries
- https://leetcode.com/submissions/detail/1164825146/
```
SELECT v.customer_id, COUNT(*) AS count_no_trans
FROM Visits v LEFT JOIN Transactions t
ON v.visit_id=t.visit_id
WHERE t.visit_id IS NULL 
GROUP BY v.customer_id (imp else count(*) just counts all rows)
```
# CALC USING COLS
https://www.tutorialspoint.com/how-to-calculate-value-from-multiple-columns-in-mysql
## mutliple queries

## using join

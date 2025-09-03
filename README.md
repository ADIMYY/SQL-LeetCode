# LeetCode SQL Solutions

This repository contains my solutions to **LeetCode SQL problems**.  
The goal of this repo is to **practice SQL queries**, improve my problem-solving skills, and track my progress over time.

I will keep updating this repository regularly as I solve more SQL problems.
---

💡 Feel free to check out the solutions, suggest improvements, or discuss alternative approaches!

---
1 - [1757. Recyclable and Low Fat Products](https://leetcode.com/problems/recyclable-and-low-fat-products/description/?envType=study-plan-v2&envId=top-sql-50)
```SQL
SELECT product_id FROM Products 
WHERE low_fats = 'Y' 
AND recyclable = 'Y';
```
---

2 - [584. Find Customer Referee](https://leetcode.com/problems/find-customer-referee/description/?envType=study-plan-v2&envId=top-sql-50)
```SQL
SELECT name FROM Customer
WHERE referee_id != 2 OR 
referee_id IS NULL;
```
---

3 - [595. Big Countries](https://leetcode.com/problems/big-countries/description/?envType=study-plan-v2&envId=top-sql-50)
```SQL
SELECT name, population, area FROM World
WHERE area >= 3000000 OR
population >= 25000000;
```
---

4 - [1148. Article Views I](https://leetcode.com/problems/article-views-i/description/?envType=study-plan-v2&envId=top-sql-50)
```SQL
SELECT DISTINCT author_id AS id 
FROM Views
WHERE author_id = viewer_id
ORDER BY author_id;
```

---

5 - [1683. Invalid Tweets](https://leetcode.com/problems/invalid-tweets/description/?envType=study-plan-v2&envId=top-sql-50)
```SQL
SELECT tweet_id FROM Tweets 
WHERE LENGTH(content) > 15;
```

---

6 - [1378. Replace Employee ID With The Unique Identifier](https://leetcode.com/problems/replace-employee-id-with-the-unique-identifier/description/?envType=study-plan-v2&envId=top-sql-50)
```SQL
SELECT eu.unique_id, e.name FROM Employees AS e
LEFT JOIN EmployeeUNI AS eu
ON e.id = eu.id;
```

---

7 - [1068. Product Sales Analysis I](https://leetcode.com/problems/product-sales-analysis-i/description/?envType=study-plan-v2&envId=top-sql-50)
```SQL
SELECT p.product_name, s.year, s.price FROM Sales AS s
INNER JOIN Product AS p
ON s.product_id = p.product_id;
```

---

8 - [1581. Customer Who Visited but Did Not Make Any Transactions](https://leetcode.com/problems/customer-who-visited-but-did-not-make-any-transactions/description/?envType=study-plan-v2&envId=top-sql-50)
```sql
SELECT V.customer_id, COUNT(V.visit_id) AS count_no_trans
FROM Visits V
LEFT JOIN Transactions T ON V.visit_id = T.visit_id
WHERE T.transaction_id IS NULL
GROUP BY V.customer_id;
```

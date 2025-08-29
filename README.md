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

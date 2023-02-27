# TASK 1
```SQL
SELECT * FROM salesman
WHERE city = 'Paris' or city = 'Rome'
```
![image](https://user-images.githubusercontent.com/122611553/221504616-0c02c953-836b-4a2f-bbb0-e445343c20d0.png)

# TASK 3 
```SQL
SELECT * FROM salesman
WHERE NOT city = 'Paris' or city = 'Rome'
```
![image](https://user-images.githubusercontent.com/122611553/221505010-0982de49-b3a3-4fef-8b53-e6e30230e510.png)

# TASK 4
```SQL
SELECT * FROM customer
WHERE customer_id IN(3007, 3008, 3009)
```
![image](https://user-images.githubusercontent.com/122611553/221505883-a3fee714-054d-471f-b0ab-1302a66ce1d0.png)

# TASK 5
```SQL
SELECT * FROM salesman
WHERE commission BETWEEN 0.12 AND 0.14
```
![image](https://user-images.githubusercontent.com/122611553/221506471-0ada891c-35eb-4498-81d0-bfdc20ba061c.png)

# TASK 6
```SQL
SELECT * FROM orders 
WHERE (purch_amt BETWEEN 500 AND 4000) 
AND NOT purch_amt IN(948.50,1983.43)
```
![image](https://user-images.githubusercontent.com/122611553/221507679-44e79819-5e06-499a-a197-a92677efd826.png)

# TASK 7
```SQL
SELECT * FROM salesman
WHERE name LIKE ('A%') OR name LIKE ('L%')
```
![image](https://user-images.githubusercontent.com/122611553/221510510-7fc382a8-76e4-46d1-a5e8-6ec201ba8523.png)

# TASK 9
```SQL
SELECT * FROM customer
WHERE cust_name LIKE 'B%'
```
![image](https://user-images.githubusercontent.com/122611553/221510932-3a59a870-21d9-4643-89f1-bfc3ae27b878.png)

# TASK 10
```SQL
SELECT * FROM customer
WHERE cust_name LIKE '%n'
```
![image](https://user-images.githubusercontent.com/122611553/221511353-fba21d00-e455-43b2-bd8c-5f3ea4374d87.png)




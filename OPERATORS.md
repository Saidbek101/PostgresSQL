# TASK 1 
```SQL
SELECT * FROM customer
WHERE grade > 100
```
![image](https://user-images.githubusercontent.com/122611553/221480822-77b6bf49-4067-4702-b9b6-4a316f521bf9.png)

# TASK 2
```SQL
SELECT * FROM customer
WHERE grade > 100 AND city = 'New York'
```
![image](https://user-images.githubusercontent.com/122611553/221482829-37acc016-a67c-47d9-a615-1250a1a31b16.png)

# TASK 3
```SQL
SELECT * FROM customer
WHERE grade > 100 OR city = 'New York'
```
![image](https://user-images.githubusercontent.com/122611553/221483194-b0c8eab1-6a82-49ba-9ff6-a7ead3c94691.png)

# TASK 4 
```SQL
SELECT * FROM customer
WHERE  NOT grade > 100 OR city = 'New York'
```
![image](https://user-images.githubusercontent.com/122611553/221484528-ba8f2949-7374-4dae-8075-214b060e5cfd.png)

# TASK 5
```SQL
SELECT * FROM customer
WHERE NOT (grade > 100 OR city = 'New York')
```
![image](https://user-images.githubusercontent.com/122611553/221484961-0770d84d-de17-4ae9-a127-87d139e531c2.png)

# TASK 6
```SQL
SELECT * FROM orders
WHERE NOT ((ord_date = '2012-09-10' OR salesman_id > 5005) OR purch_amt > 1000.00)
```
![image](https://user-images.githubusercontent.com/122611553/221486743-1be6a5e6-6e89-4bf3-a083-1dd1193db784.png)

# TASK 7
```SQL
SELECT * FROM salesman
WHERE commission > 0.10 AND commission < 0.12
```
![image](https://user-images.githubusercontent.com/122611553/221487508-adc27b75-692b-4960-8b19-28379deed107.png)

# TASK 8
```SQL
SELECT * FROM orders
WHERE purch_amt < 200 OR NOT ord_date >='2012-02-10' AND customer_id < 3009
```
![image](https://user-images.githubusercontent.com/122611553/221488521-b036f0b8-ee90-4011-887a-c1ddcaca536f.png)

# TASK 9 
```SQL
SELECT * FROM orders
WHERE NOT ord_date ='2012-08-17' OR  customer_id >= 3005 AND purch_amt > 1000
```
![image](https://user-images.githubusercontent.com/122611553/221492182-b559e284-fe84-4c5a-8785-9f1b116aecfa.png)

# TASK 10
```SQL
SELECT ord_no,purch_amt, 
(100*purch_amt)/6000 AS "Achieved %", 
(100*(6000-purch_amt)/6000) AS "Unachieved %" 
FROM  orders 
WHERE (100*purch_amt)/6000>50
```
![image](https://user-images.githubusercontent.com/122611553/221502475-01425111-4fca-42c0-ad09-b7e15d834510.png)

# TASK 11
```SQL
SELECT * FROM emp_details
WHERE emp_lname ='Dosni' OR emp_lname= 'Mardy'
```
![image](https://user-images.githubusercontent.com/122611553/221503060-dea4c934-2ad0-443f-9b27-d8b775712286.png)

# TASK 12
```SQL
SELECT * FROM emp_details
WHERE emp_dept = 47 OR emp_dept = 63
```
![image](https://user-images.githubusercontent.com/122611553/221503326-36d56bdd-30cd-41db-9d7f-cc8962d992ec.png)



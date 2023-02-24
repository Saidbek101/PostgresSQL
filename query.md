# TASK 1
```sql
SELECT * FROM categories
```
![image](https://user-images.githubusercontent.com/122611553/221135750-1ecde4c9-95cf-4eab-aadf-cd9d327c0135.png)

# TASK 2  
SELECT category_name FROM categories

![image](https://user-images.githubusercontent.com/122611553/221135883-69a1cc67-66b2-4cec-9deb-a21a0acc528c.png)

# TASK 3
SELECT category_name AS ISMI
FROM categories

![image](https://user-images.githubusercontent.com/122611553/221135981-afa83302-c7f3-4808-9fde-94b22af591d0.png)

#TASK 4
SELECT * FROM categories
WHERE category_name = 'Confections'

![image](https://user-images.githubusercontent.com/122611553/221136133-c75ab531-1933-41dc-b193-3ba979be6b62.png)

# TASK 5 
SELECT * FROM categories
WHERE category_name = 'Produce' or category_name = 'Seafood'

![image](https://user-images.githubusercontent.com/122611553/221136216-f17dd0ee-e039-4f5e-ab60-2d02772c295a.png)

# TASK 6
SELECT *  FROM categories
WHERE category_id in (6,7,8)

![image](https://user-images.githubusercontent.com/122611553/221136317-77b0e652-1042-4f92-91db-80f4ab07faf6.png)

# TASK 7 
SELECT * FROM categories
ORDER BY description DESC;

![image](https://user-images.githubusercontent.com/122611553/221136411-63e28508-c070-472d-90de-a972ad4ac4f4.png)

# TASK 8
SELECT * FROM customers

![image](https://user-images.githubusercontent.com/122611553/221136566-3dcbf2d6-1328-4d8c-b960-fbc4a60c6d72.png)

# TASK 9
SELECT
    customer_id as "Mijoz ID",
    company_name as "Kompaniya nomi",
    contact_name as "Kontakt nomi",
    contact_title as "Lavozimi",
    address as "Manzili",
    city as "Shahri",
    region as "Hududi",
    postal_code as "Postal kodi",
    country as "Davlati",
    phone as "Telefoni",
    fax as "Faks"
FROM customers

![image](https://user-images.githubusercontent.com/122611553/221136684-fcbd5147-c74c-4409-be24-b583b279d8ea.png)

# TASK 10
SELECT * FROM customers
WHERE contact_title = 'Owner'

![image](https://user-images.githubusercontent.com/122611553/221136807-635ed42f-baad-4d39-af09-6bd0c8510a49.png)

# TASK 11
SELECT * FROM customers
WHERE city = 'London'

![image](https://user-images.githubusercontent.com/122611553/221136883-62420239-3309-41f9-b6d3-47a2263860e6.png)

# TASK 12
SELECT * FROM customers
WHERE  region IS NULL

![image](https://user-images.githubusercontent.com/122611553/221137003-3b130cd4-d742-4805-b84f-f87c13eb2daa.png)

# TASK 13
SELECT * FROM customers
WHERE region IS NOT NULL

![image](https://user-images.githubusercontent.com/122611553/221137122-eba6f5ca-1f9d-42d0-9695-d08f52ed4457.png)

# TASK 14
SELECT * FROM customers
WHERE country = 'Germany'

![image](https://user-images.githubusercontent.com/122611553/221137258-e423764c-6bb5-4e6b-bfc2-671cb29c8ce3.png)

# TASK 15
SELECT COUNT(*) FROM customers
WHERE country = 'Germany'

![image](https://user-images.githubusercontent.com/122611553/221137372-9f3493af-8c66-473f-8772-afb159315784.png)

# TASK 16
SELECT * FROM customers
WHERE fax IS NOT NULL ORDER BY contact_name

![image](https://user-images.githubusercontent.com/122611553/221137579-c76a7dbc-6507-441d-9597-1d205ebd92bf.png)

# TASK 17 
SELECT * FROM employees

![image](https://user-images.githubusercontent.com/122611553/221137677-11331baf-6b15-4776-809e-665167bd572d.png)

# TASK 18
SELECT
    employee_id AS "Mijoz ID",
    last_name AS "Kompaniya nomi",
    first_name AS "Kontakt nomi",
    title AS "Lavozimi",
    title_of_courtesy AS "Manzili",
    birth_date AS "Shahri",
    hire_date AS "Hududi",
    address  AS "Postal kodi"
FROM employees

![image](https://user-images.githubusercontent.com/122611553/221137782-60cccd32-e0c7-45de-88dd-d2dd6d9b2094.png)

# TASK 19
SELECT * FROM employees
WHERE title_of_courtesy = 'Mr.' ORDER BY first_name

![image](https://user-images.githubusercontent.com/122611553/221137875-806c7249-e079-4500-abf9-52ea66c0f535.png)

# TASK 20
SELECT count(*) FROM employees
WHERE title = 'Sales Representative'

![image](https://user-images.githubusercontent.com/122611553/221137967-111859aa-3523-44ce-8ded-3df45aa7788c.png)

# TASK 21
SELECT * FROM employees
WHERE hire_date BETWEEN  '1994-01-01' AND '1994-12-31'

![image](https://user-images.githubusercontent.com/122611553/221138032-7b9b32d2-b2a3-448e-a456-4052a289ab19.png)

# TASK 22
SELECT * FROM employees
WHERE region IS NOT NULL  ORDER BY  first_name DESC

![image](https://user-images.githubusercontent.com/122611553/221138106-d652c058-e70f-4a21-9f01-994849443fac.png)

# TASK 23
SELECT * FROM orders
WHERE customer_id = 'VINET'

![image](https://user-images.githubusercontent.com/122611553/221138220-dce87a1f-81f0-44bc-b078-6d25a5c577be.png)

# TASK 24
SELECT * FROM orders
WHERE order_date BETWEEN '1996-01-01' AND '1996-12-31'

![image](https://user-images.githubusercontent.com/122611553/221138323-e9d488f2-ef7c-4507-a9df-b31955a407a1.png)

# TASK 25
SELECT * FROM orders
WHERE ship_region IS NOT NULL

![image](https://user-images.githubusercontent.com/122611553/221138482-1d8f9feb-e4b0-4fa7-b1fd-86ee00b217f7.png)

# TASK 26
SELECT * FROM orders
WHERE order_id BETWEEN '10300' AND '10400'

![image](https://user-images.githubusercontent.com/122611553/221138599-0e837dad-1e0c-41e2-b99e-c7c936a5592b.png)

# TASK 27
SELECT SUM(unit_price) FROM order_details

![image](https://user-images.githubusercontent.com/122611553/221138670-c3ddb466-3755-4143-ae0d-9c86c36f00e1.png)

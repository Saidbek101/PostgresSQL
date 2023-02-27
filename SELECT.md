# TASK 1 
```sql
SELECT * FROM salesman
```
![image](https://user-images.githubusercontent.com/122611553/221420731-e5ce5e96-de55-4b59-b9a9-945fbe3671aa.png)

# TASK 2
```sql
SELECT 'This is SQL Exercise, Practice and Solution'
```
![image](https://user-images.githubusercontent.com/122611553/221421074-39593b26-ba86-414a-b408-76ea141cf47a.png)

# TASK 3
```sql
SELECT 10, 15, 20;
```
![image](https://user-images.githubusercontent.com/122611553/221421473-9ca24bba-0cf5-4347-9bd5-3ff7f7045c8e.png)

# TASK 4 
```sql
SELECT 7 + 5
```
![image](https://user-images.githubusercontent.com/122611553/221421575-2e5e2454-a32c-413b-91fb-ae402a64f41f.png)

# TASK 5
```sql
SELECT 7 - 5 + 5 * 4
```
![image](https://user-images.githubusercontent.com/122611553/221421695-a8af4ef2-6dbf-47a7-b3c8-6b3f95632692.png)

# TASK 6
```sql
SELECT name, commission FROM salesman 
```
![image](https://user-images.githubusercontent.com/122611553/221421853-62400485-2e12-4722-9833-782e72e5d992.png)

# TASK 7
```sql
SELECT ord_date, salesman_id, ord_no, purch_amt
FROM orders 
```
![image](https://user-images.githubusercontent.com/122611553/221422008-ed386a27-6838-46a6-a3ff-f4dba7edb8e3.png)

# TASK 8
```sql
SELECT DISTINCT salesman_id
FROM orders 
```
![image](https://user-images.githubusercontent.com/122611553/221422179-df2ad0cd-0c54-44b7-a4fe-3ad8d5f414a1.png)

# TASK 9
```sql
SELECT * FROM salesman 
WHERE city = 'Paris'
```
![image](https://user-images.githubusercontent.com/122611553/221422405-153678d3-a2c3-4902-af13-02c6ac17b76a.png)

# TASK 10
```sql
SELECT * FROM customer
WHERE grade = 200
```
![image](https://user-images.githubusercontent.com/122611553/221422491-2b6804fc-9127-44c8-8aa4-9848fb0f9ae8.png)

# TASK 11
```SQL
SELECT * FROM orders
WHERE salesman_id = 5001
```
![image](https://user-images.githubusercontent.com/122611553/221422658-0ab4137c-5341-4ca2-ab08-0ed866ac2ceb.png)

# TASK 12
```SQL
SELECT year,subject,winner 
FROM nobel_win 
WHERE year=1970;
```
![image](https://user-images.githubusercontent.com/122611553/221470157-335590ac-1fcb-449c-b1b1-7bd88d35f18b.png)

# TASK 13
```SQL
SELECT year, winner FROM nobel_win 
WHERE year=1970 AND SUBJECT = 'Literature'
```
![image](https://user-images.githubusercontent.com/122611553/221470708-13d103b1-3b0f-4e53-b8db-b2d55f925b9d.png)

# TASK 14
```SQL
SELECT * FROM nobel_win 
WHERE winner = 'Dennis Gabor'
```
![image](https://user-images.githubusercontent.com/122611553/221471060-a2db1f12-cc3f-4e1c-b4f9-1d900da94287.png)

# TASK 15
```SQL
SELECT winner FROM nobel_win 
WHERE year >= 1950 AND subject = 'Physics'
```
![image](https://user-images.githubusercontent.com/122611553/221471455-6d25fc48-61c1-467f-80f7-1dd2812abc5f.png)

# TASK 16
```SQL
SELECT year, subject, winner, country
FROM nobel_win 
WHERE subject = 'Chemistry' AND year >= 1965 AND year <= 1975
```
![image](https://user-images.githubusercontent.com/122611553/221471943-27639c7a-7a0a-4e05-a3bd-0c3c8f6b5637.png)

# TASK 17
```SQL
SELECT * FROM nobel_win 
WHERE year > 1972 AND winner IN ('Menachem Begin', 'Yitzhak Rabin')
```
![image](https://user-images.githubusercontent.com/122611553/221472339-0c5e84eb-b44f-4b2b-8ffa-72d54e2c93f0.png)

# TASK 18
```SQL
SELECT * FROM nobel_win 
WHERE winner LIKE 'Louis %'
```
![image](https://user-images.githubusercontent.com/122611553/221472596-e621f92d-aa8e-47ff-9a7e-57007605cf2e.png)

# TASK 19
```SQL 
SELECT * FROM nobel_win 
WHERE (subject ='Physics' AND year=1970) UNION (SELECT * FROM nobel_win  WHERE (subject ='Economics' AND year = 1971 ))
```
![image](https://user-images.githubusercontent.com/122611553/221473039-4a811a06-fbcb-4909-a303-dcedcbf38833.png)

# TASK 20
```SQL
SELECT * FROM nobel_win 
WHERE year=1970 AND subject NOT IN ('Physiology', 'Economics')
```
![image](https://user-images.githubusercontent.com/122611553/221473339-f1c89a0d-2306-4744-bf24-a574db8aec60.png)

# TASK 21
```SQL
SELECT * FROM nobel_win 
WHERE (subject ='Physiology' AND year<1971) UNION (SELECT * FROM nobel_win WHERE (subject ='Peace' AND year>=1974))
```
![image](https://user-images.githubusercontent.com/122611553/221474303-32cfec57-c51e-4925-bc94-ab2f5cac9034.png)

# TASK 22
```SQL
SELECT * FROM nobel_win 
WHERE winner =  'Johannes Georg Bednorz'
```
![image](https://user-images.githubusercontent.com/122611553/221474811-a6f69be2-93f2-4167-a700-6e3bcba4775d.png)

# TASK 23
```SQL
SELECT * FROM nobel_win 
WHERE subject NOT LIKE 'P %'
ORDER BY year DESC, winner
```
![image](https://user-images.githubusercontent.com/122611553/221475120-a38aca4b-3173-4830-82f0-eb8b69a8159d.png)

# TASK 24
```SQL
SELECT * FROM nobel_win
WHERE year=1970 
ORDER BY
 CASE
    WHEN subject IN ('Economics','Chemistry') THEN 1
    ELSE 0
 END ASC,
 subject,
 winner
```
![image](https://user-images.githubusercontent.com/122611553/221475606-e25bace1-042a-446c-b058-2a1907637594.png)

# TASK 25
```SQL
SELECT * FROM item_mast
WHERE pro_price BETWEEN 200 AND 600
```
![image](https://user-images.githubusercontent.com/122611553/221475862-b2013f30-155d-41cf-8e23-58f49a332b3a.png)

# TASK 26
``` SQL
SELECT AVG(pro_price) FROM item_mast
WHERE pro_com = 16
```
![image](https://user-images.githubusercontent.com/122611553/221476170-eec87d82-19d5-4321-b1ba-26eb095a7e1d.png)

# TASK 27
```SQL
SELECT pro_name AS "Item Name", pro_price AS "Price in Rs."
FROM item_mast;
```
![image](https://user-images.githubusercontent.com/122611553/221477107-bb580bbc-493b-4762-9a99-9cf346444510.png)

# TASK 28
```SQL
SELECT pro_name, pro_price FROM item_mast
WHERE pro_price >= 250
ORDER BY pro_price DESC, pro_name
```
![image](https://user-images.githubusercontent.com/122611553/221477583-dbdb48e5-088f-4a72-a8e8-f44ddaa2e225.png)

# TASK 29
```SQL
SELECT AVG(pro_price), pro_com FROM item_mast
GROUP BY pro_com
```
![image](https://user-images.githubusercontent.com/122611553/221477832-d198c501-f1ad-4669-8b58-1bf90fccc56b.png)

# TASK 30
```SQL
SELECT pro_name, pro_price FROM item_mast
WHERE pro_price = (SELECT MIN(pro_price) FROM item_mast)
```
![image](https://user-images.githubusercontent.com/122611553/221478539-88fc07d0-8531-49d4-91e1-956fe9e0df1d.png)

# TASK 31
```SQL
SELECT DISTINCT emp_lname FROM emp_details
```
![image](https://user-images.githubusercontent.com/122611553/221478914-16d8f2bd-cfcb-44e4-bbe9-ff3f162d64a4.png)

# TASK 32
```SQL
SELECT * FROM emp_details
WHERE emp_lname = 'Snares'
```
![image](https://user-images.githubusercontent.com/122611553/221479172-d382a19e-ef47-476c-b182-8acf710ff086.png)

# TASK 33
```SQL
SELECT * FROM emp_details
WHERE emp_dept = 57
```
![image](https://user-images.githubusercontent.com/122611553/221479297-38f03140-10a6-41fe-bef4-76212b2c04b0.png)
 
 


# TASK 1
```SQL
SELECT E.first_name, E.last_name, 
       E.department_id, D.department_name 
        FROM employees AS E 
         JOIN departments AS D 
          ON E.department_id = D.department_id
```
![image](https://user-images.githubusercontent.com/122611553/222051948-6b377c8d-48ef-4f26-8837-f9cd7c6565aa.png)

# TASK 2
```SQL
SELECT E.first_name, E.last_name, 
       D.department_name, L.city, 
       L.state_province 
        FROM employees AS E 
         JOIN departments AS D 
          ON E.department_id = D.department_id
            JOIN locations L
             ON D.location_id = L.location_id
```
![image](https://user-images.githubusercontent.com/122611553/222052671-3d02a0cd-e3a0-4837-8a3b-7e4f9390a60f.png)

# TASK 3
```SQL
SELECT E.first_name, E.last_name, E.salary, 
       J.grade_level
        FROM employees AS E 
         JOIN job_grades AS J 
          ON E.salary BETWEEN J.lowest_sal AND 
             J.highest_sal
```
![image](https://user-images.githubusercontent.com/122611553/222070338-cca8fdb2-b3dd-4d80-8348-5a6d8fe573e1.png)

# TASK 4
```SQL
SELECT E.first_name, E.last_name, 
       E.department_id,  D.department_name 
         FROM employees AS E 
         JOIN departments AS D 
          ON E.department_id = D.department_id 
          AND E.department_id IN (80 , 40)
           ORDER BY E.last_name
```
![image](https://user-images.githubusercontent.com/122611553/222072725-2501f062-2639-47a2-bad7-f6b15ef77f7c.png)

# TASK 5
```SQL
SELECT E.first_name, E.last_name,
   D.department_name, L.city, L.state_province
     FROM employees AS E 
      JOIN departments AS D  
       ON E.department_id = D.department_id 
        JOIN locations AS L 
         ON D.location_id = L.location_id 
           WHERE E.first_name LIKE  '%z%'
```
![image](https://user-images.githubusercontent.com/122611553/222073499-2d91cdc8-c742-4262-9c47-3dd7d1695e7c.png)

# TASK 6
```SQL
SELECT E.first_name, E.last_name, D.department_id, D.department_name 
 FROM employees E 
   RIGHT OUTER JOIN departments D
     ON E.department_id = D.department_id
```
![image](https://user-images.githubusercontent.com/122611553/222075870-31f4b204-1bba-47aa-bf25-67de8b1b3591.png)

# TASK 7
```SQL
SELECT E.first_name, E.last_name, E.salary 
  FROM employees E 
   JOIN employees S
     ON E.salary < S.salary 
      AND S.employee_id = 182
```
![image](https://user-images.githubusercontent.com/122611553/222076923-9363e775-3811-4269-8b09-64a3c5330aa0.png)

# TASK 8
```SQL
SELECT E.first_name AS "Employee Name", 
   M.first_name AS "Manager"
     FROM employees E 
       JOIN employees M
         ON E.manager_id = M.employee_id
```
![image](https://user-images.githubusercontent.com/122611553/222079375-fad1a85d-1e51-43a9-8225-e2495c5491e4.png)

# TASK 9
```SQL
SELECT D.department_name, L.city, L.state_province
  FROM  departments D 
    JOIN locations L 
      ON  D.location_id = L.location_id
```
![image](https://user-images.githubusercontent.com/122611553/222079626-616cd3cf-c999-42b0-88ea-897115bf2733.png)

# TASK 10
```SQL
SELECT E.first_name, E.last_name, E.department_id, D.department_name 
  FROM employees E 
   LEFT OUTER JOIN departments D 
     ON E.department_id = D.department_id
```
![image](https://user-images.githubusercontent.com/122611553/222080339-011c4620-6846-40db-94fd-8ecfcd47a47c.png)



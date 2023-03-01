# TASK 1
```SQL
SELECT rev_name FROM reviewer
JOIN rating USING(rev_id)
WHERE rev_stars IS NULL
```
![image](https://user-images.githubusercontent.com/122611553/222087518-9b3ccee6-8dc5-4e9a-965f-b8974b9fe434.png)

# TASK 2
```SQL
SELECT act_fname,act_lname,role FROM actor 
	  JOIN movie_cast ON actor.act_id=movie_cast.act_id
		JOIN movie ON movie_cast.mov_id=movie.mov_id 
    AND movie.mov_title='Annie Hall'
```
![image](https://user-images.githubusercontent.com/122611553/222090006-87bd3c70-b49e-4e81-9a5d-f8f577e4729f.png)

# TASK 3
```SQL
SELECT dir_fname, dir_lname, mov_title FROM director
NATURAL JOIN movie_direction
NATURAL JOIN movie
NATURAL JOIN movie_cast
WHERE role  IS NOT NULL AND mov_title = 'Eyes Wide Shut'
```
![image](https://user-images.githubusercontent.com/122611553/222093280-2399c45b-3d9b-40a1-a41b-6abaae5dbd33.png)

# TASK 4
```SQL
SELECT dir_fname, dir_lname, mov_title FROM  director 
JOIN movie_direction 
  ON director.dir_id=movie_direction.dir_id
JOIN movie 
  ON movie_direction.mov_id=movie.mov_id
JOIN movie_cast 
  ON movie_cast.mov_id=movie.mov_id
  WHERE role='Sean Maguire'
```
![image](https://user-images.githubusercontent.com/122611553/222095009-f58446bd-a070-4a36-bf93-413b95699087.png)

# TASK 5 
```SQL
SELECT act_fname, act_lname, mov_title, mov_year FROM actor
JOIN movie_cast 
  ON actor.act_id=movie_cast.act_id
JOIN movie 
  ON movie_cast.mov_id=movie.mov_id
WHERE mov_year NOT BETWEEN 1990 and 2000
```
![image](https://user-images.githubusercontent.com/122611553/222097562-77803f9b-bb07-49eb-8d63-69f54834e95b.png)

# TASK 6
```SQL
SELECT dir_fname,dir_lname, gen_title,count(gen_title)
FROM director
NATURAL JOIN movie_direction
NATURAL JOIN movie_genres
NATURAL JOIN genres
GROUP BY dir_fname, dir_lname,gen_title
ORDER BY dir_fname,dir_lname
```
![image](https://user-images.githubusercontent.com/122611553/222114693-b4c13563-6691-43c3-b3e7-cf38f8dc9b96.png)


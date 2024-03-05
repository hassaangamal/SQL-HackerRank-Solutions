# HackerRank - SQL and Database<br>Basic Select `20 problems`

## Revising the Select Query I
Problem Link: [Revising the Select Query I](https://hackerrank.com/challenges/revising-the-select-query/problem)

<summary>MySQL Solution</summary>

```sql
SELECT *
FROM CITY 
WHERE population > 100000 
AND countrycode = 'USA'
;
```

---

## Revising the Select Query II
Problem Link: [Revising the Select Query II](https://www.hackerrank.com/challenges/revising-the-select-query-2/problem?isFullScreen=true)

<summary>MySQL Solution</summary>

```sql
SELECT name
FROM CITY
WHERE countrycode = 'USA'
AND population >120000
;
```

---

## Select All

Problem Link: [Select All](https://www.hackerrank.com/challenges/select-all-sql/problem?isFullScreen=true)

<summary>MySQL Solution</summary>

```sql
SELECT * 
FROM city
;
```

---

## Select By ID

Problem Link: [Select By ID](https://www.hackerrank.com/domains/sql?filters%5Bsubdomains%5D%5B%5D=select&filters%5Bstatus%5D%5B%5D=solved)

<summary>MySQL Solution</summary>

```sql
SELECT *
FROM city
WHERE id = 1661
;
```

---
## Japanese Cities Attributes

Problem Link: [Japanese Cities Attributes](https://www.hackerrank.com/challenges/japanese-cities-attributes/problem?isFullScreen=true)
<summary>MySQL Solution</summary>

```sql
SELECT *
FROM city
WHERE countrycode = 'JPN'
;
```

---
## Japanese Cities' Names

Problem Link: [Japanese Cities' Names](https://www.hackerrank.com/challenges/japanese-cities-attributes/problem?isFullScreen=true)
<summary>MySQL Solution</summary>

```sql
SELECT name
FROM city
WHERE countrycode = 'JPN'
;
```

---
## Weather Observation Station 1

Problem Link: [Weather Observation Station 1](https://www.hackerrank.com/challenges/weather-observation-station-1/submissions)
<summary>MySQL Solution</summary>

```sql
SELECT city , state 
FROM station
;
```

---
## Weather Observation Station 3

Problem Link: [Weather Observation Station 3](https://www.hackerrank.com/challenges/weather-observation-station-3/problem)<summary>MySQL Solution</summary>

```sql
SELECT DISTINCT city
FROM station
WHERE id % 2 = 0
;
```

---
## Weather Observation Station 4

Problem Link: [Weather Observation Station 4](https://www.hackerrank.com/challenges/weather-observation-station-4/submissions/code/362171534)
<summary>MySQL Solution</summary>

```sql
SELECT COUNT(city) - COUNT(DISTINCT city) 
FROM station
;
```

---
## Weather Observation Station 5

Problem Link: [Weather Observation Station 5](https://www.hackerrank.com/challenges/weather-observation-station-5/problem?isFullScreen=true)
<summary>MySQL Solution</summary>

```sql
SELECT city, LENGTH(city) AS length
FROM station
ORDER BY length ASC, city
LIMIT 1
;
```

---
## Weather Observation Station 6

Problem Link: [Weather Observation Station 6](https://www.hackerrank.com/challenges/weather-observation-station-6/problem)
<summary>MySQL Solution</summary>

```sql
SELECT city 
FROM station
WHERE city regexp '^[aeiouAEIOU]'
;
```

---
## Weather Observation Station 7

Problem Link: [Weather Observation Station 7](https://www.hackerrank.com/challenges/weather-observation-station-7/problem?isFullScreen=true)
<summary>MySQL Solution</summary>

```sql
SELECT DISTINCT city
FROM STATION
WHERE city REGEXP '[aeiouAEIOU]$'
;
```

---
## Weather Observation Station 8

Problem Link: [Weather Observation Station 8](https://www.hackerrank.com/challenges/weather-observation-station-8/problem?isFullScreen=true)
<summary>MySQL Solution</summary>

```sql
SELECT DISTINCT city
FROM STATION
WHERE city REGEXP '^[aeiouAEIOU].*[aeiouAEIOU]$'
;
```

---
## Weather Observation Station 9

Problem Link: [Weather Observation Station 9](https://www.hackerrank.com/challenges/weather-observation-station-9/problem?isFullScreen=true)
<summary>MySQL Solution</summary>

```sql
SELECT DISTINCT city
FROM STATION
WHERE city NOT REGEXP '^[aeiouAEIOU]';
;
```

---
## Weather Observation Station 10

Problem Link: [Weather Observation Station 10](https://www.hackerrank.com/challenges/weather-observation-station-10/problem?isFullScreen=true)
<summary>MySQL Solution</summary>

```sql
SELECT DISTINCT city
FROM STATION
WHERE city NOT REGEXP '[aeiouAEIOU]$'
;
```

---
## Weather Observation Station 11

Problem Link: [Weather Observation Station 11](https://www.hackerrank.com/challenges/weather-observation-station-11/problem?isFullScreen=true)
<summary>MySQL Solution</summary>

```sql
SELECT DISTINCT city
FROM STATION
WHERE city NOT REGEXP '^[aeiouAEIOU].*[aeiouAEIOU]$'
;
```

---
## Weather Observation Station 12

Problem Link: [Weather Observation Station 12](https://www.hackerrank.com/challenges/weather-observation-station-12/problem?isFullScreen=true)
<summary>MySQL Solution</summary>

```sql
SELECT DISTINCT city
FROM STATION
WHERE city not REGEXP '^[aeiouAEIOU]' AND city not REGEXP '[aeiouAEIOU]$'
;
```

---
## Higher Than 75 Marks

Problem Link: [Higher Than 75 Marks](https://www.hackerrank.com/challenges/more-than-75-marks/problem?isFullScreen=true)
<summary>MySQL Solution</summary>

```sql
SELECT
    name
FROM 
    STUDENTS
WHERE 
    Marks > 75
ORDER BY 
    RIGHT(Name, 3), ID
;
```

---
## Employee Salaries

Problem Link: [Employee Salaries](https://www.hackerrank.com/challenges/salary-of-employees/problem?isFullScreen=true)
<summary>MySQL Solution</summary>

```sql
SELECT 
    name
FROM 
    Employee 
WHERE 
	months < 10 AND salary > 2000
ORDER BY 
	employee_id DESC
;
```

---
##  Employee Names
Problem Link: [Employee Names](https://www.hackerrank.com/challenges/name-of-employees/problem?isFullScreen=true)
<summary>MySQL Solution</summary>

```sql
SELECT 
    name
FROM
    Employee
order by 
    name
;
```
---

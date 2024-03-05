# HackerRank - SQL and Database<br>Aggregation `20 problems`

## Revising Aggregations - The Count Function
Problem Link: [Revising Aggregations - The Count Function](https://www.hackerrank.com/challenges/revising-aggregations-the-count-function/problem?isFullScreen=true)

<summary>MySQL Solution</summary>

```sql
SELECT
    COUNT(*)
FROM 
    city
WHERE
    population > 100000
;
```

---

## Average Population
Problem Link: [Average Population](https://www.hackerrank.com/challenges/average-population/problem?isFullScreen=true)
<summary>MySQL Solution</summary>

```sql
SELECT 
    ROUND(AVG(population),0)
FROM 
    city
;
```

---

## Revising Aggregations - Averages

Problem Link: [Revising Aggregations - Averages](https://www.hackerrank.com/challenges/revising-aggregations-the-average-function/problem?isFullScreen=true)
<summary>MySQL Solution</summary>

```sql
SELECT 
    AVG(population)
FROM 
    city
WHERE
    district = 'California'
;
```

---

## Japan Population

Problem Link: [Japan Population](https://www.hackerrank.com/challenges/japan-population/problem?isFullScreen=true)
<summary>MySQL Solution</summary>

```sql
SELECT 
    SUM(population)
FROM
    city
WHERE 
    countrycode = 'JPN'
;
```

---
## Population Density Difference

Problem Link: [Population Density Difference](https://www.hackerrank.com/challenges/population-density-difference/problem?isFullScreen=true)
<summary>MySQL Solution</summary>

```sql
SELECT MAX(population) - MIN(population)
FROM city
;
```

---

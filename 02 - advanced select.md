# HackerRank - SQL and Database<br>Advanced Select `5 problems`

## Type of Triangle
Problem Link: [Type of Triangle](https://www.hackerrank.com/challenges/what-type-of-triangle/problem?isFullScreen=true)
<summary>MySQL Solution</summary>

```sql
SELECT
    CASE WHEN A + B <= C OR A + C <= B OR B + C <= A THEN 'Not A Triangle'
    WHEN A = B AND A = C THEN 'Equilateral'
    WHEN A = B OR B = C OR A = C THEN 'Isosceles'
    ELSE 'Scalene'
END

FROM
    triangles
;
```

---

## The PADS
Problem Link: [The PADS](https://www.hackerrank.com/challenges/the-pads/problem?isFullScreen=true)
<summary>MySQL Solution</summary>

```sql
SELECT CONCAT(name , '(' , LEFT(occupation, 1) , ')' ) AS N
FROM OCCUPATIONS 
ORDER BY N
;
SELECT 
    CONCAT('There are a total of ', COUNT(occupation), ' ', LOWER(occupation), 's.')
FROM
    occupations
GROUP BY
    occupation
ORDER BY
    COUNT(occupation),
    occupation
;
```

---

## Occupations

Problem Link: [Occupations](https://www.hackerrank.com/challenges/occupations/problem?isFullScreen=true)
<summary>MySQL Solution</summary>

```sql
SELECT
    MAX(CASE WHEN occupation = 'Doctor' THEN name END) AS Doctor,
    MAX(CASE WHEN occupation = 'Professor' THEN name END) AS Professor,
    MAX(CASE WHEN occupation = 'Singer' THEN name END) AS Singer,
    MAX(CASE WHEN occupation = 'Actor' THEN name END) AS Actor

FROM (
    SELECT 
        name,
        occupation,
        ROW_NUMBER() OVER (PARTITION BY occupation ORDER BY name) as row_num
    FROM 
        OCCUPATIONS

)   AS occupation_rows
GROUP BY
    row_num
ORDER BY
    row_num
;
```

---

## Binary Tree Nodes

Problem Link: [Binary Tree Nodes](https://www.hackerrank.com/challenges/binary-search-tree-1/problem?isFullScreen=true)
<summary>MySQL Solution</summary>

```sql
SELECT
    N,
    CASE WHEN P IS NULL THEN 'Root' 
    WHEN N IN (SELECT DISTINCT P FROM BST) THEN 'Inner'
    ELSE 'Leaf' END AS NodeType
FROM BST
ORDER BY N
;
```

---
## New Companies

Problem Link: [New Companies](https://www.hackerrank.com/challenges/the-company/problem?isFullScreen=true)
<summary>MySQL Solution</summary>

```sql
SELECT
    company_code AS c,
    founder,
    (SELECT
        COUNT(DISTINCT lead_manager_code)
     FROM
        Lead_Manager
     WHERE
        c = company_code
    ),(SELECT
        COUNT(DISTINCT senior_manager_code)
     FROM
        Senior_Manager
     WHERE
        c = company_code
    ),(SELECT
        COUNT(DISTINCT manager_code )
     FROM
        Manager
     WHERE
        c = company_code
    ),(SELECT
        COUNT(DISTINCT employee_code ) 
     FROM
        Employee
     WHERE
        c = company_code
    )
FROM
    Company 
ORDER BY
    company_code

       
;
```

---

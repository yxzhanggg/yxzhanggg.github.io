---
title: /SQL
layout: page
permalink: /SQL/
---
The Stuctural Quary Language(SQL) is based on relational model, so basically it operates on the columns(selecting the attributes) and the rows(filtering the attributes).
# Paradigm
```sql
SELECT -- Return, last excution precedence
  <column>
FROM
  <table>;
-- Optional constraints, define virtual table
WHERE -- Global filter, first execution precedence
  <constraints expression>
GROUP BY -- Execute after WHERE
  <column>
HAVING -- Group filter, execute after GROUP
  <constraints expression>
ORDER BY
  <column> DESC/ASC
LIMIT <int-value>

```
# Aggregation function
Get multiple values, return single value
```sql
MIN();
MAX();
SUM();
AVG();
COUNT();
```
# Window function
Paradigm: aggregation + OVER expression
```sql
RANK(); -- Return rank of the entries inside OVER
SELECT
  <column>,
  <aggregation function>
    OVER (
     PARTITION BY <column>
    )
FROM
  <table>;
```


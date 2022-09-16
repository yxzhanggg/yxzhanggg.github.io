---
title: /SQL
layout: page
permalink: /SQL/
---
The Stuctural Quary Language(SQL) is based on relational model, so basically it operates on the columns(selecting the attributes) and the rows(filtering the attributes).
# Paradigm
```sql
SELECT -- return, last excution precedence
  <column>
FROM
  <table>;
-- Optional constraints
WHERE -- global filter, first execution precedence
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
-- Optional constraints
GROUP BY -- execute after WHERE
  <column>
HAVING -- group filter, execute after GROUP
  <constraints expression>
```
# Window function
Paradigm: aggregation + OVER expression
```sql

```


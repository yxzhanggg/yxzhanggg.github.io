---
title: /SQL
layout: page
permalink: /SQL/
---
# Paradigm
```sql
SELECT
  <column>
FROM
  <table>;
-- Optional constraints
WHERE -- global filter
  <constraints expression>
ORDER BY
  <column> DESC/ASC
LIMIT <int value>
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
GROUP BY -- after WHERE
  <column>
HAVING -- group filter
  <constraints expression>
```
# Window function
aggregation + OVER 


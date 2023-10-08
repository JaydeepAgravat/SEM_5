# JOIN

## 1. CROSS JOIN

```sql
SELECT * FROM T1
CROSS JOIN T2;
```

## 2. INNER JOIN

```sql
SELECT * FROM T1
INNER JOIN T2
ON T1.id = T2.id;
```

## 3. LEFT JOIN

```sql
SELECT * FROM T1
LEFT JOIN T2
ON T1.id = T2.id;
```

## 4. RIGHT JOIN

```sql
SELECT * FROM T1
RIGHT JOIN T2
ON T1.id = T2.id;
```

## 5. FULL OUTER JOIN

```sql
SELECT * FROM T1
LEFT JOIN T2
ON T1.id = T2.id

UNION

SELECT * FROM T1
RIGHT JOIN T2
ON T1.id = T2.id;

```

## 6. SELF JOIN

```sql
SELECT * FROM T1
INNER JOIN SELECT * FROM T1
ON T1.ID = T1.EID;
```

## SQL SET OPRERATIONS

```sql
SELECT * FROM T1
UNION
SELECT * FROM T2;
```

1. UNION
2. UNION ALL
3. INTERSECT
4. EXCEPT

## Joining on more than one column

```sql
SELECT * FROM T1
INNER JOIN T2
ON T1.id = T2.id AND T1.eyr = T2.cyr;
```

## Joining more than 2 tables

```sql
SELECT * FROM T1
INNER JOIN T2
ON T1.id = T2.id
INNER JOIN T3
ON T2.uid = T3.uid;
```

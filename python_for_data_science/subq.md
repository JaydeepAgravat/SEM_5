# SUBQUERY

## Types of SUBQUERY

1. Based on Result
    1. Scalar
    2. Row
    3. Table
2. Based on Working
    1. Independent
    2. Correlated

## Where Subquery Place

1. INSERT
2. UPDATE
3. DELETE
4. SELECT
    1. WHERE
    2. SELECT
    3. FROM
    4. HAVING

## SCALAR SUBQUERY

```sql
SELECT * FROM T1
WHERE C1 = (SELECT MAX(C1) FROM T1);
```

## ROW SUBQUERY

```sql
SELECT * FROM T1
WHERE C1 IN (SELECT C1 FROM T1
                WHERE C2 > AVG(C2));
```

## TABLE SUBQUERY

```sql
SELECT * FROM T1
WHERE (C1,C2) IN (SELECT C1,MAX(C2) 
                    FROM T1
                    GROUP BY C1);
```

## USAGE WITH WHERE

```sql
SELECT * FROM T1 M1
WHERE C1 > (SELECT AVG(C1) FROM T1 M2 WHERE M1.C2 = M1.C2)
```

## USAGE WITH SELECT

```sql
SELECT C1,C2,C3, 
(SELECT AVG(C3) FROM T1 M2 WHERE M2.C2 = M1.C2)
FROM T1 M1
```

## USAGE WITH FROM

```sql
SELECT C2, AVG(C3) FROM 
(SELECT C1, AVG(C3) FROM T3) T1 
JOIN T2
ON T1.C1=T2.C1
```

## USAGE WITH HAVING

```sql
SELECT * FROM T1
GROUP BY C1
HAVING AVG(C2) > (SELECT AVG(C2) FROM T1)
```

## USAGE WITH INSERT

```sql
INSERT INTO NT
(C1, C2)
SELECT C1, C2 FROM T1 WHERE C2 > (SELECT AVG(C2) FROM T1)
```

## USAGE WITH UPDATE

```sql
UPDATE NT
SET C3 = (
    SELECT SUM(C2) FROM T1
    WHERE T1.C1 = NT.C1
)
```

## USAGE WITH DELETE

```sql
DELETE FROM T1
WHERE C1 IN (
    {query|sq|ssq}
)
```

# MYSQL DQL command

## SELECT

```sql
    SELECT * FROM TB LIMIT 10;

    SELECT c1,c2 FROM TB;

    SELECT DISTINCT(c1) FROM TB;

    SELECT DISTINCT c1,c2 FROM TB;

    SELECT c1 FROM TB
    WHERE c2 IN ('APPLE','NOKIA');

    SELECT c1 FROM TB
    WHERE c2 NOT IN ('APPLE','NOKIA');

    SELECT c1 FROM TB
    WHERE c2 BETWEEN 10 AND 20;

    SELECT c1,SQRT(c2),rating/10 AS star FROM TB;

    SELECT c1, 'value' As new_tmp_col FROM TB;
```

## ORDER BY [SORTING]

```sql
    SELECT model,screen_size FROM db.phones
    WHERE brand_name = 'samsung'
    ORDER BY screen_size DESC
    LIMIT 3 ;

    SELECT model, num_front_cameras + num_rear_cameras as 'Total' FROM db.phones
    ORDER BY Total DESC
    LIMIT 3;

    SELECT model, battery_capacity FROM db.phones
    ORDER BY battery_capacity DESC
    LIMIT 1,1;

    SELECT model,rating FROM db.phones
    WHERE brand_name = 'apple'
    ORDER BY rating ASC
    LIMIT 3;

    SELECT brand_name, price FROM db.phones
    ORDER BY brand_name ASC, price DESC; 
```

## GROUP BY

```sql
    SELECT brand_name, COUNT(*) AS 'no_phones',
    ROUND(AVG(price)) AS 'avg price',
    MAX(rating) AS 'max rating',
    ROUND(AVG(screen_size), 2) AS 'screen size',
    ROUND(AVG(battery_capacity)) AS 'avg battery capacity'
    FROM db.phones
    GROUP BY brand_name
    ORDER BY no_phones DESC;

    SELECT has_5g,
    ROUND(AVG(price)) AS 'avg price',
    ROUND(AVG(rating)) AS 'avg rating'
    FROM db.phones
    GROUP BY has_5g

    SELECT brand_name,
    processor_brand,
    COUNT(*) AS 'no_phones',
    ROUND(AVG(primary_camera_rear)) AS 'res'
    FROM db.phones
    WHERE brand_name = 'samsung'
    GROUP BY brand_name, processor_brand

    SELECT brand_name, 
    ROUND(AVG(price)) AS 'avg_price'
    FROM db.phones
    GROUP BY brand_name
    ORDER BY avg_price DESC LIMIT 3

    SELECT brand_name, COUNT(*) AS 'no_phones'
    FROM db.phones
    WHERE has_nfc = 'True' AND has_ir_blaster = 'True'
    GROUP BY brand_name
    ORDER BY no_phones DESC LIMIT 3

    SELECT has_5g,
    ROUND(AVG(price)) AS 'avg_price'
    FROM db.phones
    WHERE brand_name = 'samsung'
    GROUP BY has_5g;
```

## HAVING

```sql
    SELECT brand_name, 
    COUNT(*) AS 'count', 
    ROUND(AVG(rating)) AS 'avg_rating'
    FROM db.phones
    GROUP BY brand_name
    HAVING count > 80
    ORDER BY avg_rating DESC

    SELECT brand_name, 
    round((ram_capacity)) AS 'avg_ram'
    FROM db.phones
    WHERE refresh_rate > 90 AND fast_charging_available = 1
    GROUP BY brand_name
    HAVING COUNT(*) > 10
    ORDER BY avg_ram DESC LIMIT 3;

    SELECT brand_name,
    COUNT(*) AS 'num_phones',
    AVG(price) AS 'avg_price',
    AVG(rating) AS 'avg_rating'
    FROM db.phones
    WHERE has_5g = 'True'
    GROUP BY brand_name
    having avg_rating > 70 AND num_phones > 10
    ORDER BY avg_price DESC;
```

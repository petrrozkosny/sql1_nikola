## ASSIGNMENT
1. Select location, date, prcp FRON data_new where year = 2019
2. Calculate average prcp by location from data_new
3. From all data (union) calculate average prcp by year, sort the output ascending by year
4. Get TOP 3 year, avg of prcp from all data (union) where country is Cesko (so you need to join dim_locations).
Hint: Use ORDER BY avg of prcp for sorting SELECT statement

## SOLUTION

```sql
SELECT location,date,prcp
FROM data_new
WHERE YEAR(date) = 2019
```
```sql
SELECT location,AVG(prcp)
FROM data_new
GROUP BY location
```
```sql
SELECT YEAR(date) AS year,AVG(prcp) AS avg_prcp
FROM
(
SELECT * FROM data_new
UNION ALL
SELECT * FROM data_old) da
GROUP BY YEAR(date)
ORDER BY year
```
```sql
SELECT TOP 3 location, MAX(prcp) AS "max_prcp"
FROM
(
SELECT * FROM data_new
UNION ALL
SELECT * FROM data_old) da
LEFT JOIN dim_locations AS dl ON dl.station = da.location
WHERE dl.country = 'Cesko'
GROUP BY location
ORDER BY max_prcp DESC
```
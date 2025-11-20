## SELECT
* Select all columns from the data_new  table.
* Select only the columns date and prcp from the data_new table.
* Select the column location (as "city"), date, and prcp from the data_new table.
* Select the year, month, and day from the date column, as well as the columns location and prcp.
## ORDER BY
* Select all columns from the data_new table and sort them by date in ascending order.
* Select the columns date, location, and prcp from the data_new table and sort them by prcp in descending order.
* Select the year and month from the date column, location, and prcp from the data_new table and sort them by year and month in ascending order.
## WHERE
* Select all columns from the data_new table where lokalita is 'RUZYNE'.
* Select the columns datum, lokalita, and srazky from the data_new table where lokalita is 'RUZYNE'.
* Select all columns from the data_new table where the year in datum is 2015.
* Select the columns lokalita, datum, and srazky from the data_new table where datum is from January 1, 2015, and lokalita is 'RUZYNE'.
* Select srazky from the data_new nova table where lokalita is 'RUZYNE' and the year in datum is 2015, sorted by srazky in descending order.
* Calculate the average (AVG) and maximum (MAX) srazky for the location 'RUZYNE' in the data_new table.

## GROUP BY
* Calculate the average prcp for each location in the data_new table.
* Calculate the average prcp for the location 'RUZYNE' by year in the data_new table.
* Calculate the total prcp  for each location for the year 2019 in the data_new table.
* Calculate the maximum and average prcp for each month of the year 2019 for the location 'RUZYNE' in the data_new table.
## HAVING
* Calculate the average prcp for each location in the data_new table and show only those locations where the average prcp is greater than 2.
* Calculate the average prcp for each year for the location 'RUZYNE' in the data_new table and show only those years where the average prcp is greater than 1, sorted by the average prcp in ascending order.
* Calculate the average prcp for each year and month for the location 'MOSNOV' in the data_new table and show only those months where the average prcp is greater than 1, sorted by year and month in ascending order.

## TOP
* Select the first 10 prcp values from the data_new table.
* Select the first 10 prcp  values from the data_new table and sort them by srazky in descending order.
* Calculate the total prcp for each month of the year 2019 for the location 'RUZYNE' in the data_new table and show only the top 3 months with the highest total srazky, sorted by total srazky in descending order.
* Select the first 10 dates from the data_new table for the location 'RUZYNE' and sort them by srazky in descending order.

## JOIN AND UNION
* Left join the tables data_new and dim_locations, then select the columns location,prcp,country

* Left join the tables data_new and dim_oblasti, and select the columnslocation,prcp,country where country = 'Cesko'.

* Left join the tables data_new and dim_locations, calculate the sum of prcp by year and country, and select country, yeaR, sum_prcp, sorted in asc order by country, year.

* Append (UNION ALL) the columns location,date,prcp from the tables data_new and data_old (without handling duplicates).

* Append (UNION ALL) the columns llocation,date,prcp from the tables data_new and data_old, filtering those before the union for location= 'RUZYNE'.
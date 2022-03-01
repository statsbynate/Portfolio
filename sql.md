### SQL

Below you will have a variety of SQL queries I've executed. These are mostly derived through work on [HackerRank](https://www.hackerrank.com). 

## Easy-Level Queries

![sql1](https://user-images.githubusercontent.com/97853367/156213439-f64b7373-e834-4f38-9bfb-2d0050db4639.jpg)

Task --> Query a count of the number of cities in CITY having a Population larger than 100,000.

SELECT COUNT(NAME) 
  FROM CITY 
  WHERE POPULATION >= 100000;

Task --> Query all columns for all American cities in the CITY table with populations larger than 100000. The CountryCode for America is USA.

SELECT *
    FROM CITY
    WHERE POPULATION >= 100000 AND COUNTRYCODE = 'USA'

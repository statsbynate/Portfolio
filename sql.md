### SQL

Below you will have a variety of SQL queries I've executed. These are mostly derived through work on [HackerRank](https://www.hackerrank.com). 

## Easy-Level Queries

![sql1](https://user-images.githubusercontent.com/97853367/156213439-f64b7373-e834-4f38-9bfb-2d0050db4639.jpg)

Task --> Query a count of the number of cities in CITY having a Population larger than 100,000.

**SELECT** COUNT(NAME) 
  **FROM** CITY 
  **WHERE** POPULATION >= 100000;

Task --> Query all columns for all American cities in the CITY table with populations larger than 100000. The CountryCode for America is USA.

**SELECT** *
    **FROM** CITY
    **WHERE** POPULATION >= 100000 AND COUNTRYCODE = 'USA'

## Medium-Level Queries

![sql2](https://user-images.githubusercontent.com/97853367/156215274-12f858df-ed1e-4751-b6c2-c164d198be23.png)
![sql3](https://user-images.githubusercontent.com/97853367/156215295-83470047-d511-44c6-bc02-b0dee6d32240.png)

Task --> Query an alphabetically ordered list of all names in OCCUPATIONS, immediately followed by the first letter of each profession as a parenthetical (i.e.: enclosed in parentheses). For example: AnActorName(A), ADoctorName(D), AProfessorName(P), and ASingerName(S).
Query the number of ocurrences of each occupation in OCCUPATIONS. Sort the occurrences in ascending order, and output them in the following format:

There are a total of [occupation_count] [occupation]s.

where [occupation_count] is the number of occurrences of an occupation in OCCUPATIONS and [occupation] is the lowercase occupation name. If more than one Occupation has the same [occupation_count], they should be ordered alphabetically.


SELECT (NAME || '(' || SUBSTR(OCCUPATION,1,1) || ')') FROM OCCUPATIONS ORDER BY NAME ASC;

**SELECT** ('There are a total of' || ' ' || COUNT(OCCUPATION) || ' ' || LOWER(OCCUPATION) || 's' || '.')
**FROM** OCCUPATIONS
**GROUP BY** OCCUPATION
**ORDER BY** COUNT(OCCUPATION), OCCUPATION ASC;

# HackerRank SQL 

Solving Code Challanges and Improving programming skills

## Code Challenge:The Pads
For this challenge, I wrote two SQL queries to generate required results.
![Screenshot 2024-06-10 at 9 48 10 PM](https://github.com/yonci09/HackerRank_SQL/assets/126642768/98c1dd8a-9401-4422-8044-e66faae723de)


## SQL QUERIES

As database, i used MySQL.

```bash
  SELECT CONCAT(NAME,'(',SUBSTR(OCCUPATION,1,1),')') AS N
FROM OCCUPATIONS
ORDER BY N;
SELECT CONCAT('There are a total of ',COUNT(OCCUPATION),' ',LOWER(OCCUPATION),'s.')
FROM OCCUPATIONS
GROUP BY OCCUPATION
ORDER BY COUNT(OCCUPATION), OCCUPATION;
```

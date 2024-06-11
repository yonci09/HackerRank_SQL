# HackerRank SQL 

Solving Code challenges and Improving programming skills

## Code Challenge: The Pads
I wrote two SQL queries for this challenge to generate the required results.

![Screenshot 2024-06-10 at 9 48 10 PM](https://github.com/yonci09/HackerRank_SQL/assets/126642768/98c1dd8a-9401-4422-8044-e66faae723de)


## SQL QUERIES

As a database, I chose to use MySQL.

```bash
  SELECT CONCAT(NAME,'(',SUBSTR(OCCUPATION,1,1),')') AS N
FROM OCCUPATIONS
ORDER BY N;
SELECT CONCAT('There are a total of ',COUNT(OCCUPATION),' ',LOWER(OCCUPATION),'s.')
FROM OCCUPATIONS
GROUP BY OCCUPATION
ORDER BY COUNT(OCCUPATION), OCCUPATION;
```

## Code Challenge: New Companies
I wrote a SQL query for this challenge to generate the required results.
![Screenshot 2024-06-10 at 9 58 42 PM](https://github.com/yonci09/HackerRank_SQL/assets/126642768/3133ba17-a7d9-425d-8bb8-500b2a063b6b)

## SQL QUERY
```bash
 select c.company_code, c.founder,
       count(distinct l.lead_manager_code),
       count(distinct s.senior_manager_code),
       count(distinct m.manager_code),
       count(distinct e.employee_code)
from Company as c 
join Lead_Manager as l 
on c.company_code = l.company_code
join Senior_Manager as s
on l.lead_manager_code = s.lead_manager_code
join Manager as m 
on m.senior_manager_code = s.senior_manager_code
join Employee as e
on e.manager_code = m.manager_code
group by c.company_code, c.founder
order by c.company_code;
```

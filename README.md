# HackerRank SQL 

Solving Code challenges and Improving programming skills
## Challenge: The Pads

![Occupation](https://github.com/yonci09/HackerRank_SQL/assets/126642768/647c33a3-7e92-4a56-8f54-1e7f55fa7bca)

## SQL Query

Working Platform: MySQL.

```bash
  SELECT CONCAT(NAME,'(',SUBSTR(OCCUPATION,1,1),')') AS N
FROM OCCUPATIONS
ORDER BY N;
SELECT CONCAT('There are a total of ',COUNT(OCCUPATION),' ',LOWER(OCCUPATION),'s.')
FROM OCCUPATIONS
GROUP BY OCCUPATION
ORDER BY COUNT(OCCUPATION), OCCUPATION;
```

## Challenge: New Companies

![NewCompanies](https://github.com/yonci09/HackerRank_SQL/assets/126642768/8bed336a-726d-4d6a-a231-cd33ac30b800)

## SQL Query
Working Platform: MySQL.

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

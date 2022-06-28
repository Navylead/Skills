# Skills
### About Me
I'm a junior QA trying to do my best in learning new skills)
### Skills
* **Testing theory**
* **Manual testing**
* **SQL(MySQL/Postgres):**
    * DML: select, where, order by, having, group by, join, except, insert into, update
    * DDL: create, alter, foreign key, primary key
* **JS basics**(functions, if, while, for)
* **GitHub**(repositories, branches)
* **Postman**(JS, auto tests API, collections, environments)
* **DevTools**(network, elements, console, sources, throttling, user agent)
* **Charles**(breakpoints, rewrites)
* **Android Studio**
### Code Examples:
```
select project, commits, contributors, regexp_replace(address,'[0-9]','!','g') address from repositories;
```
```
select case
when sum(number1)%2=0 then (select max(number1) from numbers)
else (select min(number1) from numbers)
end number1, case 
when sum(number2)%2=0 then (select max(number2) from numbers)
else (select min(number2) from numbers)
end number2 from numbers
```
```
select monthly_salary, role_name, employee_name from employee_salary es 
join salary s on s.id = es.salary_id 
join roles_employee re on re.employee_id = es.employee_id 
join roles r on r.id = re.role_id
join employees e on e.id = es.employee_id
where role_name like '%Junior%' and role_name like '%Python%';
```
### Education
* [Vadim Ksendzov](https://ksendzov.com/) course
  * Manual testing
* A. Rusov course
  * Manual testing
* Magnitogorsk State Technical University
  * Mining engineer
### Languages
* **Russian** - native
* **English** - A2-B1

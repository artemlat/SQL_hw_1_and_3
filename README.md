# SQL first and third homeworks  
*Here I learned to create tables in database and work with sql requests.*  
### Таблица employees

1) Создать таблицу employees
- id. serial,  primary key,
- employee_name. Varchar(50), not null
2) Наполнить таблицу employee 70 строками.

```
create table employees (
	id serial primary key,
	employee_name varchar(50) not null
);

insert into employees (employee_name)
values   
  ('Desirae Hayes'),
  ('Renee Walter'),
  ('Mallory Thornton'),
  ('Kato Carrillo'),
  ('Marcia Cleveland'),
  ('Salvador Kinney'),
  ('Kyra Rodgers'),
  ('Wylie Woods'),
  ('Hyatt Long'),
  ('Jescie Keith'),
  ('Bruno Sloan'),
  ('Lysandra Dotson'),
  ('Cally Mccoy'),
  ('Guy Stephenson'),
  ('Bert Hawkins'),
  ('Barrett Hendricks'),
  ('Harlan Rodriquez'),
  ('Mason Carey'),
  ('Glenna Acosta'),
  ('Victoria Bailey'),
  ('Amber Mcfadden'),
  ('Deborah West'),
  ('Lani Herrera'),
  ('Karyn Holt'),
  ('Cheryl Ewing'),
  ('Nomlanga Chen'),
  ('Burke Richardson'),
  ('Abdul Deleon'),
  ('Zeph Jennings'),
  ('Rajah Battle'),
  ('Lacey Tate'),
  ('Hammett Cortez'),
  ('Shelly Rivas'),
  ('Bert Schultz'),
  ('Kaseem Herrera'),
  ('Christian Tyson'),
  ('Aidan Petersen'),
  ('Kim Pena'),
  ('Hollee Christensen'),
  ('Lucas Nash'),
  ('Kenneth Albert'),
  ('Geoffrey Forbes'),
  ('Illana Nguyen'),
  ('Dylan Travis'),
  ('Zoe Palmer'),
  ('Clarke Daniel'),
  ('Allistair Henson'),
  ('Edan Kaufman'),
  ('Kyle Crosby'),
  ('Dean Bishop'),
  ('Yuli Mcguire'),
  ('Pamela Horn'),
  ('Richard Graham'),
  ('Carissa Leblanc'),
  ('Heather Durham'),
  ('Ferris Fowler'),
  ('Zoe Maxwell'),
  ('Bo Hudson'),
  ('Jesse Velasquez'),
  ('Joel James'),
  ('Jerome Mcconnell'),
  ('Craig Rowe'),
  ('Octavius Garrett'),
  ('Claudia Carlson'),
  ('Kalia Austin'),
  ('Ginger Conley'),
  ('Hashim Ayala'),
  ('Sybil Hamilton'),
  ('Ursa Bennett'),
  ('Reece Dunlap');
```

### Таблица salary

3) Создать таблицу salary
- id. Serial  primary key,
- monthly_salary. Int, not null
4) Наполнить таблицу salary 16 строками:
- 1000
- 1100
- 1200
- 1300
- 1400
- 1500
- 1600
- 1700
- 1800
- 1900
- 2000
- 2100
- 2200
- 2300
- 2400
- 2500

```
 create table salary (
 	id serial primary key,
 	monthly_salary int not null
);

insert into salary (monthly_salary)
values 
  (1000),
  (1100),
  (1200),
  (1300),
  (1400),
  (1500),
  (1600),
  (1700),
  (1800),
  (1900),
  (2000),
  (2100),
  (2200),
  (2300),
  (2400),
  (2500);
```
### Таблица employee_salary

5) Создать таблицу employee_salary
- id. Serial  primary key,
- employee_id. Int, not null, unique
- salary_id. Int, not null
6) Наполнить таблицу employee_salary 40 строками:
- в 10 строк из 40 вставить несуществующие employee_id
 
![employee_salary_table](https://github.com/artemlat/SQL_hw_1_and_3/blob/main/employee_salary_table.png)  

```
create table employee_salary (
	id serial primary key,
	employee_id int not null unique,
	salary_id int not null
);

insert into employee_salary (employee_id, salary_id)
values
  (3, 11),
  (1, 3),
  (5, 10),
  (40, 10),
  (23, 6),
  (11, 3),
  (52, 2),
  (15, 14),
  (26, 4),
  (16, 12),
  (33, 9),
  (85, 7), /*1*/
  (2, 1),
  (27, 9),
  (100, 4), /*2*/
  (8, 13),
  (41, 13),
  (69, 15),
  (71, 6), /*3*/
  (10, 14),
  (12, 15),
  (47, 5),
  (61, 12),
  (99, 4), /*4*/
  (17, 8),
  (34, 10),
  (44, 14),
  (75, 15), /*5*/
  (55, 16),
  (59, 8),
  (111, 2), /*6*/
  (67, 11),
  (18, 14),
  (77, 2), /*7*/
  (4, 3),
  (6, 7),
  (89, 11), /*8*/
  (90, 9), /*9*/
  (63, 12),
  (81, 14); /*10*/
```

### Таблица roles

7) Создать таблицу roles
- id. Serial  primary key,
- role_name. int, not null, unique
8) Поменять тип столба role_name с int на varchar(30)
9) Наполнить таблицу roles 20 строками:

![roles](https://github.com/artemlat/SQL_hw_1_and_3/blob/main/roles.png)
  
```
create table roles (
	id serial primary key,
	role_name int not null unique
);

alter table roles
alter column role_name type varchar (30);

insert into roles (role_name)
values
  ('Junior Python developer'),
  ('Middle Python developer'),
  ('Senior Python developer'),
  ('Junior Java developer'),
  ('Middle Java developer'),
  ('Senior Java developer'),
  ('Junior JavaScript developer'),
  ('Middle JavaScript developer'),
  ('Senior JavaScript developer'),
  ('Junior Manual QA engineer'),
  ('Middle Manual QA engineer'),
  ('Senior Manual QA engineer'),
  ('Project Manager'),
  ('Designer'),
  ('HR'),
  ('CEO'),
  ('Sales manager'),
  ('Junior Automation QA engineer'),
  ('Middle Automation QA engineer'),
  ('Senior Automation QA engineer');
```

### Таблица roles_employee

10) Создать таблицу roles_employee
- id. Serial  primary key,
- employee_id. Int, not null, unique (внешний ключ для таблицы employees, поле id)
- role_id. Int, not null (внешний ключ для таблицы roles, поле id)
11) Наполнить таблицу roles_employee 40 строками:

![roles_employee](https://github.com/artemlat/SQL_hw_1_and_3/blob/main/roles_employee.png)

```
create table roles_employee (
 	id serial primary key,
 	employee_id int not null unique,
 	role_id int not null,
 	foreign key(employee_id)
 		references employees(id),
 	foreign key(role_id)
 		references roles(id)
);

insert into roles_employee (employee_id, role_id)
values
  (3, 8),
  (1, 4),
  (5, 8),
  (40, 18),
  (9, 11),
  (38, 1),
  (52, 10),
  (15, 13),
  (26, 4),
  (16, 1),
  (33, 8),
  (6, 8), 
  (2, 8),
  (27, 5),
  (7, 4), 
  (8, 9),
  (41, 14),
  (69, 20),
  (32, 1), 
  (10, 14),
  (12, 3),
  (47, 11),
  (61, 12),
  (23, 4), 
  (17, 5),
  (34, 2),
  (44, 6),
  (11, 9), 
  (55, 13),
  (59, 11),
  (31, 2), 
  (67, 19),
  (18, 3),
  (56, 19), 
  (4, 1),
  (48, 2),
  (51, 11), 
  (49, 9), 
  (63, 3),
  (66, 14);
```

### Request training

1. Вывести всех работников чьи зарплаты есть в базе, вместе с зарплатами.

```
select employees.employee_name from employee_salary
join employees on employees.id  = employee_salary.employee_id;
```
![hw_3_1](https://github.com/artemlat/SQL_hw_1_and_3/blob/main/hw_3_1.png)

2. Вывести всех работников у которых ЗП меньше 2000.

```
select employees.employee_name, salary.monthly_salary from employee_salary
join employees on employees.id  = employee_salary.employee_id
join salary on salary.id = employee_salary.salary_id
where salary.monthly_salary < 2000;
```
![hw_3_2](https://github.com/artemlat/SQL_hw_1_and_3/blob/main/hw_3_2.png)

3. Вывести все зарплатные позиции, но работник по ним не назначен. 
(ЗП есть, но не понятно кто её получает.)

```
select salary.monthly_salary, employees.employee_name from employee_salary 
join salary on salary.id = employee_salary.salary_id
full join employees on employees.id = employee_salary.employee_id
where employees.employee_name is null;
```
![hw_3_3](https://github.com/artemlat/SQL_hw_1_and_3/blob/main/hw_3_3.png)

4. Вывести все зарплатные позиции  меньше 2000 но работник по ним не назначен. 
(ЗП есть, но не понятно кто её получает.)

```
select salary.monthly_salary, employees.employee_name from employee_salary
full join employees on employees.id = employee_salary.employee_id
join salary on salary.id = employee_salary.salary_id
where employees.employee_name is null
and 
salary.monthly_salary < 2000;
```
![hw_3_4](https://github.com/artemlat/SQL_hw_1_and_3/blob/main/hw_3_4.png)

5. Найти всех работников кому не начислена ЗП.

```
select employees.employee_name, salary.monthly_salary from employee_salary
full join employees on employees.id = employee_salary.employee_id
full join salary on salary.id = employee_salary.salary_id
where salary.monthly_salary is null;
```

![hw_3_5](https://github.com/artemlat/SQL_hw_1_and_3/blob/main/hw_3_5.png)  

6. Вывести всех работников с названиями их должности.

```
select employees.employee_name, roles.role_name from roles_employee
join employees on employees.id = roles_employee.employee_id
join roles on roles.id = roles_employee.role_id;
```

![hw_3_6](https://github.com/artemlat/SQL_hw_1_and_3/blob/main/hw_3_6.png)

7. Вывести имена и должность только Java разработчиков.

```
select employees.employee_name, roles.role_name from roles_employee
join employees on employees.id = roles_employee.employee_id
join roles on roles.id = roles_employee.role_id
where roles.role_name like '%Java developer%';
```
![hw_3_7](https://github.com/artemlat/SQL_hw_1_and_3/blob/main/hw_3_7.png)

8. Вывести имена и должность только Python разработчиков.

```
select employees.employee_name, roles.role_name from roles_employee
join employees on employees.id = roles_employee.employee_id 
join roles on roles.id = roles_employee.role_id 
where roles.role_name like '%Python developer%';
```
![hw_3_8](https://github.com/artemlat/SQL_hw_1_and_3/blob/main/hw_3_8.png)

9. Вывести имена и должность всех QA инженеров.

```
select employees.employee_name, roles.role_name from roles_employee
join employees on employees.id = roles_employee.employee_id
join roles on roles.id = roles_employee.role_id
where roles.role_name like '%QA engineer%';
```
![hw_3_9](https://github.com/artemlat/SQL_hw_1_and_3/blob/main/hw_3_9.png)

10. Вывести имена и должность ручных QA инженеров.

```
select employees.employee_name, roles.role_name from roles_employee
join employees on employees.id = roles_employee.employee_id 
join roles on roles.id = roles_employee.role_id 
where roles.role_name like '%Manual QA engineer%';
```
![hw_3_10](https://github.com/artemlat/SQL_hw_1_and_3/blob/main/hw_3_10.png)

11. Вывести имена и должность автоматизаторов QA

```
select employees.employee_name, roles.role_name from roles_employee
join employees on employees.id = roles_employee.employee_id 
join roles on roles.id = roles_employee.role_id 
where roles.role_name like '%Automation QA engineer%';
```
![hw_3_11](https://github.com/artemlat/SQL_hw_1_and_3/blob/main/hw_3_11.png)

12. Вывести имена и зарплаты Junior специалистов

```
select employees.employee_name, salary.monthly_salary, roles.role_name from employee_salary
join employees on employees.id = employee_salary.employee_id 
join salary on salary.id = employee_salary.salary_id 
join roles_employee on roles_employee.employee_id = employees.id 
join roles on roles.id = roles_employee.role_id 
where roles.role_name like '%Junior%';
```
![hw_3_12](https://github.com/artemlat/SQL_hw_1_and_3/blob/main/hw_3_12.png)

13. Вывести имена и зарплаты Middle специалистов

```
select employees.employee_name, salary.monthly_salary, roles.role_name from employee_salary 
join employees on employees.id = employee_salary.employee_id 
join salary on salary.id = employee_salary.salary_id 
join roles_employee on roles_employee.employee_id = employees.id 
join roles on roles.id = roles_employee.role_id
where roles.role_name like '%Middle%';
```
![hw_3_13](https://github.com/artemlat/SQL_hw_1_and_3/blob/main/hw_3_13.png)

14. Вывести имена и зарплаты Senior специалистов  

```
select employees.employee_name, salary.monthly_salary, roles.role_name from employee_salary
join employees on employees.id  = employee_salary.employee_id
join salary on salary.id = employee_salary.salary_id 
join roles_employee on roles_employee.employee_id = employees.id 
join roles on roles.id = roles_employee.role_id
where roles.role_name like '%Senior%';
```
![hw_3_14](https://github.com/artemlat/SQL_hw_1_and_3/blob/main/hw_3_14.png)

15. Вывести зарплаты Java разработчиков

```
select salary.monthly_salary, roles.role_name from employee_salary, salary, roles_employee, roles, employees
where salary.id = employee_salary.salary_id 
and employees.id = employee_salary.employee_id 
and roles_employee.employee_id = employees.id 
and roles.id = roles_employee.role_id
and roles.role_name like '%Java developer%';
```
![hw_3_15](https://github.com/artemlat/SQL_hw_1_and_3/blob/main/hw_3_15.png)

16. Вывести зарплаты Python разработчиков

```
select salary.monthly_salary, roles.role_name from employee_salary
join employees on employees.id = employee_salary.employee_id 
join salary on salary.id = employee_salary.salary_id 
join roles_employee on roles_employee.employee_id = employees.id 
join roles on roles.id = roles_employee.role_id
where roles.role_name like '%Python developer%';
```
![hw_3_16](https://github.com/artemlat/SQL_hw_1_and_3/blob/main/hw_3_16.png)

17. Вывести имена и зарплаты Junior Python разработчиков

```
select employees.employee_name, salary.monthly_salary, roles.role_name from employee_salary
join employees on employees.id = employee_salary.employee_id
join salary on salary.id = employee_salary.salary_id 
join roles_employee on roles_employee.employee_id = employees.id 
join roles on roles.id = roles_employee.role_id
where roles.role_name like '%Junior Python%';
```
![hw_3_17](https://github.com/artemlat/SQL_hw_1_and_3/blob/main/hw_3_17.png)

18. Вывести имена и зарплаты Middle JS разработчиков

```
select employees.employee_name, salary.monthly_salary, roles.role_name from employee_salary
join employees on employees.id = employee_salary.employee_id
join salary on salary.id = employee_salary.salary_id 
join roles_employee on roles_employee.employee_id = employees.id 
join roles on roles.id = roles_employee.role_id
where roles.role_name = 'Middle JavaScript developer';
```
![hw_3_18](https://github.com/artemlat/SQL_hw_1_and_3/blob/main/hw_3_18.png)

19. Вывести имена и зарплаты Senior Java разработчиков

```
select employees.employee_name, salary.monthly_salary, roles.role_name from employee_salary
join employees on employees.id = employee_salary.employee_id
join salary on salary.id = employee_salary.salary_id 
join roles_employee on roles_employee.employee_id = employees.id 
join roles on roles.id = roles_employee.role_id
where roles.role_name = 'Senior Java developer';
```
![hw_3_19](https://github.com/artemlat/SQL_hw_1_and_3/blob/main/hw_3_19.png)

20. Вывести зарплаты Junior QA инженеров  

```
select salary.monthly_salary, roles.role_name from employee_salary
join employees on employees.id = employee_salary.employee_id
join salary on salary.id = employee_salary.salary_id 
join roles_employee on roles_employee.employee_id = employees.id 
join roles on roles.id = roles_employee.role_id
where roles.role_name like '%Junior%QA engineer%';
```
![hw_3_20](https://github.com/artemlat/SQL_hw_1_and_3/blob/main/hw_3_20.png)

21. Вывести среднюю зарплату всех Junior специалистов

```
select round(avg(salary.monthly_salary), 2) as avg_Junior_salary from employee_salary
join employees on employees.id = employee_salary.employee_id
join salary on salary.id = employee_salary.salary_id 
join roles_employee on roles_employee.employee_id = employees.id 
join roles on roles.id = roles_employee.role_id
where roles.role_name like '%Junior%';
```
![hw_3_21](https://github.com/artemlat/SQL_hw_1_and_3/blob/main/hw_3_21.png)

22. Вывести сумму зарплат JS разработчиков

```
select sum(salary.monthly_salary) as sum_js_dev_salary  from employee_salary
join employees on employees.id = employee_salary.employee_id
join salary on salary.id = employee_salary.salary_id 
join roles_employee on roles_employee.employee_id = employees.id 
join roles on roles.id = roles_employee.role_id
where roles.role_name like '%JavaScript developer%';
```
![hw_3_22](https://github.com/artemlat/SQL_hw_1_and_3/blob/main/hw_3_22.png)

23. Вывести минимальную ЗП QA инженеров  

```
select min(salary.monthly_salary) as min_qa_salary  from employee_salary
join employees on employees.id = employee_salary.employee_id
join salary on salary.id = employee_salary.salary_id 
join roles_employee on roles_employee.employee_id = employees.id 
join roles on roles.id = roles_employee.role_id
where roles.role_name like '%QA engineer%';
```
![hw_3_23](https://github.com/artemlat/SQL_hw_1_and_3/blob/main/hw_3_23.png)

24. Вывести максимальную ЗП QA инженеров

```
select max(salary.monthly_salary) as min_qa_salary  from employee_salary
join employees on employees.id = employee_salary.employee_id
join salary on salary.id = employee_salary.salary_id 
join roles_employee on roles_employee.employee_id = employees.id 
join roles on roles.id = roles_employee.role_id
where roles.role_name like '%QA engineer%';
```
![hw_3_24](https://github.com/artemlat/SQL_hw_1_and_3/blob/main/hw_3_24.png)

25. Вывести количество QA инженеров

```
select count(roles.role_name) as qty_qa from roles_employee
join roles on roles.id = roles_employee.role_id
where roles.role_name like '%QA engineer%';
```
![hw_3_25](https://github.com/artemlat/SQL_hw_1_and_3/blob/main/hw_3_25.png)




















   






  



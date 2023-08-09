# #3. SQL first and third homeworks  
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




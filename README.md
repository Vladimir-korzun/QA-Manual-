# Решение заданий из тренажера [SQL Academy](https://sql-academy.org/ru)

1. Вывести имена всех людей, которые есть в базе данных
   авиакомпаний [(сайт)](https://sql-academy.org/ru/trainer/tasks/1)

<details>
  <summary>Решение</summary>

```mysql
SELECT name
FROM passenger;
```

</details>

2. Вывести названия всеx авиакомпаний [(сайт)](https://sql-academy.org/ru/trainer/tasks/2)


<details>
  <summary>Решение</summary>

```mysql
SELECT name
FROM company;
```

</details>

3. Вывести все рейсы, совершенные из Москвы [(сайт)](https://sql-academy.org/ru/trainer/tasks/3)

<details>
   <summary>Решение</summary>

```mysql
SELECT *
from trip
WHERE town_from = 'moscow'
```
   
</details>

4. Вывести имена людей, которые заканчиваются на "man" [(сайт)](https://sql-academy.org/ru/trainer/tasks/4)

<details>
   <summary>Решение</summary>

```mysql
SELECT name
from passenger
WHERE name LIKE '%man'
```
   
</details>

5. Вывести количество рейсов, совершенных на TU-134 [(сайт)](https://sql-academy.org/ru/trainer/tasks/5)

<details>
   <summary>Решение</summary>

```mysql
SELECT count(*) as COUNT
from trip
WHERE plane = 'TU-134'
```
   
</details>

6. Какие компании совершали перелеты на Boeing [(сайт)](https://sql-academy.org/ru/trainer/tasks/6)

<details>
   <summary>Решение</summary>

```mysql
SELECT DISTINCT name
FROM company
	join trip on company.id = trip.company
where plane = "Boeing";
```
   
</details>

7. Вывести все названия самолётов, на которых можно улететь в Москву (Moscow) [(сайт)](https://sql-academy.org/ru/trainer/tasks/7)

<details>
   <summary>Решение</summary>

```mysql
select DISTINCT plane
from trip
WHERE town_to = 'Moscow'
```
   
</details>

8. В какие города можно улететь из Парижа (Paris) и сколько времени это займёт? [(сайт)](https://sql-academy.org/ru/trainer/tasks/8)

<details>
   <summary>Решение</summary>

```mysql
SELECT town_to,
	TIMEDIFF(time_in, time_out) as flight_time
from trip
where town_from = 'paris';
```
   
</details>

9. Какие компании организуют перелеты из Владивостока (Vladivostok)? [(сайт)](https://sql-academy.org/ru/trainer/tasks/9)

<details>
   <summary>Решение</summary>

```mysql
SELECT DISTINCT name
from company
	join trip on company.id = trip.company
WHERE town_from = 'Vladivostok'
```
   
</details>

10. Вывести вылеты, совершенные с 10 ч. по 14 ч. 1 января 1900 г. [(сайт)](https://sql-academy.org/ru/trainer/tasks/10)

<details>
   <summary>Решение_1</summary>

```mysql
SELECT *
from trip
where time_out BETWEEN '1900.01.01 10.00.00' AND '1900.01.01 14.00.00'
```
   
</details>

<details>
  <summary>Решение_2</summary>

```mysql
SELECT *
FROM trip
WHERE DATE(time_out) = '1900-01-01'
  AND TIME_FORMAT(time_out, '%H:%i') >= '10:00'
  AND TIME_FORMAT(time_out, '%H:%i') <= '14:00';
```

</details>

11. Выведите пассажиров с самым длинным ФИО. Пробелы, дефисы и точки считаются частью имени. [(сайт)](https://sql-academy.org/ru/trainer/tasks/11)

<details>
   <summary>Решение</summary>

```mysql

```
   
</details>

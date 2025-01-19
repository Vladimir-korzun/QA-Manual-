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

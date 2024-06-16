# Домашнее задание к занятию "`Название занятия`" - `Фамилия и имя студента`
---
Задание можно выполнить как в любом IDE, так и в командной строке.

### Задание 1
Получите уникальные названия районов из таблицы с адресами, которые начинаются на “K” и заканчиваются на “a” и не содержат пробелов.

### Решение 1

SELECT DISTINCT district
FROM address
WHERE district  LIKE 'k%a' and district not LIKE  '% %';

![Название скриншота 1](ссылка на скриншот 1)`

### Задание 2
Получите из таблицы платежей за прокат фильмов информацию по платежам, которые выполнялись в промежуток с 15 июня 2005 года по 18 июня 2005 года включительно и стоимость которых превышает 10.00.

### Решение 2

SELECT *
FROM payment
WHERE payment_date  BETWEEN '2005-06-15' and '2005-06-19'
AND amount > 10;

![Название скриншота 1](ссылка на скриншот 1)`

### Задание 3
Получите последние пять аренд фильмов.

### Решение 3

SELECT *  
FROM rental   
ORDER by rental_date DESC 
LIMIT 5;

![Название скриншота 1](ссылка на скриншот 1)`

### Задание 4
Одним запросом получите активных покупателей, имена которых Kelly или Willie.

Сформируйте вывод в результат таким образом:

все буквы в фамилии и имени из верхнего регистра переведите в нижний регистр,
замените буквы 'll' в именах на 'pp'.

### Решение 4

SELECT LOWER(REPLACE(first_name, 'LL', 'pp')) 
FROM customer
WHERE first_name LIKE 'Willie' OR first_name  LIKE 'Kelly';

![Название скриншота 1](ссылка на скриншот 1)`


....
....
```

`При необходимости прикрепитe сюда скриншоты
![Название скриншота](ссылка на скриншот)`

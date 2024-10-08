#### Домашнее задание к занятию «SQL. Часть 1» -"Хасаншин Марат"

#### Задание 1
Получите уникальные названия районов из таблицы с адресами, которые начинаются на “K” и заканчиваются на “a” и не содержат пробелов.

```
SELECT DISTINCT district 
FROM address 
WHERE district  LIKE 'k%a' and district not LIKE  '% %';

```
![alt text](21.png)

#### Задание 2
Получите из таблицы платежей за прокат фильмов информацию по платежам, которые выполнялись в промежуток с 15 июня 2005 года по 18 июня 2005 года включительно и стоимость которых превышает 10.00.

```
SELECT *
FROM payment
WHERE payment_date  BETWEEN '2005-06-15' and '2005-06-19' and amount > 10
ORDER BY payment_date;
```
![alt text](22.png)

#### Задание 3
Получите последние пять аренд фильмов.

```
SELECT *  
FROM rental   
ORDER by rental_date DESC 
LIMIT 5;
```
![alt text](23.png)
#### Задание 4
Одним запросом получите активных покупателей, имена которых Kelly или Willie.

Сформируйте вывод в результат таким образом:

все буквы в фамилии и имени из верхнего регистра переведите в нижний регистр,
замените буквы 'll' в именах на 'pp'.
```
SELECT LOWER(REPLACE(first_name, 'L', 'p')), LOWER(last_name) 
FROM customer
WHERE first_name LIKE 'Willie' OR first_name  LIKE 'Kelly';
```
![alt text](24.png)

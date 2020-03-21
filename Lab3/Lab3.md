Lab: SQL injection UNION attack, determining the number of columns returned by the query

Здесь нам надо выяснить сколо таблиц в запросе.

1) Выбираем любую категорию

![](0.jpg)
![](1.jpg)

2) Предположим, что в запросе 2 столбца, тогда мы вводим 'UNION SELECT NULL, NULL --

![](2.jpg)
![](3.jpg)

3) Видим ошибку и предполагаем, что в запросе 3 столбца, вводим ' UNION SELECT NULL, NULL, NULL --

![](4.jpg)

5) И у нас выводятся наши колонки, значит, в запросе 3 столбца

![](5.jpg)

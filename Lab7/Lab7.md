 Lab: Exploiting XXE using external entities to retrieve files
 
 1) Переходим на сайт и выбираем товар
 
 ![](0000.jpg)
 
 2) Включаем Burp, кликаем на кнопку "Check stock" и перехватываем запрос берпом во вкладке Proxy -> HTTP history, отправляем его в Repeater
 
 ![](0001.png)
 
 3) Изменяем запрос, вставляем обращение к сущности - файлу, который нам нужно вытащить :
'<!DOCTYPE foo [ <!ENTITY xxe SYSTEM "file:///etc/passwd"> ]>'
<stockCheck><productId>&xxe;</productId
 
 ![](0002.png)
 
 4) Получаем ответ:
 
 ![](0003.png)
 
 5) Видим, что лаба выполнена успешно
 
 ![](0004.png)

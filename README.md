#Postman

![alt text](https://github.com/HelHitch/main_portfolio_prj/blob/content/Postman_(software).png)

На данной ветке собраны колекции API запросов. В каждой коллекци есть тесты для проверки body и headers.

<h1> SWAGGER </h1>

![alt text](https://github.com/HelHitch/main_portfolio_prj/blob/content/7658037.png)


Конечно, куда без знаменитого SWAGGER petstore? 
В данной колекции, я создала юзера, изменила его данные. После этого, создала питомца. Обновила данные питомца. С помощью запроса GET убедилась, что данные изменились на те, что я задала. После, удалила питомца через DELETE и убедилась, опять же через GET, что данного питомца в системе нет.

![alt text](https://github.com/HelHitch/main_portfolio_prj/blob/content/Скриншот%2009-06-2022%20180048.jpg)

К каждому запросу я прописала тесты, которые посчитала нужными: 

![alt text](https://github.com/HelHitch/main_portfolio_prj/blob/content/test_result.jpg)

Но, что самое важное - прописать запрос на ответ от сервера со статус-кодом 200. Почему я считаю, что это важно?
Практикуясь и тестируя разные API серверы, я наткнулась на такую частую ошибку, как возвращение статус кода 200, на попытку зарегестрироваться
существующим пользователем. Так как мы получили ошибку, о том, что регистрация не удалась, то и статус код должен быть соответсвующий (например, 400) .
Но иногда разработчики либо не так выставляют статус-коды, либо забывают их изменить. 
Проверять корректность ответов очень важно, так как может получиться так, что человек ввел неккоректные данные, а ему присылается статус-код 500. Потому что кто-то из разработчиков что-то напутал. И человек просто думает, что наш сайт не доступен и не сможет воспользоваться им для удовлетворения тех целей, за которым он пришел на сайт. Клиент потерян.

Также, в тестах прописала проверку наличия определенных данных в JSON, потому что не мала вероятность того, что после PUT, обновления не произойдет и у человека не обновится информация, над которой он так старался. Согласитесь, будет очень обидно, если человек изменял много параметров на сайте, нажал сохранить и после перезагрузки страницы обнаружил, что ничего из того, на что он потратил пол часа, не сохранилось. Клиент потерян х2.

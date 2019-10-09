**Запуск контейнеров**

`docker-compose up`

Через env можно передать желаемый порт, по умолчанию 80

Пример запуска на порту 8080

`PORT=8080 docker-compose up`

Так же можно передать USERS_CONTAINER_NAME и SITE_CONTAINER_NAME
 
Это имена контейнеров и они доступны из php в массиве $_ENV


Другие доступные переменные можно посмотерть в .env


**Тесты**

`composer install -d ./site && ./site/vendor/bin/phpunit  --configuration=./site/phpunit.xml`

`composer install -d ./users && ./users/vendor/bin/phpunit --configuration=./users/phpunit.xml`


**Покрытие**

`php coverage-checker.php ./site/build/logs/clover.xml 100`

`php coverage-checker.php ./users/build/logs/clover.xml 100`
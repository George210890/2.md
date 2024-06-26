# Домашнее задание к занятию 2 «Кластеризация и балансировка нагрузки»


### Задание 1
- Запустите два simple python сервера на своей виртуальной машине на разных портах
- Установите и настройте HAProxy, воспользуйтесь материалами к лекции по [ссылке](2/)
- Настройте балансировку Round-robin на 4 уровне.
- На проверку направьте конфигурационный файл haproxy, скриншоты, где видно перенаправление запросов на разные серверы при обращении к HAProxy.

### Решение 1


[Конфигурационный файл haproxy для задания №1](https://github.com/George210890/2.md/blob/main/haproxy1%20(1).cfg)

Скриншоты работы haproxy и страница статистики

![1-1](https://github.com/George210890/2.md/blob/main/1-1.PNG)
![1-2](https://github.com/George210890/2.md/blob/main/1-2.PNG)

------

### Задание 2
- Запустите три simple python сервера на своей виртуальной машине на разных портах
- Настройте балансировку Weighted Round Robin на 7 уровне, чтобы первый сервер имел вес 2, второй - 3, а третий - 4
- HAproxy должен балансировать только тот http-трафик, который адресован домену example.local
- На проверку направьте конфигурационный файл haproxy, скриншоты, где видно перенаправление запросов на разные серверы при обращении к HAProxy c использованием домена example.local и без него.

### Решение 2

В конфигурационном файле haproxy для второго задания переделал секцию backend web_servers
[Конфигурационный файл haproxy для задания №2](https://github.com/George210890/2.md/blob/main/haproxy2%20(1).cfg)

Скриншоты работы haproxy второго задания и страница статистики

![2-1](https://github.com/George210890/2.md/blob/main/2-1.PNG)
![2-2](https://github.com/George210890/2.md/blob/main/2-2.PNG)

Задание: модуль HTTPReqRes
=============================
База данных: Yandex Clickhouse


Атрибуты
--------

1. Path [String] - путь запроса
2. Params [String] -параметры запроса
3. Req_data [String] -вложенные json
4. Created_date [Date] -дата создания
4. Created_time [Time] -время создания
5. Res_data [String] -ответ
6. Status [String] - код состояния http
7. Method [String] - тип запроса

Методы
------

 1. Add (HTTPReqRes, *bool) - Добавление новой записи в таблице HTTPReqRes.


Требования
----------

 1. Все методы работающие с БД должны быть написаны в файле clickhouse.go
 2. Все методы кроме описанных в пункте Методы, должны быть приватными
 3. Каждый метод из пункта Методы, должен быть написан по требованиям пакета RPC (https://golang.org/pkg/net/rpc)
 4. SQL скрипт создания таблицы должен лежать в файле HTTPReqRes.sql
 5. Таблица должна быть создана с движком Merge tree, индекс:Path + Created_date
 6. Код должен быть задокументирован
 7. ORM не используется
 8. Должна быть валидация переданных параметров перед каждым запросом (см. модель User)
 9. Типы сделать через указатели (см. модель User)


Используемые пакеты
-------------------

 1. net/rpc (https://golang.org/pkg/net/rpc)
 2. https://github.com/roistat/go-clickhouse
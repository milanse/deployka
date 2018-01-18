# Vanessa Deployment Engine

Развертывание конфигураций 1С на целевой базе 1С.

## Возможные команды

* help      - Вывод справки по параметрам
* loadcfg   - Загрузка/обновление конфигурации
* loadrepo  - Обновить из хранилища подключенную базу
* session   - Управление сеансами информационной базы
* dbupdate  - Обновление конфигурации базы данных
* run       - Управление запуском в режиме предприятия

Для подсказки по конкретной команде наберите help <команда>

## session - Управление сеансами информационной базы

### Параметры:
* <Действие> - lock|unlock|kill
* -ras - Сетевой адрес RAS, по умолчанию localhost:1545
* -rac - Команда запуска RAC, по умолчанию находим в каталоге установки 1с
* -db - Имя информационной базы
* -db-user - Пользователь информационной базы
* -db-pwd - Пароль пользователя информационной базы
* -cluster-admin - Администратор кластера
* -cluster-pwd - Пароль администратора кластера
* -v8version - Маска версии платформы 1С
* -lockmessage - Сообщение блокировки
* -lockuccode - Ключ разрешения запуска
* -lockstart - Время старта блокировки пользователей, время указываем как '2040-12-31T23:59:59'
* -lockstartat - Время старта блокировки через n сек


## loadcfg - Загрузка/обновление конфигурации

### Параметры:

* <СтрокаПодключения> - Строка подключения к рабочему контуру
* <ПутьДистрибутива> - Путь к дистрибутиву в виде каталога версии
* /mode - Режим обновления:
 *	-auto - Сначала искать CFU, потом CF
 *	-cf   - Использовать только CF
 *	-cfu  - Использовать только CFU
 *	-load - Полная загрузка конфигурации
 *	-skip - Не выполнять обновление
* -db-user - Пользователь информационной базы
* -db-pwd - Пароль пользователя информационной базы
* -v8version - Маска версии платформы 1С

## loadrepo - Обновить из хранилища подключенную базу

### Параметры:

* <СтрокаПодключения> - Строка подключения к рабочему контуру
* <АдресХранилища> - Путь или сетевой адрес хранилища 1С
* -db-user - Пользователь информационной базы
* -db-pwd - Пароль пользователя информационной базы
* -storage-user - Пользователь хранилища конфигурации
* -storage-pwd - Пароль пользователя хранилища конфигурации
* -storage-ver - Версия (номер) закладки в хранилище - необязательно
* -v8version - Маска версии платформы 1С
* -uccode - Ключ разрешения запуска


## dbupdate - Обновление конфигурации базы данных

### Параметры:

* <СтрокаПодключения> - Строка подключения к рабочему контуру
* -db-user - Пользователь информационной базы
* -db-pwd - Пароль пользователя информационной базы
* -v8version - Маска версии платформы 1С
* -uccode - Ключ разрешения запуска
* -allow-warnings - Маска версии платформы 1С
* -allow-dynamic - Разрешить обновлять динамически

## run - Управление запуском в режиме предприятия

### Параметры:
 
* <СтрокаПодключения> - Строка подключения к рабочему контуру
* -db-user - Пользователь информационной базы
* -db-pwd - Пароль пользователя информационной базы
* -v8version - Маска версии платформы 1С
* -uccode - Ключ разрешения запуска
* -command - Строка передаваемя в ПараметрыЗапуска, /C''
* -execute - Путь обработки для запуска



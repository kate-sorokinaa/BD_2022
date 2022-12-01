# Описание сущностей
(имя поля, тип, ограничения, связь с другими сущностями)
## Картина (User Painting)
|имя поля | тип | ограничения | описание |
|:---:|:---:|:---:|:---:|
| painting_id | pk | auto increment; not null; unique | первичный ключ |
| title | VARCHAR(100) | not null | название картины |
| painter_id |  |  | художник |
| year | int| not null | год |
| cost | float | not null | стоимость |
| owner_id |  |  | владелец картины |
| style_id |  |  | стиль картины |
| material_id |  |  | использованные материалы |
## Владелец (Owner)
|имя поля | тип | ограничения | описание |
|:---:|:---:|:---:|:---:|
| owner_id | pk | auto increment; not null; unique | первичный ключ |
| name | VARCHAR(50) | not null | имя владельца |
| email | VARCHAR(50) | not null | почта владельца |
## Художник (Painter)
|имя поля | тип | ограничения | описание |
|:---:|:---:|:---:|:---:|
| painter_id | pk | auto increment; not null; unique | первичный ключ |
| name | VARCHAR(100) | not null | имя художника |
| era | VARCHAR(100) | not null | эпоха |
| country | VARCHAR(50) | not null | страна |
## Материал (Material)
|имя поля | тип | ограничения | описание |
|:---:|:---:|:---:|:---:|
| material_id | pk | auto increment; not null; unique | первичный ключ |
| material | VARCHAR(50) | not null | использованный материал |
## Стиль (Style)
|имя поля | тип | ограничения | описание |
|:---:|:---:|:---:|:---:|
| style_id | pk | auto increment; not null; unique | первичный ключ |
| style | VARCHAR(50) | not null | стиль |
## Сотрудник (Employee)
|имя поля | тип | ограничения | описание |
|:---:|:---:|:---:|:---:|
| employee_id | pk | auto increment; not null; unique | первичный ключ |
| full_name | VARCHAR(100) | not null | ФИО сотрудника|
| age | int | not null | возраст |
| phone_number | int | not null | номер телефона |
| position_id | int | not null | внешний ключ на должность |
## Покупатель (Customer)
|имя поля | тип | ограничения | описание |
|:---:|:---:|:---:|:---:|
| customer_id | pk | auto increment; not null; unique | первичный ключ |
| name | VARCHAR(100) | not null | имя покупателя |
| balance | double | not null | баланс |
## Должность сотрудника (Position)
|имя поля | тип | ограничения | описание |
|:---:|:---:|:---:|:---:|
| position_id | pk | auto increment; not null; unique | первичный ключ |
| name_of_position | VARCHAR(100) | not null | название должности |
| salary | int | not null | з/п |
| employment | VARCHAR(30) | not null | занятость |
## Покупка (Purchase)
|имя поля | тип | ограничения | описание |
|:---:|:---:|:---:|:---:|
| purchase_id | pk | auto increment; not null; unique | первичный ключ |
| customer_id | int | auto increment; not null; unique | внешний ключ на клиента |
| employee_id | int | auto increment; not null; unique | внешний ключ на сотрудника |
| date | datetime | not null | дата покупки |
| status_id | int | not null | статус заказа |
## Статус (Status)
|имя поля | тип | ограничения | описание |
|:---:|:---:|:---:|:---:|
| status_id | pk | auto increment; not null; unique | первичный ключ |
| status | VARCHAR(30) | not null | статус заказа |

# Сущности и их представление в базе данных

## User (Пользователь)
| Название поля | Тип | Ограничение | Описание |
|---------------|-----|-------------|----------|
|Id|PK|auto increment; not null; unique|Первичный ключ|
|Name|VARCHAR[30]| not null|Имя пользователя|
|Nickname|VARCHAR[20]|not null| Ник пользователя в клиенте|
|Email|VARCHAR[20]|not null| Почта пользователя|
|Password|VARCHAR[50]|not null|Пароль|

## Game (игра)
| Название поля | Тип | Ограничение | Описание |
|---------------|-----|-------------|----------|
|Id|PK|auto increment; not null; unique|Первичный ключ|
|Name|VARCHAR[20]| not null|Название игры|
|Description|TEXT| not null|Описание игры|
|Price|FLOAT| not null|Цена игры|
|ReleaseDate|DATE|not null|Дата выхода игры|

## Wallet (кошелек)
| Название поля | Тип | Ограничение | Описание |
|---------------|-----|-------------|----------|
|Id|PK|auto increment; not null; unique|Первичный ключ|
|UserId|FK|not null|Внешний ключ пользователя|
|Ballance|FLOAT|not null| Балланс кошелька|

## Cart (корзина)
| Название поля | Тип | Ограничение | Описание |
|---------------|-----|-------------|----------|
|Id|PK|auto increment; not null; unique|Первичный ключ|
|WalletId|FK|not null| Внешний ключ на кошелек|

## PaymentHistory ( История транзакций)
| Название поля | Тип | Ограничение | Описание |
|---------------|-----|-------------|----------|
|Id|PK|auto increment; not null; unique|Первичный ключ|
|WalletId|FK|not null| Внешний ключ на кошелек|
|Time|DATETIME|not null|Дата и время транзакции|

## Workbench (Мастерская для сотрудников)
| Название поля | Тип | Ограничение | Описание |
|---------------|-----|-------------|----------|
|Id|PK|auto increment; not null; unique|Первичный ключ|
|UserId|FK|not null|Внешний ключ пользователя|
|StartDate|DATE|not null|Дата начала проекта|
|ProjectName|VARCHAR[50]|not null|Название Проекта|

## GameFeedBack(Отзывы и оценки игр)
| Название поля | Тип | Ограничение | Описание |
|---------------|-----|-------------|----------|
|Id|PK|auto increment; not null; unique|Первичный ключ|
|SenderId|FK|not null|Внешний ключ отправителя|
|GameId|PK|not null|Внешний ключ игры|
|Score|TINYINT UNSIGNED|not null;<=100| оценка игры|
|Comment|TEXT||Отзыв об игре|

## Discussion(Обсуждения на произвольные темы)
| Название поля | Тип | Ограничение | Описание |
|---------------|-----|-------------|----------|
|Id|PK|auto increment; not null; unique|Первичный ключ|
|OwenerId|FK|not null|Внешний ключ создателя обсуждения|
|Theme|VARCHAR[50]|not null|Тема обсуждения|


# Вспомогательные 


## GameLibrary(Библиотека игр)
| Название поля | Тип | Ограничение | Описание |
|---------------|-----|-------------|----------|
|Id|PK|auto increment; not null; unique|Первичный ключ|
|GameId|PK|not null|Внешний ключ игры|
|UserId|FK|not null|Внешний ключ пользователя|
|State|VARCHAR(10)|not null|Состояние игры|

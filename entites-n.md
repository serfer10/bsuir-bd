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
|UserId|FK|not null|Внешний ключ индентификатора пользователя|
|Ballance|FLOAT|not null| Балланс кошелька|

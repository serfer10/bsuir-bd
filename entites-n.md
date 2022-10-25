# Сущности и их представление в базе данных

## User (Пользователь)
| Название поля | Тип | Ограничение | Описание |
|---------------|-----|-------------|----------|
|Id|PK|auto increment; not null; unique|Первичный ключ|
|Name|VARCHAR[30]| not null|Имя пользователя|
|Nickname|VARCHAR[20]|not null| ник пользователя в клиенте|
|Email|VARCHAR[20]|not null| почта пользователя|
|Password|VARCHAR[50]|not null|пароль|

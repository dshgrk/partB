# Система управління салоном краси

Цей проєкт є системою управління салоном краси для адміністраторів, яка допомагає організувати та керувати записами, клієнтами та майстрами краси в салоні, розраховувати їхню заробітню плату.

## Ключові можливості

1. **Клієнт**
   - Додавання нових клієнтів до системи та видалення старих.
   - Перегля інформації про клієнтів.

2. **Процедури**
   - Перегляд списку доступних процедур в салоні та інформації про них.

3. **Майстер**
   - Перегляд інформації про майстрів салону.
   - Розрахунок заробітної плати для майстра. Фіксована ставка для кожного дорівнює 10000 грн/місяць + бонуси (10% від кожної процедури, яку зробить майстер).

4. **Запис**
   - Записати клієнта на процедуру або видалити запис.

## Компоненти

- **Booking**: Представляє запис клієнта, включаючи деталі, такі як призначений майстер, назва процедури та її дата і час.

- **Client**: Представляє клієнта в системі салону краси. Включає ім'я, вік і список записів на процедури.

- **BeautySpecialist**: Представляє майстра краси в салоні. Включає ім'я, вік, зарплату, спеціалізацію та список призначених йому процедур.

- **Procedure**: Представляє процедуру, яку пропонує салон. Включає інформацію, таку як назва, ціна, тривалість та майстер, який призначений виконати процедуру.

- **ProcedureTypes**: Перелічення, яке визначає різні типи процедур краси, які пропонує салон.

## Відношення між класами

1. Композиція між класом `Сlient` та класом `Booking`.
2. Двостороння асоціація між `Booking` та `BeautySpecialist`.
3. Одностороння асоціація між `Booking` та `Procedure`.
4. Двостороння агрегація між `BeautySpecialist` та `Procedure`.
5. Залежність перелічення `ProcedureTypes` від `Procedure`.
6. Класи `Client` та `BeautySpecialist` реалізують інтерфейс `IPerson`.
7. Класи `Procedure` та `Booking` реалізують інтерфейс `IPrint`.

![image](https://github.com/dshgrk/Project_partA_-_program/assets/149286064/62f759c7-3cb3-47ac-9985-5ea4e37f2c71)


### Задание 1. - Создание базы данных c 3 таблицами в mySqlWorkbench

Научиться пользоваться инстументом визуальной работы с БД - mySQLWorkbench  
Учебное видео [Создание базы данных MySQL Workbench](https://www.youtube.com/watch?v=ChLjnsKLoZE)  

1. Найдите в строке поиска `mySQLWorkbench` и запустите программу  
2. Добавьте новую модель `File \ New Model` и переименуйте ее с `myDB` на `ProductDB-K231B`
3. Добавьте новую диаграмму через `Add diagram`
4. Добавьте новую таблицу (нажав на иконку с изображением таблицы)
```
Название:
user
Поля (Columns):
id INT PK NN AI
name VARCHAR(45)
surname VARCHAR(45)
```
5. Добавьте еще одну таблицу (2-ю)
```
Название:
product
Поля (Columns):
id INT PK NN AI
name VARCHAR(45)
description LONGTEXT
```
6. Добавьте еще одну таблицу (3-ю)
```
Название:
orders
Поля (Columns):
id INT PK NN AI
user_id INT NN
product_id INT NN
sum FLOAT
```
Сохраните модель `File \ Save model` как `K231b`
<hr>

### Задание 2. - Связь между таблицами

Последняя таблица - таблица связи между двумя другими таблицами,   
поэтому для нее надо добавить внешние ключи (вкладка `Foreign keys`)
```
Foreign keys
user_key (Ref.table user) user_id CASCADE, CASCADE
product_key (Ref.table product) product_id CASCADE, CASCADE
```
<hr>

### Задание 3. - Экспорт скрипта на создание и Создание БД

1. Выполните для загруженной модели `File \ Export \ Forward Engeneer SQL CREATE Script`  
(указав название скрипта `K231b`, два раза нажмите `Next` и один раз `Finish`, если ругается на права - скопируйте через буфер обмена и создайте файл через Блокнот)  
2. Запустите сервер СУБД `mySQL` через программу `XAMPP Control Panel` (найдите в строке поиска) - нажмите кнопку Start, чтобы надпись mySQL загорелась зеленым
3. Закройте `mySQLWorkbench` и запустите программу заново
4. Нажмите `mySQL Connection` кнопку (+) для создания нового соединения
(назовите его `K231b-connection` и нажмите `OK`)
5. Нажмите на получившееся соединение (откроется окно с молниями)
6. Откройте скрипт на создание базы данных (БД) через меню `File \ Open script`
7. Удалите `VISIBLE` для последней таблицы (- может мешать при выполнении скрипта) и
   запустите загруженный скрипт на выполнение нажатием молнии
8. Если ошибок не случилось - поздаравляю, Вы создали БД из трех таблиц - откройте вкладку `Schemas` (в левой панели) и, вызвав правой клавишей мыши контекстное меню, обновите схему данных, выбрав пункт `Refresh All`
<hr>

### Задание 4. - Вставка данных

1. Откройте вкладку для записи запроса `File \ New Query Tab` и вставьте 3 записи языком запросов SQL в таблицу `user`
```
INSERT INTO .. (.., ..) VALUES ('Иван', 'Сидоров');
INSERT INTO .. (.., ..) VALUES ('Агафья', 'Петрова');
INSERT INTO .. (.., ..) VALUES ('Афанасий', 'Самоваров');

вместо многоточия (..) добавьте название таблицы и названия списка полей
```
2. В схеме данных (слева) найдите таблицу `user` и нажмите кнопку просмотра данных таблицы - иконка таблицы, рядом с названием
3. Убедитесь в том что SQL-запрос на просмотр данных выглядит как
```
SELECT * FROM user;
```
4. Откройте вкладку для записи запроса `File \ New Query Tab` и, самостоятельно, вставьте 3 записи языком запросов SQL в таблицу `product`
```
В поле 'name' укажите 'Пицца Маргарита', а в поле 'description' - 'Пицца «Маргарита» — это традиционная итальянская пицца. Ее основные ингредиенты это спелые томаты, сыр моцарелла и листья базилика — сочетание этих простых ингридиентов придает пицце ее неповторимый вкус'

('Пицца Гавайская',
'Гавайская пицца (также ананасовая пицца) — пицца, приготовляемая с использованием белого соуса, сыра, ананасов, курицы и морепродуктов');

('Пицца 4 сыра',
'В состав пиццы «4 сыра» входят сыры: моцарелла, пармезан, горгонзолла (с голубой плесенью) и эмменталь (сладковатый сыр с пряным привкусом)');
```

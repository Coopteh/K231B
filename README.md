### Задание 1. - Расчет суммы

1. видео-урок [Расчет суммы в Excel](https://www.youtube.com/watch?v=_fcL5qXamyc)
2. Откройте Excel и создайте новую книгу  
4. Добавьте в столбцы 4-й строки (начиная с ячейки E4) названия `Товар`, `Ед.изм`, `Кол-во`, `Цена`, `Сумма` - сделайте фон желтый.  
5. Выше добавьте заголовок `План закупок`  
6. Ниже названий, в столбцы 5-й строки (начиная с ячейки E5) добавьте строку `Клей Момент`, `шт`, `19`, `30.1`
   Добавьте еще строки
   ```
   Пена монтажная, шт, 43, 120
   Мешки д/мусора, уп, 10, 70
   Герметик, шт, 18, 105
   Саморезы, уп, 20, 40
   ```
8. Выделить 1 столбец, сделать голубой фон
9. Сделать обрамление таблицы, строк, столбцов в рамку
10. Сделайте форматирование столбцов `Цена` и `Сумма` с двумя десятичными знаками после запятой (от 5 до 10 строки включительно)
11. В первой ячейке столбца `Сумма` запишите вычисление суммы `=G5*H5` (как колва* цену)
12. Сделайте методом перетягивания вычисление сумм в остальных ячейках столбца
13. В 5 строке столбца задайте в ячейке (`I10`) итоговую сумму формулой `=СУММ(I5:I9)`
<h2>

### Задание 2. - Проценты
1. Видео к заданию [Как посчитать проценты в excel](https://www.youtube.com/watch?v=KyPJ9CJDBLY)
2. Добавьте справа еще два столбца `Скидка,%`, `Сумма со скидкой`
3. Отформатируйте ячейки столбца `Скидка,%` как `Процентный` без десятичных знаков
4. Вставьте проценты: 5, 2, 10, 7, 5
5. В первой ячейке столбца `Сумма со скидкой` запишите вычисление суммы `=I5-(I5*J5)` (как сумма - процент*сумма)
6. Сделайте методом перетягивания вычисление сумм со скидкой в остальных ячейках столбца
7. Вычислите итоговую сумму со скидками для всех товаров

### Задание 3. - Круговая диаграмма  
1. Учебное видео - [Как посчитать проценты в excel](https://www.youtube.com/watch?v=KyPJ9CJDBLY)
2.  Выделите ячейки от Наименования до Суммы и вставьте объемную круговую диаграмму `Вставка \ Диаграмма`
3. Нажмите плюс (на диаграмме, справа сверху) и измените подписи на доли - чтобы были видны суммы для каждого товара  

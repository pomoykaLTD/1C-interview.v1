# Версия тестового задания от фирмы 1С

### 1. Исходные данные представляют собой массив значений типа «Число».
*Например:*
<table>
<tr><td>3</td><td>7</td><td>-2</td><td>0</td><td>-11</td><td>6</td><td>57</td><td>2</td><td>-13</td><td>0</td><td>3</td><td>-42</td><td>19</td><td>1</td></tr>
</table>	

Необходимо реализовать алгоритм, который удалит из массива все элементы, в которых содержатся отрицательные числа.<br>

*Условия:*
1)	Порядок «годных» элементов должен остаться прежним.<br>
2)	Вернуть нужно тот же самый массив, который был получен на входе.<br>
Нельзя создать новый массив и переложить в него «годные» элементы.<br>
Результат нужно представить в виде программного кода на встроенном языке 1С (с разумными упрощениями, можно в английской нотации).

### 2. В конфигурации определены две таблицы:
<pre>
1) Регистр сведений «Курсы валют» (периодический, независимый).
  a. Измерение: Валюта.
  b. Ресурс: Курс.
2) Документ «Продажа».
  a. Табличная часть: Товар, Количество, Цена, Сумма.
  
Бизнес-логика устроена следующим образом:
1) Валютные курсы хранятся только на банковские дни.
2) Продажи совершаются в любые дни.
3) Суммы в документе «Продажа» — в рублях.
</pre>
*Пример исходных данных:*

<table><tr><td>

<table>
  <caption>Продажи</caption>
  <tr><th>Дата</th><th>Товар</th><th>Сумма</th></tr>
  <tr><td>26.08</td><td> грабли</td><td>	150</td></tr>
  <tr><td>27.08</td><td> грабли</td><td>	220</td></tr>
  <tr><td>28.08</td><td>	грабли</td><td>	356</td></tr>
  <tr><td>29.08</td><td>	грабли</td><td>	18</td></tr>
  <tr><td>30.08</td><td>	грабли</td><td>	59</td></tr>
  <tr><td>31.08</td><td>	грабли</td><td>	187</td></tr>
  <tr><td>01.09</td><td>	грабли</td><td>	225</td></tr>
  <tr><td>02.09</td><td>	грабли</td><td>	365</td></tr>
  <tr><td>03.09</td><td>	грабли</td><td>	1025</td></tr>
</table>
  
</td><td> &#8195; </td><td>

<table>
<caption>Курсы валют</caption>
<tr><th>Дата</th><th>	Валюта</th><th>	Курс</th></tr>
<tr><td>26.08</td><td>	доллар</td><td>	63.15</td></tr>
<tr><td>n/a</td><td>	n/a</td><td>	n/a</td></tr>
<tr><td>n/a</td><td>	n/a</td><td>	n/a</td></tr>
<tr><td>29.08</td><td>	доллар</td><td>	64.77</td></tr>
<tr><td>30.08</td><td>	доллар</td><td>	65.01</td></tr>
<tr><td>31.08</td><td>	доллар</td><td>	64.32</td></tr>
<tr><td>01.09</td><td>	доллар</td><td>	64.10</td></tr>
<tr><td>02.09</td><td>	доллар</td><td>	63.95</td></tr>
<tr><td>n/a</td><td>	n/a</td><td>	n/a</td></tr>
</table>
  
</td></tr></table>

Необходимо разработать запрос, при помощи которого можно будет отвечать на вопросы вида «Сколько составила выручка по товару N за период X в долларах по курсу на день продажи»?<br>
Важно: это должен быть один запрос (один пакет запросов).<br>
Обработка результата запроса кодом не допускается.<br>
Результат нужно представить в виде программного кода на встроенном языке 1С (с разумными упрощениями, можно в английской нотации).

### 3. Исходные данные представляют собой таблицу вида «Поставщик – Сумма – Добавка».  Колонка «Добавка» пустая.
<table>
<tr><th>Поставщик</th><th>	Сумма</th><th>	Добавка</th></tr>
<tr><td>А</td><td>	101.25</td><td>	</td></tr>
<tr><td>Б</td><td>	1.03</td><td>	</td></tr>
<tr><td>В</td><td>	0.04</td><td>	</td></tr>
<tr><td>Г</td><td>	529000</td><td>	</td></tr>
<tr><td>Д</td><td>	34.60</td><td>	</td></tr>
<tr><td>Е</td><td>	54.20</td><td>	</td></tr>
<tr><td>Ж</td><td>	199.88</td><td>	</td></tr>
<tr><td>З</td><td>	20548.03</td><td> </td></tr>
<tr><td>И</td><td>	10.50</td><td>	</td></tr>
<tr><td>К</td><td>	1470.78</td><td></td></tr>	
<tr><td>Л</td><td>	1.01</td><td>	</td></tr>
</table>

Также частью исходных данных является «Общая сумма добавки».<br> 
*Например:*
**542.13**

Требуется реализовать алгоритм, который выполнит распределение «Общей суммы добавки» по таблице.<br> 
Условия:<br>
1) Распределение должно быть строго пропорциональным, согласно значению в колонке «Сумма».<br>
2) Результатом являются не числа, а суммы — рубли и копейки.<br>
3) Распределение должно быть максимально точным и справедливым.<br>
4) При любом количестве повторных запусков на тех же исходных данных результат всегда должен быть одинаковым.<br>

Результат нужно представить в виде программного кода.

### 4. В конфигурации задан регистр сведений «Посетители» следующей структуры:
•	Измерение: «Посетитель» (справочник «Посетители»).<br>
•	Ресурс: «Направление» (перечисление, «Вошел, Вышел»).<br>
Регистр — периодический, независимый.<br>
*Например:*

<table>
<tr><th>Период</th><th>	Посетитель</th><th>	Направление</th></tr>
<tr><td>23.08 10:42</td><td>	А</td><td>	Вошел</td></tr>
<tr><td>23.08 10:43</td><td>	Б</td><td>	Вошел</td></tr>
<tr><td>23.08 10:44</td><td>	В</td><td>	Вошел</td></tr>
<tr><td>23.08 10:45</td><td>	Г</td><td>	Вошел</td></tr>
<tr><td>23.08 10:46</td><td>	А</td><td>	Вышел</td></tr>
<tr><td>23.08 10:47</td><td>	Д</td><td>	Вошел</td></tr>
<tr><td>23.08 10:48</td><td>	Ж</td><td>	Вошел</td></tr>
<tr><td>23.08 11:05</td><td>	А</td><td>	Вошел</td></tr>
<tr><td>23.08 11:13</td><td>	Б</td><td>	Вышел</td></tr>
<tr><td>23.08 11:22</td><td>	Г</td><td>	Вышел</td></tr>
<tr><td>23.08 11:50</td><td>	К</td><td>	Вошел</td></tr>
</table>

Физический смысл регистра: логирование прохода посетителей в некое помещение (например, посещение доклада на партнерском семинаре).<br>
Задача: подсчитать «пиковую нагрузку» на помещение за указанный промежуток времени.<br>
Под «пиковой нагрузкой» понимается максимальное количество посетителей, которые находились в помещении одновременно.<br>
Результат обязательно представлять кодом.

### 5. Исходные данные — таблица с двумя колонками, «Родитель» и «Потомок». Например, это может быть таблица связей между событиями (причина и следствие). 
Тип связи — «многие ко многим»:<br>
•	Каждому родителю может соответствовать любое количество потомков.<br> 
•	У каждого потомка может быть любое количество родителей.<br>
*Пример исходных данных:*
<table>
<tr><th>Родитель</th><th>	Потомок</th></tr>
<tr><td>А</td><td>	Г</td></tr>
<tr><td>Б</td><td>	В</td></tr>
<tr><td>Б</td><td>	Г</td></tr>
<tr><td>В</td><td>	Д</td></tr>
<tr><td>В</td><td>	Ж</td></tr>
<tr><td>Г</td><td>	Д</td></tr>
<tr><td>Д</td><td>	Е</td></tr>
<tr><td>Е</td><td>	З</td></tr>
<tr><td>Е</td><td>	К</td></tr>
<tr><td>Е</td><td>	Л</td></tr>
<tr><td>Ж</td><td>	Е</td></tr>
<tr><td>З</td><td>	Г</td></tr>
<tr><td>И</td><td>	З</td></tr>
<tr><td>К</td><td>	З</td></tr>
</table>

Необходимо дать ответ на вопрос — «Содержится ли в исходных данных зацикливание»?<br>
Зацикливанием считается ситуация, когда хотя бы одно из событий через любое количество связей оказывается замкнутым само на себя.<br>
•	Массив исходных данных может быть очень большим.<br>
•	Требования к производительности — высокие.<br>
Результат  обязательно представлять кодом.<br>

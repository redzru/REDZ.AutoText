Скачать последнюю версию REDZ.AutoText: https://github.com/redzru/REDZ.AutoText/releases

REDZ.AutoText
=============

С помощью плагина REDZ.AutoText textarea при наборе текста будет растягиваться по вертикали, чтобы весь текст помещался без скролинга.

Для использования плагина, пропишите его после подключения к jQuery:
~~~ html
<script type="text/javascript" src="redz.autotext.c.js"></script>
~~~
**У плагина есть несколько режимов работы:**

1. Обрабатывать только избранные textarea, указывая их ID при инициализации скрипта.
2. Обрабатывать все textarea на странице.

Параметры: `__InitREDZAutoText(<идентификатор>,<длина текста>)`

* `<идентификатор>` - Идентификатор `textarea`, к которому применяется плагин ИЛИ `AllTextArea` - применить плагин ко всем textarea на странице.
* `<длина текста>` - Длина текста в `textarea`, после которого начнется скролинг, чтобы объект `textarea` не был слишком "резиновым".

Для инициализации плагина в конце странице пропишите:
~~~ html
<script type="text/javascript">__InitREDZAutoText('AllTextArea',100);</script>
~~~
Где `AllTextArea` - команда для обработки всех texarea на странице. Подходит для режима работы №2.

Если вы хотите подключить плагин для какого-то определенного объекта `textarea`, подключите
~~~ html
<textarea name="example" rows="2" style="width:200px;" id="text1"></textarea>
<script type="text/javascript">__InitREDZAutoText('text1',100);</script>
~~~

Пример при выборочном подключении:
~~~ html
<textarea name="example" rows="2" style="width:200px;" id="text1"></textarea>
<textarea name="example" rows="2" style="width:200px;" id="text2"></textarea>
<textarea name="example" rows="2" style="width:200px;" id="text3"></textarea>
<script type="text/javascript">__InitREDZAutoText('text1',100);__InitREDZAutoText('text3',100);</script>
~~~
В этом примере плагин будет применен только к textarea с ID `text1` и `text3`

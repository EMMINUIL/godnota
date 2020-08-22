
Библиотеки/Модули
=================
Requests
"""""""""""""""""
Библиотека **requests** является стандартным инструментом для составления HTTP-запросов в Python. Простой и аккуратный API значительно облегчает трудоемкий процесс создания запросов. Таким образом, можно сосредоточиться на взаимодействии со службами и использовании данных в приложении.


Ключевые аспекты:

- Создание запросов при помощи самых популярных HTTP методов;
- Редактирование заголовков запросов и данных при помощи строки запроса и содержимого сообщения;
- Анализ данных запросов и откликов;
- Создание авторизированных запросов;
- Настройка запросов для предотвращения сбоев и замедления работы приложения.


**Документация**:
    https://requests.readthedocs.io/en/master/ - Requests: HTTP for Humans

Tkinter
"""""""""""""""""
Tkinter python предлагает простой и быстрый способ создания приложений с графическим интерфейсом. Tkinter - это стандартная библиотека GUI для языка программирования Python. Он предлагает мощный объектно-ориентированный интерфейс для инструментария Tk GUI.

Tkinter предлагает более 15 типов виджетов, включая кнопки, метки и текстовые поля. Каждый из них имеет доступ к некоторым конкретным методам управления геометрией, которые служат для организации виджетов по всей области родительского виджета.


Особенности:

- Поставляется с набором виджетов, которые поддерживают методы управления геометрией
- Облегчает разработку приложений с графическим интерфейсом
- Поддерживает эффективный объектно-ориентированный интерфейс





.. code-block:: Python

    from tkinter import *  
    window = Tk()  
    window.title("Добро пожаловать в приложение PythonRu")  
    lbl = Label(window, text="Привет")  
    lbl.grid(column=0, row=0)  
    window.mainloop()

.. image:: https://pythonru.com/wp-content/uploads/2019/01/uroki-po-tkinter-2.png

**Документация**:
    https://docs.python.org/3/library/tkinter.html


BeautifulSoup
"""""""""""""""""
BeautifulSoup является библиотекой Python для парсинга HTML и XML документов. Часто используется для скрапинга веб-страниц. BeautifulSoup позволяет трансформировать сложный HTML-документ в сложное древо различных объектов Python. Это могут быть теги, навигация или комментарии.

**Пример:**

.. image:: https://i.imgur.com/lhaQJGT.png


.. image:: https://i.imgur.com/svv0vMc.png





.. code:: python

    import requests
    from bs4 import BeautifulSoup
    
    page = requests.get('https://pogoda.online.ua/in/moscow/')
    soup = BeautifulSoup(page.text, "html.parser")
    t = soup.find('span', class_='supernew-temp-max mb-0 h1 deg')
    print(t.string)

**result** +22 °C

**Документация:**

https://www.crummy.com/software/BeautifulSoup/bs4/doc/

PrettyTable
===============
PrettyTable предназначена для создания таблицы выходных данных в красивом формате. Имеется функция импорта CSV-форматов.

**Пример:**

.. code:: python
    from prettytable import PrettyTable
    table = PrettyTable()
    
    table.field_names = ['Name', 'Age', 'City']
    table.add_row(["Alice", 20, "Adelaide"])
    table.add_row(["Bob", 20, "Brisbane"])
    table.add_row(["Chris", 20, "Cairns"])
    table.add_row(["David", 20, "Sydney"])
    table.add_row(["Ella", 20, "Melbourne"])
    print(table)

.. image:: https://leonardo.osnova.io/47911dd7-1c6c-a659-1c9f-e327ac6c4169/-/resize/500/
    :width: 350 px
   
**Документация:**

https://ptable.readthedocs.io/en/latest/tutorial.html
.. image:: https://i.imgur.com/lhaQJGT.png


.. image:: https://i.imgur.com/svv0vMc.png





.. code:: python

    import requests
    from bs4 import BeautifulSoup
    
    page = requests.get('https://pogoda.online.ua/in/moscow/')
    soup = BeautifulSoup(page.text, "html.parser")
    t = soup.find('span', class_='supernew-temp-max mb-0 h1 deg')
    print(t.string)

**result** +22 °C

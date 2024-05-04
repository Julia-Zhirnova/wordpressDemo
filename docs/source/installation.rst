Установка
=========

.. _installation:

XAMPP
------

Кроссплатформенная сборка локального веб-сервера, содержащая:
- Apache;
- MariaDB;
- интерпретатор скриптов PHP

Скачиваем XAMPP for Linux с официального сайта https://www.apachefriends.org/

.. image:: /_static/выбор_xampp.png
   :alt: выбор xampp
   :width: 700

Далее вводим команды в терминале от root (для переключения ввести su). Открываем терминал в папке, куда был скачан файл xampp-linux-x64-8.2.12-0-installer.run. Передаем права для запуска файла и запускаем его

.. code-block:: console

   $ chmod +x xampp-linux-x64-8.2.12-0-installer.run
   $ ./xampp-linux-x64-8.2.12-0-installer.run

.. image:: /_static/установка.png
   :alt: установка
   :width: 700

Выбираем далее и не запускаем xampp

.. image:: /_static/xampp.png
   :alt: xampp
   :width: 700

Переходим в папку, где установлен xampp и запускаем его 

.. code-block:: console

   $ /opt/lampp/lampp start
   $ dnf install libxcrypt-compat
   $ dnf install libnsl
   $ /opt/lampp/lampp start

.. image:: /_static/библиотеки.png
   :alt: библиотеки
   :width: 700
.. image:: /_static/библиотеки_2.png
   :alt: библиотеки
   :width: 700
.. image:: /_static/xampp_запущен.png
   :alt: библиотеки
   :width: 700

WordPress
----------

Для установки необходимо скачать с сайта https://ru.wordpress.org/download/ 

.. image:: /_static/скачать_wordoress.png
   :alt: скачать_wordoress
   :width: 700

Удаляем папку htdocs с ее содержимым и создаем заново 

.. code-block:: console

   $ rm -fr htdocs/
   $ mkdir htdocs/

Необходимо распаковать файл и переместить содержимое папки в /opt/lampp/htdocs/

.. code-block:: console

   $ unzip wordpress-6.5.2-ru_RU.zip
   $ cp -a /home/rexam/Загрузки/wordpress/. /opt/lampp/htdocs/

.. image:: /_static/распаковка.png
   :alt: распаковка
   :width: 700

.. autofunction:: lumache.get_random_ingredients

The ``kind`` parameter should be either ``"meat"``, ``"fish"``,
or ``"veggies"``. Otherwise, :py:func:`lumache.get_random_ingredients`
will raise an exception.

.. autoexception:: lumache.InvalidKindError

For example:

>>> import lumache
>>> lumache.get_random_ingredients()
['shells', 'gorgonzola', 'parsley']


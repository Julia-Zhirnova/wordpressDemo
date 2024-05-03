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
   :width: 100

Далее вводим команды в терминале от root (для переключения ввести su). Открываем терминал в папке, куда был скачан файл xampp-linux-x64-8.2.12-0-installer.run. Передаем права для запуска файла и запускаем его
.. code-block:: console

   $ chmod +x xampp-linux-x64-8.2.12-0-installer.run
   $ ./xampp-linux-x64-8.2.12-0-installer.run

.. image:: /_static/установка.png
   :alt: установка
   :width: 100
WordPress
----------------

To retrieve a list of random ingredients,
you can use the ``lumache.get_random_ingredients()`` function:

.. autofunction:: lumache.get_random_ingredients

The ``kind`` parameter should be either ``"meat"``, ``"fish"``,
or ``"veggies"``. Otherwise, :py:func:`lumache.get_random_ingredients`
will raise an exception.

.. autoexception:: lumache.InvalidKindError

For example:

>>> import lumache
>>> lumache.get_random_ingredients()
['shells', 'gorgonzola', 'parsley']


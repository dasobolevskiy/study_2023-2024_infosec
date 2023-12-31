---
lang: ru-RU
title: Лабораторная работа № 3
author:
  - Соболевский Денис Андреевич
date: 2023, Москва
aspectratio: 169
babel-lang: russian
babel-otherlangs: english
toc: false
toc-title: Содержание
slide_level: 2
theme: Madrid
mainfont: Times New Roman
sansfont: Arial
---

## Цели

Целью данной работы является получение практических навыков работы в консоли с атрибутами файлов для групп пользователей.

## Задачи

1. Создать новую учетную запись guest2.

2. Выполнить ряд операций в новой и старой учетных записях.

3. Сформировать таблицу "Установленные права и разрешенные действия".

4. Сформировать таблицу "Минимальные права для совершения операций".

## Ход работы

Создадим учетную запись пользователя guest2 и зададим пароль.

![Создание и настройка учетной записи guest2](image.png){#fig:001 width=90%}

## Ход работы

Добавим пользователя guest2 в группу guest.

![Добавление пользователя guest2 в группу guest](image-1.png){#fig:002 width=90%}

## Ход работы

Осуществим вход в систему от двух пользователей на двух разных консолях.

![Консоли с авторизованными пользователями](image-2.png){#fig:003 width=50%}

## Ход работы

Для обоих пользователей командой pwd определим директорию, в которой мы находимся. Видим, что приглашение в командной строке соответствует.

![Определение директории в консоли guest](image-3.png){#fig:004 width=90%}

![Определение директории в консоли guest2](image-4.png){#fig:005 width=90%}

## Ход работы

Уточним имя пользователя, его группу, кто входит в неё и к каким группам принадлежит он сам.

![Вывод информации о пользователе в консоли guest](image-5.png){#fig:006 width=40%}

![Вывод информации о пользователе в консоли guest2](image-6.png){#fig:007 width=40%}

Заметим, что все команды выводят одинаковую информацию, но в разных форматах

## Ход работы

Сравним полученную информацию с содержимым файла /etc/group.

![Содержимое файла /etc/group](image-7.png){#fig:008 width=20%}

Видим информацию о группе, ее id и название подгруппы.

## Ход работы

От имени пользователя guest2 выполним регистрацию пользователя guest2 в группе guest

![Регистрация пользователя guest2 в группе guest](image-8.png){#fig:009 width=90%}

## Ход работы

От имени пользователя guest изменим права директории /home/guest, разрешив все действия для пользователей группы

![Изменение прав директории /home/guest](image-9.png){#fig:010 width=90%}

## Ход работы

От имени пользователя guest снимем с директории /home/guest/dir1 все атрибуты

![Снятие с директории /home/guest/dir1 всех атрибутов](image-10.png){#fig:011 width=90%}

## Ход работы

Заполним таблицу «Установленные права и разрешённые действия».

![Фрагмент таблицы 3.1](image-11.png){#fig:012 width=90%}

## Ход работы

Заполним таблицу «Минимальные права для совершения операций».

![Таблица 3.2](image-12.png){#fig:013 width=50%}

## Результаты

В ходе данной лабораторной работы были получены практические навыки работы в консоли с атрибутами файлов для групп пользователей.

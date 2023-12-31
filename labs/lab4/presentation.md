---
lang: ru-RU
title: Лабораторная работа № 4
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

Целью данной работы является получение практических навыков работы в консоли с расширенными атрибутами файлов.

## Задачи

1. Исследовать доступность команд при установленном расширенном aтрибуте a.

2. Исследовать доступность команд при установленном расширенном aтрибуте i.

## Ход работы

От имени пользователя guest определим расширенные атрибуты файла /home/guest/dir1/file1.

![Расширенные атрибуты файла /home/guest/dir1/file1](image.png)

## Ход работы

Установим командой chmod 600 file1 на файл file1 права, разрешающие чтение и запись для владельца файла.

![Установка прав на файл /home/guest/dir1/file1](image-1.png)

## Ход работы

Попробуем установить на файл /home/guest/dir1/file1 расширенный атрибут "a" от имени пользователя guest.

![Попытка установки атрибута а на файл /home/guest/dir1/file1 от имени пользователя guest](image-2.png)

## Ход работы

Откроем вторую консоль с правами администратора. Установим на файл /home/guest/dir1/file1 расширенный атрибут a.

![Установка атрибута а на файл /home/guest/dir1/file1](image-3.png)

## Ход работы

Проверим правильно ли установлен атрибут.

![Атрибуты на файл /home/guest/dir1/file1](image-4.png)

## Ход работы

Дозапишем в файл file1 слова «test» и выполним чтение файла file1.

![Запись и чтение файла /home/guest/dir1/file1](image-5.png)

## Ход работы

Попробуем стереть имеющуюся в файле информацию.

![Попытка удаления информации /home/guest/dir1/file1](image-6.png)

## Ход работы

Попробуем установить на файл file1 права, запрещающие чтение и запись для владельца файла.

![Попытка установить права на файл /home/guest/dir1/file1](image-7.png)

## Ход работы

Снимем расширенный атрибут a с файла /home/guest/dirl/file1 от
имени суперпользователя.

![Снятие атрибута "а" с файла /home/guest/dir1/file](image-8.png)

## Ход работы

Повторим операции, которые нам ранее не удавалось выполнить. Теперь все операции выполняются.

![Повторение операций после снятия атрибута "а"](image-9.png)

## Ход работы

Меняем атрибут "a" на "i" и повторяем действия.

![Установка атрибута "i"](image-10.png)

## Ход работы

![Снятие атрибута "i](image-11.png)

## Результаты

В данной лабораторной работе были получены практические навыки работы в консоли с расширенными атрибутами файлов.

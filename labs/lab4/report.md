---
title: "Лабораторная работа № 4"
subtitle: "Дискреционное разграничение прав в Linux. Расширенные атрибуты"
author: "Соболевский Денис Андреевич"
lang: ru-RU
toc-title: "Содержание"
toc: true 
toc-depth: 2
lof: true 
lot: false
fontsize: 12pt
linestretch: 1.5
papersize: a4
documentclass: scrreprt
polyglossia-lang:
  name: russian
  options:
	- spelling=modern
	- babelshorthands=true
polyglossia-otherlangs:
  name: english
babel-lang: russian
babel-otherlangs: english
mainfont: "Times New Roman"
sansfont: Arial
monofont: "Courier New"
biblatex: true
biblio-style: "gost-numeric"
biblatexoptions:
  - parentracker=true
  - backend=biber
  - hyperref=auto
  - language=auto
  - autolang=other*
  - citestyle=gost-numeric
figureTitle: "Рис."
tableTitle: "Таблица"
listingTitle: "Листинг"
lofTitle: "Список иллюстраций"
lotTitle: "Список таблиц"
lolTitle: "Листинги"
indent: true
header-includes:
  - \usepackage[utf8]{inputenc}
  - \usepackage[T2A]{fontenc}
---

# Цель работы

Целью данной работы является получение практических навыков работы в консоли с расширенными атрибутами файлов.

# Задание

1. Исследовать доступность команд при установленном расширенном aтрибуте a.

2. Исследовать доступность команд при установленном расширенном aтрибуте i.

# Теоретическое введение

- Операционная система — это комплекс программ, предназначенных для управления ресурсами компьютера и организации взаимодействия с пользователем.

- Права доступа определяют, какие действия конкретный пользователь может или не может совершать с определенным файлами и каталогами. С помощью разрешений можно создать надежную среду — такую, в которой никто не может поменять содержимое ваших документов или повредить системные файлы.

# Выполнение лабораторной работы

1. От имени пользователя guest определим расширенные атрибуты файла /home/guest/dir1/file1.

![Расширенные атрибуты файла /home/guest/dir1/file1](image.png)

2. Установим командой chmod 600 file1 на файл file1 права, разрешающие чтение и запись для владельца файла.

![Установка прав на файл /home/guest/dir1/file1](image-1.png)

3. Попробуем установить на файл /home/guest/dir1/file1 расширенный атрибут "a" от имени пользователя guest.

![Попытка установки атрибута а](image-2.png)

4. Откроем вторую консоль с правами администратора. Установим на файл /home/guest/dir1/file1 расширенный атрибут a.

![Установка атрибута а на файл /home/guest/dir1/file1](image-3.png)

5. Проверим правильно ли установлен атрибут.

![Атрибуты на файл /home/guest/dir1/file1](image-4.png)

6. Дозапишем в файл file1 слова «test» и выполним чтение файла file1.

![Запись и чтение файла /home/guest/dir1/file1](image-5.png)

7. Попробуем стереть имеющуюся в файле информацию.

![Попытка удаления информации /home/guest/dir1/file1](image-6.png)

8. Попробуем установить на файл file1 права, запрещающие чтение и запись для владельца файла.

![Попытка установить права на файл /home/guest/dir1/file1](image-7.png)

9. Снимем расширенный атрибут a с файла /home/guest/dirl/file1 от
   имени суперпользователя.

![Снятие атрибута "а" с файла /home/guest/dir1/file1](image-8.png)

10. Повторим операции, которые нам ранее не удавалось выполнить. Теперь все операции выполняются.

![Повторение операций после снятия атрибута "а"](image-9.png)

11. Меняем атрибут "a" на "i" и повторяем действия.

![Установка атрибута "i"](image-10.png)

![Снятие атрибута "i"](image-11.png)

# Выводы

В данной лабораторной работе были получены практические навыки работы с расширенными атрибутами файлов.

# Список литературы

[1] https://codeby.school/blog/informacionnaya-bezopasnost/razgranichenie-dostupa-v-linux-znakomstvo-s-astra-linux

[2] https://debianinstall.ru/diskretsionnoe-razgranichenie-dostupa-linux/

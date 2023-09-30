---
title: "Лабораторная работа № 3"
subtitle: "Дискреционное разграничение прав в Linux. Два пользователя"
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

Целью данной работы является получение практических навыков работы в консоли с атрибутами файлов для групп пользователей.

# Задание

1. Создать новую учетную запись guest2.

2. Выполнить ряд операций в новой и старой учетных записях.

3. Сформировать таблицу "Установленные права и разрешенные действия".

4. Сформировать таблицу "Минимальные права для совершения операций".

# Теоретическое введение

- Операционная система — это комплекс программ, предназначенных для управления ресурсами компьютера и организации взаимодействия с пользователем.

- Права доступа определяют, какие действия конкретный пользователь может или не может совершать с определенным файлами и каталогами. С помощью разрешений можно создать надежную среду — такую, в которой никто не может поменять содержимое ваших документов или повредить системные файлы.

# Выполнение лабораторной работы

1. Первые два пункта были выполнены в предыдущей лабораторной работе. Создаем учетную запись guest2.

![Создание новой учетной записи](image.png)

2. Добавим пользователя guest2 в группу guest.

![Добавление нового пользователя в группу guest](image-1.png)

3. Войдем в учетные записи с разных консолей.

![Вход в учетные записи с двух консолей](image-2.png)

4. Для обоих пользователей командой pwd определим директорию, в которой мы находимся. Приглашение в командной строке соответствует.

![Определение директории в консоли guest](image-4.png)

![Определение директории в консоли guest2](image-3.png)

5. Уточним имя пользователя, его группу, кто входит в неё и к каким группам принадлежит он сам.

![Вывод информации о пользователе в консоли guest](image-5.png)

![Вывод информации о пользователе в консоли guest2](image-6.png)

Все команды выводят одну и ту же информацию в разных форматах.

6. Сравним полученную информацию с содержимым файла /etc/group.

![Содержимое файла](image-7.png)

Отображается группа, ее id и название подгруппы.

7. От имени пользователя guest2 выполним регистрацию пользователя guest2 в группе guest.

![Регистрация пользователя guest2 в группе guest](image-8.png)

8. От имени пользователя guest изменим права директории /home/guest, разрешив все действия для пользователей группы.

![Изменение прав директории /home/guest](image-9.png)

9. От имени пользователя guest снимем с директории /home/guest/dir1 все атрибуты командой chmod 000 dir1.

![Снятие атрибутов](image-10.png)

10. Заполним первую таблицу.

![Фрагмент таблицы 3.1](image-11.png)

11. Заполним вторую таблицу.

![Таблица 3.2](image-12.png)

# Выводы

В ходе лабораторной работы были получены практические навыки работы в консоли с атрибутами файлов для групп пользователей.

# Список литературы{.unnumbered}

[1] https://codeby.school/blog/informacionnaya-bezopasnost/razgranichenie-dostupa-v-linux-znakomstvo-s-astra-linux

[2] https://debianinstall.ru/diskretsionnoe-razgranichenie-dostupa-linux/
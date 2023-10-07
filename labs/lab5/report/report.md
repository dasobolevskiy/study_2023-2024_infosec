---
title: "Лабораторная работа № 5"
subtitle: "Дискреционное
разграничение прав в Linux. Исследование
влияния дополнительных атрибутов"
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

Изучение механизмов изменения идентификаторов, применения
SetUID- и Sticky-битов. Получение практических навыков работы в консоли с дополнительными атрибутами. Рассмотрение работы механизма
смены идентификатора процессов пользователей, а также влияние бита
Sticky на запись и удаление файлов.

# Задание

1. Исследовать влияние дополнительных атрибутов.

2. Исследовать Sticky-бит.

# Теоретическое введение

- Операционная система — это комплекс программ, предназначенных для управления ресурсами компьютера и организации взаимодействия с пользователем.

- Права доступа определяют, какие действия конкретный пользователь может или не может совершать с определенным файлами и каталогами. С помощью разрешений можно создать надежную среду — такую, в которой никто не может поменять содержимое ваших документов или повредить системные файлы.

# Выполнение лабораторной работы

1. От имени пользователя guest создадим программу simpleid.c, скомпилируем ее и убедимся, что файл программы создан.

![Создание программы simleid.c](image.png).

2. Выполним команды ./simpleid и id и убедимся, что полученные данные совпадают.

![Выполнение команд ./simpleid и id](image-1.png)

3. Усложним программу, добавив вывод действительных индентификаторов.

![Создание и программы simpleid2](image-2.png)

4. От имени суперпользователя выполним команды.

![Установка новых атрибутов и смена владельца файла simpleid2](image-3.png)

5. Выполним команды ./simpleid2 и id и убедимся, что полученные данные совпадают.

![Использование команд ./simpleid2 и id](image-4.png)

6. Выполним проверку правильности установки новых атрибутов.

![Выполнение команды ls -l simpleid2](image-5.png)

7. Создадим и скомпилируем программу readfile.c.

![Создание программы readfile.c](image-6.png)

8. Сменим владельца у файла readfile.c и изменим права так, чтобы только суперпользователь (root) мог прочитать его, a guest не мог.

![Изменение владельца и прав файла readfile.c](image-7.png)

9. Проверим, что пользователь guest не может прочитать файл readfile.c.

![Проверка, что пользователь guest не может прочитать файл readfile.c](image-8.png)

10. Сменим владельца и установим SetUID-бит.

![Смена прав файла](image-9.png)

11. Проверим, может ли программа readfile прочитать файл readfile.c.

![Чтение файла readfile.c](image-10.png)

12. Проверим, может ли программа readfile прочитать файл /etc/shadow.

![Чтение файла /etc/shadow](image-11.png)

13. Выясним, установлен ли атрибут Sticky на директории /tmp.

![Выполнение команды ls -l / | grep tmp](image-12.png)

14. От имени пользователя guest создадим файл file01.txt в директории /tmp.

![Создание файла file01.txt](image-13.png)

15. От пользователя guest2 попробуем прочитать файл file01.txt.

![Чтение файла file01.txt](image-14.png)

16. От пользователя guest2 попробуем дозаписать файл file01.txt.

![Дозапись в файл /tmp/file01.txt](image-15.png)

17. От пользователя guest2 попробуем записать в файл file01.txt слово test3, стерев при этом всю имеющуюся в файле информацию.

![Перезапись в файле /tmp/file01.txt](image-16.png)

18. От пользователя guest2 попробуем удалить файл file01.txt.

![Удаление файла /tmp/file01.txt](image-17.png)

19. От имени суперпользователя снимем атрибут t с директории /tmp..

![Удаление атрибута t](image-18.png)

20. Повторим предыдущие шаги. Теперь файл удален успешно.

![Повторение предыдущих шагов](image-19.png)

21. Повысим свои права до суперпользователя и вернем атрибут t на директорию /tmp.

![Повышение прав и возвращение атрибута](image-20.png)

# Выводы

В рамках данной лабораторной работы были изучены механизмы изменения идентификаторов, применения SetUID- и Sticky-битов. Получены практические навыков работы в консоли с дополнительными атрибутами. Рассмотрены принципы работы механизма смены идентификатора процессов пользователей, а также влияние бита
Sticky на запись и удаление файлов.

# Список литературы

[1] https://codeby.school/blog/informacionnaya-bezopasnost/razgranichenie-dostupa-v-linux-znakomstvo-s-astra-linux

[2] https://www.researchgate.net/profile/Dmitry-Kulyabov/publication/339290917_Informacionnaa_bezopasnost_komputernyh_setej_laboratornye_raboty/links/5e482028299bf1cdb92e26d4/Informacionnaa-bezopasnost-komputernyh-setej-laboratornye-raboty.pdf

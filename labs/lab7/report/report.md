---
title: "Лабораторная работа № 7"
subtitle: "Элементы криптографии. Однократное гаммирование"
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

Освоить на практике применение режима однократного гаммирования.

# Задание

Нужно подобрать ключ, чтобы получить сообщение «С Новым Годом,
друзья!». Требуется разработать приложение, позволяющее шифровать и
дешифровать данные в режиме однократного гаммирования. Приложение
должно:

1. Определить вид шифротекста при известном ключе и известном открытом тексте.
2. Определить ключ, с помощью которого шифротекст может быть преобразован в некоторый фрагмент текста, представляющий собой один из
   возможных вариантов прочтения открытого текста.

# Теоретическое введение

- Шифрование — это процесс кодирования информации с целью предотвращения несанкционированного доступа. В случае кражи или утечки зашифрованные данные будут недоступны для прочтения без соответствующего ключа.

- Гаммирование - преобразование исходного (открытого) текста, при котором символы исходного текста складываются (по модулю, равному мощности алфавита) с символами псевдослучайной последовательности, вырабатываемой по определенному правилу.

# Выполнение лабораторной работы

1. Импортируем модули.

![Импорт модулей](image-1.png)

2. Напишем функцию для преобразования данных в шестнадцатеричный формат.

![Первая функция](image-2.png)

3. Напишем функцию для генерации ключа.

![Вторая функция](image-3.png)

4. Реализуем функцию для кодирования и декодирования данных.

![Третья функция](image-4.png)

5. Закодируем и декодируем сообщение "С Новым годом, друзья!".

![Кодирование и декодирование собщение](image-5.png)

6. Получим ключ, с помощью которого получим сообщение "С Новым годом, коллега", вместо "С Новым годом, друзья!" при декодировании. Воспользуемся симметричностью кодирования.

![Получение ключа для другого прочтения открытого текста](image-6.png)

# Выводы

В данной лабораторной работе было освоено на практике применение режима однократного гаммирования.

# Список литературы{.unnumbered}

[1] https://www.eset.com/ua-ru/support/information/entsiklopediya-ugroz/shifrovaniye/

[2] https://www.finam.ru/publications/item/gammirovanie-20230628-2028/
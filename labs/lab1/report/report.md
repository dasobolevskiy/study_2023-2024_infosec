---
## Front matter
title: "Лабораторная работа № 1"
subtitle: "Установка и конфигурация
операционной системы на виртуальную машину и подготовка репозитория"
author: "Соболевский Денис Андреевич"

## Generic otions
lang: ru-RU
toc-title: "Содержание"

## Bibliography
bibliography: bib/cite.bib
csl: pandoc/csl/gost-r-7-0-5-2008-numeric.csl

## Pdf output format
toc: true # Table of contents
toc-depth: 2
lof: true # List of figures
lot: false
fontsize: 12pt
linestretch: 1.5
papersize: a4
documentclass: scrreprt
## I18n polyglossia
polyglossia-lang:
  name: russian
  options:
	- spelling=modern
	- babelshorthands=true
polyglossia-otherlangs:
  name: english
## I18n babel
babel-lang: russian
babel-otherlangs: english
## Fonts
mainfont: PT Serif
romanfont: PT Serif
sansfont: PT Sans
monofont: PT Mono
mainfontoptions: Ligatures=TeX
romanfontoptions: Ligatures=TeX
sansfontoptions: Ligatures=TeX,Scale=MatchLowercase
monofontoptions: Scale=MatchLowercase,Scale=0.9
## Biblatex
biblatex: true
biblio-style: "gost-numeric"
biblatexoptions:
  - parentracker=true
  - backend=biber
  - hyperref=auto
  - language=auto
  - autolang=other*
  - citestyle=gost-numeric
## Pandoc-crossref LaTeX customization
figureTitle: "Рис."
tableTitle: "Таблица"
listingTitle: "Листинг"
lofTitle: "Список иллюстраций"
lotTitle: "Список таблиц"
lolTitle: "Листинги"
## Misc options
indent: true
header-includes:
  - \usepackage{indentfirst}
  - \usepackage{float} # keep figures where there are in the text
  - \floatplacement{figure}{H} # keep figures where there are in the text
---

# Цель работы

Целью данной работы является приобретение практических навыков
установки операционной системы на виртуальную машину, настройки минимально необходимых для дальнейшей работы сервисов, а также изучение средств контроля версий и получение навыков работы с git.

# Задание

1. Установить и настроить ОС Linux на виртуальную машину.

2. Подготовить репозиторий для дальнейшей работы.

# Теоретическое введение

- Операционная система — это комплекс программ, предназначенных для управления ресурсами компьютера и организации взаимодействия с пользователем.

# Выполнение лабораторной работы

1. Создаем виртуальную машину.

![Окно создания](image-1.png)

2. Запускаем виртуальную машину

![Настройка ОС](image-2.png)

3. Отрываем терминал и выводим следующую информацию:

![Версия ядра Linux (Linux version)](image-3.png)

![Частота процессора (Detected Mhz processor)](image-4.png)

![Модель процессора (CPU0)](image-5.png)

![Объем доступной оперативной памяти (Memory available)](image-6.png)

![Тип обнаруженного гипервизора (Hypervisor detected)](image-7.png)

![Тип файловой системы корневого раздела](image-8.png)

![Последовательность монтирования файловых систем](image-9.png)

# Выводы

Были приобретены практические навыки установки операционной системы на виртуальную машину, настройки минимально необходимых для дальнейшей работы сервисов.

# Список литературы

https://sevo44.ru/rocky-linux-8-ustanovka-i-nastrojka/

https://www.dz-techs.com/ru/goodbye-centos-how-to-install-rocky-linux

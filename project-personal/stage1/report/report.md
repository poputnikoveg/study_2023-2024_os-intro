---
## Front matter
title: "Отчёт по лабораторной работе №1"
author: "Попутников Егор Сергеевич"

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
lot: true # List of tables
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

Целью данной работы является приобретение практических навыков установки операционной системы на виртуальную машину, настройки минимально необходимых для дальнейшей работы сервисов.

# Задание

Установить и настроить виртуальную машину.

# Выполнение лабораторной работы

Переключимся на роль супер-пользователя и обновим все пакеты .(рис.1 [-@fig:001]

![](image/l1 1.jpg){#fig:001 width=70%}

Установим программы для упрощения работы.(рис.2 [-@fig:002])

![](image/l1.jpg){#fig:002 width=70%}

Установим pandoc(рис.3 [-@fig:003])

![](image/l1 2.jpg){#fig:003 width=70%}

Установим TexLive.(рис.4[-@fig;004])

![](image/l1 3.jpg){#fig:004 width=70%}

Выполним домашнее задание.(рис.5 [-@fig;005])

![](image/l1 4.jpg){#fig:005 width=70%}

![](image/l1 5.jpg){#fig:006 width=70%}

![](image/l1 6.jpg){#fig:007 width=70%}

![](image/l1 7.jpg){#fig:008 width=70%}



# Выводы

Я приобрёл навыки установки и минимальной настройки витруальной машины.


---
## Front matter
lang: ru-RU
title: Презентация к лабораторной работе №1
author:
  - Попутников Егор Сергеевич
institute:
  - Российский университет дружбы народов, Москва, Россия
date: 28 февраля 2024 года

## i18n babel
babel-lang: russian
babel-otherlangs: english

## Formatting pdf
toc: false
toc-title: Содержание
slide_level: 2
aspectratio: 169
section-titles: true
theme: metropolis
header-includes:
 - \metroset{progressbar=frametitle,sectionpage=progressbar,numbering=fraction}
 - '\makeatletter'
 - '\beamer@ignorenonframefalse'
 - '\makeatother'
## Fonts
mainfont: PT Serif
romanfont: PT Serif
sansfont: PT Sans
monofont: PT Mono
mainfontoptions: Ligatures=TeX
romanfontoptions: Ligatures=TeX
sansfontoptions: Ligatures=TeX,Scale=MatchLowercase
monofontoptions: Scale=MatchLowercase,Scale=0.9
---


# Информация

## Докладчик

:::::::::::::: {.columns align=center}
::: {.column width="70%"}

  * Попутников Егор Сергеевич
  * Студент НПИбд-02-23
  * Российский университет дружбы народов

## Актуальность

Для работы каждому студенту направления прикладной информатики необходимо иметь виртуальную машину и навыки для её первоначальной настройки.

## Цели и задачи


Целью данной работы является приобретение практических навыков установки операционной системы на виртуальную машину, настройки минимально необходимых для дальнейшей работы сервисов.



## Выполнение лабораторной работы №1.

Для начала необходимо установить Virtual Box на свой ПК.
Далее, установить операционную систему с загрузочного диска.
Перейти в консоль и переключиться на роль супер-пользователя.(sudo -i)
Обновить все пакеты.(dnf -y update)
Установить программы для удобства работы в консоли(dnf -y install tmux mc)
Установить автоматические обновления(при необходимости(dnf install dnf-automatic)
Установить необходимые драйвера для виртуальной машины.
Настроить раскладку клавиатуры.
Самое важное это установить Pandoc и TexLive.

## Вывод.

Установить и настроить виртуальную машину совсем не сложно, но очень важно для выполнения лабораторных работ. Я приобрел необходимые навыки для этого.

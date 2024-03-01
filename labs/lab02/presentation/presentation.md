---
## Front matter
lang: ru-RU
title: Презентация к лабораторной работе №2
author:
  - Попутников Егор Сергеевич
institute:
  - Российский университет дружбы народов, Москва, Россия
date: 1 марта 2024 года

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

Для хранения лабораторных работ и их отчётов, необходимо иметь доступ к облачному хранилищу,как гитхаб, именно поэтому важно уметь пользоваться им.

## Цели и задачи


Целью работы является настройка git.



## Выполнение лабораторной работы №1.

Установка git

Установим git:
dnf install git
Установка gh:
dnf install gh

Базовая настройка git
Зададим имя и email владельца репозитория:

git config --global user.name "egpoputnikov"
git config --global user.email "poputnikov-egor1@mail"
Настроим utf-8 в выводе сообщений git:

git config --global core.quotepath false
Зададим имя начальной ветки (будем называть её master):

git config --global init.defaultBranch master
Параметр autocrlf:

git config --global core.autocrlf input

Параметр safecrlf:
git config --global core.safecrlf warn

Создайте ключи ssh

по алгоритму rsa с ключём размером 4096 бит:
ssh-keygen -t rsa -b 4096

по алгоритму ed25519:
 ssh-keygen -t ed25519

Создайте ключи pgp
генерируем ключ

gpg --full-generate-key

Из предложенных опций выбираем:
тип RSA and RSA;
размер 4096;
выберите срок действия; значение по умолчанию — 0 (срок действия не истекает никогда).
GPG запросит личную информацию, которая сохранится в ключе:
Имя (не менее 5 символов).
Адрес электронной почты.
При вводе email убедитесь, что он соответствует адресу, используемому на GitHub.
Комментарий. Можно ввести что угодно или нажать клавишу ввода, чтобы оставить это поле пустым.

Настройка github

Создайте учётную запись на https://github.com.
Заполните основные данные на https://github.com.

Добавление PGP ключа в GitHub

Выводим список ключей и копируем отпечаток приватного ключа:

gpg --list-secret-keys --keyid-format LONG

Отпечаток ключа — это последовательность байтов, используемая для идентификации более длинного, по сравнению с самим отпечатком ключа.

    
Cкопируйте ваш сгенерированный PGP ключ в буфер обмена:

    gpg --armor --export <PGP Fingerprint> | xclip -sel clip

Перейдите в настройки GitHub (https://github.com/settings/keys), нажмите на кнопку New GPG key и вставьте полученный ключ в поле ввода.

Настройка автоматических подписей коммитов git

Используя введёный email, укажите Git применять его при подписи коммитов:

    git config --global user.signingkey <PGP Fingerprint>
    git config --global commit.gpgsign true
    git config --global gpg.program $(which gpg2)

Настройка gh
Для начала необходимо авторизоваться

gh auth login

Утилита задаст несколько наводящих вопросов.
Авторизоваться можно через броузер.

Шаблон для рабочего пространства

Рабочее пространство для лабораторной работы
Репозиторий: https://github.com/yamadharma/course-directory-student-template.

Сознание репозитория курса на основе шаблона

    mkdir -p ~/work/study/2022-2023/"Операционные системы"
    cd ~/work/study/2022-2023/"Операционные системы"
    gh repo create study_2022-2023_os-intro --template=yamadharma/course-directory-student-template --public
    git clone --recursive git@github.com:<owner>/study_2022-2023_os-intro.git os-intro

Настройка каталога курса
Перейдите в каталог курса:
cd ~/work/study/2022-2023/"Операционные системы"/os-intro
Удалите лишние файлы:
rm package.json

Создайте необходимые каталоги:

echo os-intro > COURSE
make

Отправьте файлы на сервер:

    git add .
    git commit -am 'feat(main): make course structure'
    git push



## Вывод.

Я научился пользоваться git.

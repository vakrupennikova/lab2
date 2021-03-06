---
## Front matter
lang: ru-RU
title: Laboratory №15
author: |
	Krupennikova V.
institute: |
	RUDN University, Moscow, Russian Federation
	
date: MAY--2021

## Formatting
toc: false
slide_level: 2
theme: metropolis
header-includes: 
 - \metroset{progressbar=frametitle,sectionpage=progressbar,numbering=fraction}
 - '\makeatletter'
 - '\beamer@ignorenonframefalse'
 - '\makeatother'
aspectratio: 43
section-titles: true
---

## Цель работы

Приобретение практических навыков работы с именованными каналами.

## Задание

1.Ознакомиться с теоретическим материалом.

2.Изучить основы программирования в оболочке ОС UNIX/Linux.

3.Выполнить упражнения.

4.Ответить на контрольные вопросы.

## Выполнение:

1) Для начала я создала необходимые файлы с помощью команды «touch common.h server.c client.c Makefile» и открыла редактор emacs для их редактирования. 

![Создание файлов](image/1.png){ #fig:001 width=70% }

##

2) Далее я изменила коды программ, представленных в тексте лабораторной работы. 

В файл common.h добавила стандартные заголовочные файлы unistd.h и time.h, необходимые для работы кодов других файлов. Common.h предназначен для заголовочных файлов, чтобы в остальных программах их не прописывать каждый раз. 

![Скрипт common.h](image/2.png){ #fig:002 width=60% }

##

В файл server.c добавила цикл while для контроля за временем работы сервера. Разница между текущим временем time(NULL) и временем начала работы clock_t start=time(NULL) (инициализация до цикла) не должна превышать 30 секунд.

![Скрипт server.c](image/3.png){ #fig:003 width=60% }

##

![Скрипт server.c продолжение](image/4.png){ #fig:004 width=60% }

##

В файл client.c добавила цикл, который отвечает за количество сообщений о текущем времени (4 сообщения), которое получается в результате выполнения команд (/* текущее время */) и команду sleep(5) для приостановки работы клиента на 5 секунд.

![Скрипт client.c](image/6.png){ #fig:006 width=60% }

##

![Скрипт client.c продолжение](image/7.png){ #fig:007 width=60% }

##

Makefile (файл для сборки) не изменяла.

![Скрипт Makefile](image/8.png){ #fig:008 width=60% }

##

3) После написания кодов я, используя команду «make all», скомпилировала необходимые файлы. 

##

Далее я проверила работу написанного кода. Отрыла 3 консоли (терминала) и запустила:  в первом терминале − «./server», в остальных двух – «./client». 

В результате каждый терминал - клиент вывел по 4 сообщения. Спустя 30 секунд работа сервера была прекращена. Программа работает корректно.

![Консоли](image/10.png){ #fig:010 width=60% }

##

Также я отдельно проверила длительность работы сервера, введя команду «./server» в одном терминале. Он завершил свою работу через 30 секунд.

![Команда «./server»](image/11.png){ #fig:011 width=70% }

Если сервер завершит свою работу, не закрыв канал, то, когда мы будем запускать этот сервер снова, появится ошибка «Невозможно создать FIFO», так как у нас уже есть один канал.


## Вывод

В ходе выполнения данной лабораторной работы я приобрела практические навыки работы с именованными каналами.

##

The end.


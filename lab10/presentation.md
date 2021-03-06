---
## Front matter
lang: ru-RU
title: Laboratory №10
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

Познакомиться с операционной системой Linux. Получить практические навыки работы с редактором Emacs.

## Задание

1.Ознакомиться с теоретическим материалом.
2.Ознакомиться с редактором emacs.
3.Выполнить упражнения.
4.Ответить на контрольные вопросы.

## Выполнение:

1) Откроем редактор Emacs с помощью команды «emacs&» пути.

![Открытие редактора](image/1.png){ #fig:001 width=70% }

![Редактор](image/2.png){ #fig:002 width=70% }

## 

2) Создадим файл lab10.sh с помощью комбинации «Ctrl-x»«Ctrl-f».

![Создание файла](image/3.png){ #fig:003 width=70% }

##

3) В открывшемся буфере наберем необходимый текст

![Набор текста](image/4.png){ #fig:004 width=70% }

##

4) Сохраним файл с помощью комбинации «Ctrl-x»«Ctrl-s».

5.1) Вырежем одной командой целую строку («Сtrl-k»)

![Вырезка строки](image/5.png){ #fig:005 width=70% }

##

5.2) Вставим эту строку в конец файла («Ctrl-y») 

![Вставка строки](image/6.png){ #fig:006 width=70% }

##

5.3) Выделим область текста («Ctrl-space») 

![Выделение области текста](image/7.png){ #fig:007 width=70% }

##

5.4) Скопируем область в буфер обмена («Alt-w»).
5.5) Вставим область в конец файла(«Ctrl-y») 

![Вставка области текста](image/8.png){ #fig:008 width=70% }

##

5.6) Вновь выделим эту область(«Ctrl-space»)

![Выделение области](image/9.png){ #fig:009 width=70% }

##

и на этот раз вырежем её («Ctrl-w»)

![Вырезка области](image/10.png){ #fig:010 width=70% }

##

5.7) Отменим последнее действие («Ctrl-/»)

![Отмена последнего действия](image/11.png){ #fig:011 width=70% }

##

6.1) Переместим курсор в начало строки («Ctrl-a») 

6.2) Переместим курсор в конец строки («Ctrl-e») 

6.3) Переместим курсор в начало буфера («Alt-<»)

![Курсор в начале буфера](image/15.png){ #fig:015 width=70% }

##

6.4) Переместим курсор в конец буфера («Alt->») 

![Курсор в конце буфера](image/16.png){ #fig:016 width=70% }

##

7.1) Выведем список  активных  буферов  на  экран  («Ctrl-x»«Ctrl-b») 

![Список активных буферов](image/17.png){ #fig:017 width=70% }

##

7.2) Переместимся во  вновь  открытое  окно  («Ctrl-xo») со  списком открытых буферов

![Перемещение в окно со списком буферов](image/18.png){ #fig:018 width=70% }

##

и переключимся на другой буфер(для этого необходимо нажать на «enter» после выбора необходимого буфера) 

![Переключение на другой буфер](image/19.png){ #fig:019 width=70% }

##

7.3) Закроем это окно («Ctrl-x0») 

![Закрытие окна](image/20.png){ #fig:020 width=70% }

##

7.4) Теперь вновь переключимся между буферами, но уже без вывода их списка на экран («Ctrl-x b») 

![Переключение между буферами](image/22.png){ #fig:022 width=70% }

##

8.1) Поделим фрейм  на  4  части:  разделим  фрейм  на  два  окна  по вертикали («Ctrl-x 3»), а затем каждое из этих окон на две части по горизонтали («Ctrl-x 2»)

![Деление фрейма](image/23.png){ #fig:023 width=70% }

![Деление фрейма](image/24.png){ #fig:024 width=70% }

![Деление фрейма](image/25.png){ #fig:025 width=70% }

##

8.2) В каждом из четырёх созданных окон откроем новый буфер (файл) и введемнесколько строк текста. Для этого предварительно создадим эти файлы с помощью команд «touchexample1.txt»,«touchexample2.txt», «touchexample3.txt», «touchexample4.txt»

![Создание файлов](image/26.png){ #fig:026 width=70% }

![Открытие нового буфера](image/27.png){ #fig:027 width=70% }

![Вывод на экран](image/28.png){ #fig:028 width=70% }

##

9.1) Переключимсяв режим поиска («Ctrl-s») и найдем несколько слов, присутствующих в тексте 

![Поиск слова](image/29.png){ #fig:029 width=70% }

![Поиск слова](image/30.png){ #fig:030 width=70% }

##

9.2) Переключимся между  результатами  поиска,  нажимая «Ctrl-s»

9.3) Выйдемиз режима поиска, нажав «Ctrl-g»

9.4) Перейдем в  режим  поиска  и  замены  («Alt-%»),  введем текст, который следует найти и заменить, нажмем«enter», затем введем текст для  замены.  После  того  как  будут  подсвечены  результаты  поиска, нажмем «!» для подтверждения замены.Важно, чтобы курсор находился в начале текста.

![Замена](image/34.png){ #fig:034 width=70% }

##

9.5) Пробуемдругой режим поиска, нажав «Alt-so»
Данный вид поиска отличается от обычного тем, что тут считывается строка поиска,  которая трактуется как  регулярное  выражение, и не осуществляется поиск точного совпадения в тексте буфера.Регулярное выражение − это образец, который обозначает набор строк, возможно, и неограниченный набор.


##

The end.


---
# Front matter
lang: ru-RU
title: "Лабораторная работа №10"
subtitle: "Дисциплина: Операционные системы"
author: "Колчева Юлия вячеславовна"

# Formatting
toc-title: "Содержание"
toc: true # Table of contents
toc_depth: 2
lof: true # List of figures
lot: true # List of tables
fontsize: 12pt
linestretch: 1.5
papersize: a4paper
documentclass: scrreprt
polyglossia-lang: russian
polyglossia-otherlangs: english
mainfont: PT Serif
romanfont: PT Serif
sansfont: PT Sans
monofont: PT Mono
mainfontoptions: Ligatures=TeX
romanfontoptions: Ligatures=TeX
sansfontoptions: Ligatures=TeX,Scale=MatchLowercase
monofontoptions: Scale=MatchLowercase
indent: true
pdf-engine: lualatex
header-includes:
  - \linepenalty=10 # the penalty added to the badness of each line within a paragraph (no associated penalty node) Increasing the value makes tex try to have fewer lines in the paragraph.
  - \interlinepenalty=0 # value of the penalty (node) added after each line of a paragraph.
  - \hyphenpenalty=50 # the penalty for line breaking at an automatically inserted hyphen
  - \exhyphenpenalty=50 # the penalty for line breaking at an explicit hyphen
  - \binoppenalty=700 # the penalty for breaking a line at a binary operator
  - \relpenalty=500 # the penalty for breaking a line at a relation
  - \clubpenalty=150 # extra penalty for breaking after first line of a paragraph
  - \widowpenalty=150 # extra penalty for breaking before last line of a paragraph
  - \displaywidowpenalty=50 # extra penalty for breaking before last line before a display math
  - \brokenpenalty=100 # extra penalty for page breaking after a hyphenated line
  - \predisplaypenalty=10000 # penalty for breaking before a display
  - \postdisplaypenalty=0 # penalty for breaking after a display
  - \floatingpenalty = 20000 # penalty for splitting an insertion (can only be split footnote in standard LaTeX)
  - \raggedbottom # or \flushbottom
  - \usepackage{float} # keep figures where there are in the text
  - \floatplacement{figure}{H} # keep figures where there are in the text
---

# Цель работы

Познакомиться с операционной системой Linux. Получить практические навыки работы с редактором Emacs.


# Выполнение лабораторной работы

Откроем редактор Emacs с помощью команды «emacs» (рис. -@fig:001)

![Запуск](image/1.png){ #fig:001 width=70% }

Создадим файл lab07.sh с помощью комбинации «Ctrl-x»«Ctrl-f». (рис. -@fig:002)

![Создание](image/2.png){ #fig:002 width=70% }

В открывшемся буфере наберем необходимый текст и сохраним файл с помощью комбинации «Ctrl-x»«Ctrl-s»(рис. -@fig:003)

![Вводим текст](image/3.png){ #fig:003 width=70% }

Вырежем одной командой целую строку («Сtrl-k») (рис. -@fig:004)

![Вырежем строку](image/4.png){ #fig:004 width=70% }

Вставим эту строку в конец файла («Ctrl-y») (рис. -@fig:005)

![Вставим строку](image/5.png){ #fig:005 width=70% }

Выделим область текста («Ctrl-space»)(рис. -@fig:006)

![Выделение](image/6.png){ #fig:006 width=70% }

Скопируем область в буфер обмена («Alt-w»). Вставим область в конец файла («Ctrl-y») (рис. -@fig:007) 

![Вставить строку](image/7.png){ #fig:007 width=70% }

Вновь выделим эту область(«Ctrl-space») и на этот раз вырежем её («Ctrl-w») (рис. -@fig:008)

![Вырезание строки](image/8.png){ #fig:008 width=70% }

Отменим последнее действие («Ctrl-/»). Переместим курсор в начало строки («Ctrl-a») (рис. -@fig:009)

![Курсор в начале](image/9.png){ #fig:009 width=70% }

Переместим курсор в конец строки («Ctrl-e») (рис. -@fig:010)

![Курсор в конце](image/10.png){ #fig:010 width=70% }

Переместим курсор в начало буфера («Alt-<»). (рис. -@fig:011)

![Дописывание](image/11.png){ #fig:011 width=70% }

Переместим курсор в конец буфера («Alt->») (рис. -@fig:012)

![Удаление строки](image/12.png){ #fig:012 width=70% }

Выведем список активных буферов на экран  («Ctrl-x»«Ctrl-b»)  (рис. -@fig:013) 

![Команда отмены](image/13.png){ #fig:013 width=70% }

Переместимся во вновь открытое окно («Ctrl-xo») со списком открытых буферов и переключимся на другой буфер. (рис. -@fig:014) 

![Переключение](image/14.png){ #fig:014 width=70% }

Закроем это окно («Ctrl-x 0») (рис. -@fig:015)

![Закроем окно](image/15.png){ #fig:015 width=70% }

 Теперь вновь переключимся между буферами, но уже без вывода их списка на экран («Ctrl-x b»)(рис. -@fig:016)

![Переключение](image/16.png){ #fig:016 width=70% }

 Поделим фрейм на 4 части: разделим фрейм на два окна по вертикали («Ctrl-x 3»), а затем каждое из этих окон на две части по горизонтали («Ctrl-x 2»)(рис. -@fig:017)

![Разделение](image/17.png){ #fig:017 width=70% }

 В каждом из четырёх созданных окон откроем новый буфер и введем несколько строк текста. Для этого предварительно создадим эти файлы с помощью команд «touchexample1.txt»,«touchexample2.txt», «touchexample3.txt», «touchexample4.txt» (рис. -@fig:018) (рис. -@fig:019) 

![Создание файлов](image/18.png){ #fig:018 width=70% }

![Текст](image/19.png){ #fig:019 width=70% }

Переключимся в режим поиска («Ctrl-s») и найдем несколько слов, присутствующих в тексте (рис. -@fig:020) 

![Режим поиска](image/20.png){ #fig:020 width=70% }

 Переключимся между  результатами  поиска,  нажимая «Ctrl-s» (рис. -@fig:021) 

![Переключение](image/21.png){ #fig:021 width=70% }

 Выйдем из режима поиска, нажав «Ctrl-g» Перейдем в  режим  поиска  и  замены  («Alt-%»),  введем текст, который следует найти и заменить, нажмем «enter», затем введем текст для замены. После того как  будут  подсвечены  результаты  поиска, нажмем «!» для подтверждения замены (рис. -@fig:022) (рис. -@fig:023)

![Замена](image/22.png){ #fig:022 width=70% }

 ![Итог замены](image/23.png){ #fig:023 width=70% }
 
 Пробуем другой режим поиска, нажав «Alt-s o». Данный вид поиска отличается от обычного тем, что тут считывается строкапоиска,  котораятрактуетсякак  регулярное  выражение, ине осуществляется поиск точного совпаденияв тексте буфера.Регулярное выражение−это образец, который обозначает набор строк, возможно, и неограниченный набор.
 
 ![Режим поиска](image/24.png){ #fig:024 width=70% }

# Выводы

В ходе выполнения данной лабораторной работы я познакомилась с операционной системой Linux и получила практические навыки работы с редактором Emacs.

# Контрольные вопросы

1) Emacs − один  из  наиболее  мощных  и  широко  распространённых редакторов,  используемых  в  мире Unix.  По  популярности  он соперничает с редактором vi и его клонами. В зависимости от ситуации, Emacs может быть текстовым редактором;
программой для чтения почты и новостей Usenet;
интегрированной средой разработки (IDE);
операционной системой и т.д.Всё  это  разнообразие  достигается  благодаря  архитектуре Emacs, которая  позволяет  расширять  возможности  редактора  при  помощи языка Emacs  Lisp. На  языке C написаны  лишь  самые  базовые  и низкоуровневые  части Emacs, включая  полнофункциональный.
интерпретатор языка Lisp. Таким образом, Emacs имеет встроенный язык программирования, который может использоваться для настройки, расширения  и  изменения  поведения  редактора.  В  действительности, большая часть того редактора, с которым пользователи Emacs работают в наши дни,написана на языке Lisp.
2)Основную трудность для новичков при освоенииданного редактора могутсоставлять  большое  количество  команд,  комбинаций  клавиш, которые не получится все запомнить с первого раза и поэтоупридется часто обращаться к справочным материалам.
3)Буфер –это  объект,  представляющий  собой  текст. Если  имеется несколько буферов, то редактировать можно только один. Обычно буфер считывает данные из файла или записывает в файл данные из буфера.Окно –это область экрана, отображающая буфер. При запуске редактора отображается одно окно, но при обращении к некоторым функциям могут открыться дополнительные окна. Окна Emacsи окна графической среды XWindow–разные вещи. Одно окно XWindowможет быть разбито  на  несколько  окон  в  смысле Emacs,  в  каждом  из  которых отображается отдельный буфер.
4)Да, можно.
5)При запуске Emacsпо умолчанию создаются следующие буферы:
«scratch»(буфер для несохраненного текста)
«Messages»(журнал ошибок, включающий такжеинформацию, которая появляется в области EchoArea)
«GNUEmacs»(справочный буфер о редакторе)
6)C-c |сначала, удерживая «ctrl»,нажимаю «c»,после –отпускаюобе клавишии нажимаю «|» C-cC-|сначала, удерживая «ctrl»,нажимаю «с», после –отпускаю обе клавиши и, удерживая «ctrl», нажимаю «|»
7)Чтобы  поделить  окно  на  две  части  необходимо  воспользоваться комбинацией «Ctrl-x 3»(по вертикали) или «Ctrl-x 2» (по горизонтали).
8)Настройки Emacsхранятся в файле .emacs.
9)По  умолчанию  клавиша «←» удаляет  символперед  курсором, нов редакторе  её  можно  переназначить.  Для  этого  необхдимоизменить конфигурацию файла .emacs.
10)Более удобным я считаю редактор emacs, потому чтов нем проще открывать другие файлы, можно использовать сразу несколько окон, нет «Командногорежима», «Режима ввода», «Режима командной строки», которые  являются  немного  непривычными  и  в  какой-то  степени неудобным.



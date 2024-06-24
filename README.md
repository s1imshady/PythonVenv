# Виртуальные среды в Python  
В этом уроке вы научитесь работать с Python vevb модуль создавать и управлять отдельными виртуальные среды для ваших проектов Python. Каждая среда может использовать разные версии зависимостей пакетов и Python. Научившись работать с виртуальными средами, вы будете знать, как помочь другим программистам воспроизвести ваши настройки разработки, и убедитесь, что ваши проекты никогда не вызывают конфликтов зависимостей друг для друга.

К концу этого урока вы будете знать, как:
- Создавать и активировать виртуальную среду Python
- Объяснять, почему вы хотите изолировать внешние зависимости
- Визуализировать, что делает Python, когда вы создаете виртуальную среду
- Настроить ваши виртуальные среды, используя дополнительные аргументы для venv
- Деактивировать и удалять виртуальные среды
- Выбирать дополнительные инструменты для управления версиями Python и виртуальными средами
Виртуальные среды — распространенный и эффективный метод, используемый при разработке Python. Лучшее понимание того, как они работают, зачем они вам нужны и что вы можете с ними делать, поможет вам освоить рабочий процесс программирования на Python.
## Как вы можете работать с виртуальной средой Python?
Если вам просто нужно запустить виртуальную среду Python, чтобы продолжить работу над любимым проектом, то этот раздел — подходящее место для вас.
В инструкциях этого руководства используетсяPython venv модуль для создания виртуальных сред. Этот модуль является частью стандартной библиотеки Python и официально рекомендуется для создания виртуальных сред, начиная с Python 3.5.  
*Примечание: Существуют и другие замечательные сторонние инструменты для создания виртуальных сред, такие какКондаивиртуальное окружение, о котором вы сможете узнать подробнее позже в этом уроке. Любой из этих инструментов может помочь вам настроить виртуальную среду Python.*  
Для базового использования,venv— отличный выбор, поскольку он уже включен в вашу установку Python. Имея это в виду, вы готовы создать свою первую виртуальную среду в этом руководстве.
### Создать виртуальную среду
Каждый раз, когда вы работаете над проектом Python, в котором используются внешние зависимости, лучше всего сначала создать виртуальную среду:  
```
Windows PowerShell
PS>python -m venv venv
```
Если вы используете Python в Windowsи  вы не настроили переменные среды, то вам может потребоваться указать полный путь к исполняемому файлу Python:  
```
Windows PowerShell 
PS>C:\Users\Name\AppData\Local\Programs\Python\Python310\python -m venv venv
```
Указанный выше системный путь предполагает, что вы установили Python 3.10 с помощью установщика Windows. Путь к исполняемому файлу Python в вашей системе может быть другим.
### Активировать виртуальную среду
Теперь у вашего проекта есть собственная виртуальная среда. Как правило, прежде чем начать его использовать, вы сначала активируете среду, выполнив сценарий, который поставляется вместе с установкой:  
```
PS>venv\scripts\acrivate
(venv) PS>
```
Прежде чем запускать эту команду, убедитесь, что вы находитесь в папке, содержащей только что созданную виртуальную среду.
*Примечание: Вы также можете работать со своей виртуальной средой, не активируя ее. Для этого укажите полный путь своему интерпретатору Python при выполнении команды. Однако чаще всего вам потребуется активировать виртуальную среду после ее создания, чтобы избавить себя от необходимости неоднократно вводить длинные пути.*
Как только вы увидите имя вашей виртуальной среды — в данном случае(venv)— в командной строке, тогда вы знаете, что ваша виртуальная среда активна. Все готово и готово к установке внешних пакетов!
### Установите пакеты
После создания и активации виртуальной среды вы можете установить любые внешние зависимости, необходимые для вашего проекта:
Эта команда является командой по умолчанию, которую следует использовать для установки внешних пакетов Python с помощьюпункт. Поскольку вы сначала создали и активировали виртуальную среду,пунктустановит пакеты в изолированное место.  
*Примечание: Поскольку вы создали свою виртуальную среду с использованием версии Python 3, вам не нужно вызывать python3 или pip3 явно.*
Поздравляем, теперь вы можете установить пакеты в свою виртуальную среду. Чтобы добраться до этого момента, вы начали с создания виртуальной среды Python с именемvenvа затем активировал его в текущем сеансе оболочки.  
Пока вы не закроете свой терминал, каждый Пакет Python который вы установите, окажется в этой изолированной среде вместо ваших глобальных site-packages Python. Это означает, что теперь вы можете работать над своим проектом Python, не беспокоясь о конфликтах зависимостей.
### Деактивировать среду
Закончив работу с этой виртуальной средой, вы можете деактивировать ее:  
```
Windows PowerShell
(venv) PS>deactivate
PS>
```
После выполнения  ваша командная строка вернется в нормальное состояние. Это изменение означает, что вы вышли из виртуальной среды. Если вы взаимодействуете с Python, теперь вы будете взаимодействовать с вашей глобально настроенной средой Python.
Если вы хотите вернуться в виртуальную среду, которую вы создали ранее, вам снова необходимо запустить скрипт активации этой виртуальной среды.  
*Примечание: Перед установкой пакета найдите имя вашей виртуальной среды в круглых скобках перед командной строкой..
Если имя отображается, значит, вы знаете, что ваша виртуальная среда активна, и вы можете установить внешние зависимости. Если вы не видите имя в командной строке, не забудьте активировать виртуальную среду Python перед установкой каких-либо пакетов.*   
На этом этапе вы рассмотрели основы работы с виртуальными средами Python. Если это все, что вам нужно, то счастливого пути к продолжению творчества!
Однако, если вы хотите знать, что именно только что произошло, почему во многих руководствах вас вообще просят создать виртуальную среду и что на самом деле представляет собой виртуальная среда Python, продолжайте читать!
## Зачем вам нужны виртуальные среды?
Почти все в сообществе Python предлагают использовать виртуальные среды для всех своих проектов. Но почему? Если вы хотите узнать, почему вам вообще необходимо настраивать виртуальную среду Python, то этот раздел для вас.
Короткий ответ: Python не очень хорош в управлении зависимостями. Если не конкретизировать, то pip поместит все внешние пакеты, которые вы устанавливаете, в папку в вашей базовой установке Python.
Если все ваши внешние пакеты находятся в одной папке, может возникнуть несколько проблем. В этом разделе вы узнаете больше о них, а также о других проблемах, которые решаются виртуальными средами.
### Избегайте загрязнения системы
Linux и macOS поставляются с предустановленной версией Python, которую операционная система использует для внутренних задач.
Если вы устанавливаете пакеты в глобальный Python вашей операционной системы, эти пакеты будут смешиваться с пакетами, соответствующими системе. Эта путаница может иметь неожиданные побочные эффекты для задач, имеющих решающее значение для нормального поведения вашей операционной системы.
Кроме того, если вы обновите свою операционную систему, установленные вами пакеты могут быть перезаписаны и потеряны. Вы не хотите, чтобы случилась любая из этих головных болей!
### Обход конфликтов зависимостей
Для одного из ваших проектов может потребоваться другая версия внешней библиотеки, чем другая. Если у вас есть только одно место для установки пакетов, то вы не сможете работать с двумя разными версиями одной и той же библиотеки. Это одна из наиболее распространенных причин, по которым рекомендуется использовать виртуальную среду Python.
Чтобы лучше понять, почему это так важно, представьте, что вы строите Веб-сайты Django  для двух разных клиентов. Одному клиенту нравится существующее веб-приложение, которое вы изначально создали с помощью Dlango 2.2.26, и этот клиент отказывается обновлять свой проект до современной версии Django. Другой клиент хочет, чтобы вы включили на его веб-сайт функциональность асинхронности, которая доступна только начиная с Django 4.0.
Если вы установили Django глобально, у вас может быть установлена только одна из двух версий:
```
PS> python -m pip install django==2.2.26
PS> python -m pip list
Package    Version
---------- -------
Django     2.2.26
pip        22.0.4
pytz       2022.1
setuptools 58.1.0
sqlparse   0.4.2

PS> python -m pip install django==4.0.3
PS> python -m pip list
Package    Version
---------- -------
asgiref    3.5.0
Django     4.0.3
pip        22.0.4
pytz       2022.1
setuptools 58.1.0
sqlparse   0.4.2
tzdata     2022.1
```
Если вы устанавливаете две разные версии одного и того же пакета в глобальную среду Python, вторая установка перезапишет первую. По той же причине не получится создать единую виртуальную среду для обоих клиентов. Вы не можете иметь две разные версии одного и того же пакета в одной среде Python.
Похоже, с такой настройкой вы не сможете работать над одним из двух проектов! Однако если вы создадите виртуальную среду для каждого проекта ваших клиентов, вы сможете установить в каждый из них разные версии Django:
```
PS> mkdir client-old
PS> cd client-old
PS> python -m venv venv --prompt="client-old"
PS> venv\Scripts\activate
(client-old) PS> python -m pip install django==2.2.26
(client-old) PS> python -m pip list
Package    Version
---------- -------
Django     2.2.26
pip        22.0.4
pytz       2022.1
setuptools 58.1.0
sqlparse   0.4.2
(client-old) PS> deactivate

PS> cd ..
PS> mkdir client-new
PS> cd client-new
PS> python -m venv venv --prompt="client-new"
PS> venv\Scripts\activate
(client-new) PS> python -m pip install django==4.0.3
(client-new) PS> python -m pip list
Package    Version
---------- -------
asgiref    3.5.0
Django     4.0.3
pip        22.0.4
setuptools 58.1.0
sqlparse   0.4.2
tzdata     2022.1
(client-new) PS> deactivate
```
Если вы сейчас активируете любую из двух виртуальных сред, вы заметите, что она по-прежнему содержит свою собственную версию Django. Эти две среды также имеют разные зависимости, и каждая содержит только те зависимости, которые необходимы для этой версии Django.
С помощью этой настройки вы можете активировать одну среду, когда работаете над одним проектом, и другую, когда работаете над другим. Теперь вы можете одновременно радовать любое количество клиентов!
### Минимизация проблем с воспроизводимостью
Если вы какое-то время работали с Python, то ваша глобальная среда Python уже может включать в себя всевозможные сторонние пакеты. Если это не так, то похлопайте себя по плечу! Вероятно, вы недавно установили новую версию Python или уже знаете, как работать с виртуальными средами.
Чтобы прояснить, с какими проблемами воспроизводимости вы можете столкнуться при совместном использовании среды Python в нескольких проектах, мы рассмотрим следующий пример ситуации. Представьте, что за последний месяц вы работали над двумя независимыми проектами:
1.	Проект парсинга веб-страниц с помощью Beautiful Soup
2.	Приложение Flask
Не зная о виртуальных средах, вы установили все необходимые пакеты в свою глобальную среду Python:
```
Windows PowerShell
PS> python -m pip install beautifulsoup4 requests
PS> python -m pip install flask
```
Ваше приложение Flask оказалось весьма полезным, поэтому другие разработчики тоже хотят над ним поработать. Им необходимо воспроизвести среду, которую вы использовали для работы над ним. Вы хотите идти вперед изакрепите свои зависимости, чтобы вы могли поделиться своим проектом в Интернете:
```
Windows PowerShell
PS> python -m pip freeze
beautifulsoup4==4.10.0
certifi==2021.10.8
charset-normalizer==2.0.12
click==8.0.4
colorama==0.4.4
Flask==2.0.3
idna==3.3
itsdangerous==2.1.1
Jinja2==3.0.3
MarkupSafe==2.1.1
requests==2.27.1
soupsieve==2.3.1
urllib3==1.26.9
Werkzeug==2.0.3
```
Какие из этих пакетов актуальны для вашего приложения Flask, а какие находятся здесь из-за вашего проекта по очистке веб-страниц? Трудно сказать, когда все внешние зависимости находятся в одном месте.
В такой единой среде вам придется вручную просматривать зависимости и знать, какие из них необходимы для вашего проекта, а какие нет. В лучшем случае этот подход утомителен, но, скорее всего, он подвержен ошибкам.
Если вы используете отдельную виртуальную среду для каждого из своих проектов, вам будет проще прочитать требования проекта из закрепленных зависимостей. Это означает, что вы можете поделиться своим успехом, разработав отличное приложение, позволяя другим сотрудничать с вами!
### Блокировка привилегий установки Dodge
Наконец, вам могут потребоваться права администратора на компьютере для установки пакетов в каталог site-packages хоста Python. В корпоративной рабочей среде у вас, скорее всего, не будет такого уровня доступа к машине, на которой вы работаете.
Если вы используете виртуальные среды, вы создаете новое место установки в рамках ваших пользовательских привилегий, что позволяет вам устанавливать внешние пакеты и работать с ними.
Независимо от того, занимаетесь ли вы программированием в качестве хобби на своем компьютере, разрабатываете веб-сайты для клиентов или работаете в корпоративной среде, использование виртуальной среды в долгосрочной перспективе избавит вас от многих неприятностей.
## Что такое виртуальная среда Python?
На этом этапе вы убеждены, что хотите работать с виртуальными средами. Отлично, но с чем вы работаете, когда используете виртуальную среду? Если вы хотите понять, что такое виртуальные среды Python, то этот раздел для вас.
Короткий ответ: виртуальная среда Python — это структура папок, которая дает вам все необходимое для запуска облегченной, но изолированной среды Python.
### Структура папок
Когда вы создаете новую виртуальную среду с помощью venv, Python создает автономную структуру папок и копирует символические ссылки python.
Вам не нужно глубоко копаться в этой структуре папок, чтобы узнать больше о том, из чего состоят виртуальные среды. Совсем скоро вы аккуратно соскоблите верхний слой почвы и исследуете обнаруженные вами высокоуровневые структуры.
Папка виртуальной среды содержит множество файлов и папок, но вы можете заметить, что большая часть того, что делает эту древовидную структуру такой долгой, находится внутри нее. Если вы сократите находящиеся там подпапки и файлы, вы получите не слишком громоздкую древовидную структуру:
```
venv\
│
├── Include\
│
├── Lib\
│   │
│   └── site-packages\
│       │
│       ├── _distutils_hack\
│       │
│       ├── pip\
│       │
│       ├── pip-22.0.4.dist-info\
│       │
│       ├── pkg_resources\
│       │
│       ├── setuptools\
│       │
│       ├── setuptools-58.1.0.dist-info\
│       │
│       └── distutils-precedence.pth
│
│
├── Scripts\
│   ├── Activate.ps1
│   ├── activate
│   ├── activate.bat
│   ├── deactivate.bat
│   ├── pip.exe
│   ├── pip3.10.exe
│   ├── pip3.exe
│   ├── python.exe
│   └── pythonw.exe
│
└── pyvenv.cfg
```
Эта уменьшенная древовидная структура дает вам лучшее представление о том, что происходит в папке вашей виртуальной среды:
```
Windows
-	Include\ изначально пустая папка, которую Python использует длявключить заголовочные файлы Cдля пакетов, которые вы можете установить и которые зависят от расширений C.
-	lib\site-packages\ является одной из основных причин создания виртуальной среды. В этой папке вы будете устанавливать внешние пакеты, которые хотите использовать в своей виртуальной среде. По умолчанию в вашей виртуальной среде предустановлены две зависимости:пункти инструменты настройки. Вы узнаете о них больше немного позже.
-	scripts\содержит исполняемые файлы вашей виртуальной среды. Наиболее примечательными являются интерпретатор Python (python.exe),пунктисполняемый файл (пип.exe) и сценарий активации для вашей виртуальной среды, который доступен в нескольких вариантах, позволяющих работать с разными оболочками. В этом уроке вы использовалиактивировать, который управляет активацией вашей виртуальной среды для Windows в большинстве оболочек.
-	pyvenv.cfg— это важный файл для вашей виртуальной среды. Он содержит всего пару пар ключ-значение, которые Python использует для установки переменных всистемамодуль, который определяет, какой интерпретатор Python и какой каталог site-packages будет использовать текущий сеанс Python. Вы узнаете больше о настройках этого файла, когда прочтете о том, как работает виртуальная среда.
Из этого обзора содержимого папки вашей виртуальной среды с высоты птичьего полета вы можете еще больше уменьшить масштаб и обнаружить, что существует три основные части виртуальной среды Python:
```
1.	Копия или символическая ссылка двоичного файла Python.
2.	Аpyvenv.cfgфайл
3.	Каталог site-packages
Установленные пакеты внутри site-packages/являются необязательными, но используются по умолчанию. Однако ваша виртуальная среда все равно была бы действительной виртуальной средой, если бы этот каталог был пустым, и есть способы ее создать без установки каких-либо зависимостей.
Вы можете дважды проверить, что Python установил pip и setuptools в вашу виртуальную среду с помощью pip list:
```
Windows PowerShell
(venv) PS> python -m pip list
Package    Version
---------- -------
pip        22.0.4
setuptools 58.1.0
---------- -------
```
Номера ваших версий могут отличаться, но эти выходные данные подтверждают, что Python установил оба пакета, когда вы создавали виртуальную среду с настройками по умолчанию.  
*Примечание:Ниже этого вывода pip также может отображаться предупреждение о том, что вы используете не последнюю версию модуля. Пока не беспокойтесь об этом. Позже вы узнаете больше о том, почему это происходит и как с этим бороться.*  
Эти два установленных пакета составляют большую часть содержимого вашей новой виртуальной среды. Однако вы заметите, что в папке есть еще несколько папок:
•	The_distutils_hack/module,в соответствии со своим названием, гарантирует, что при установке пакета Python выберет локальный.
•	Thepkg_resources/module помогает приложениям автоматически обнаруживать плагины и позволяет пакетам Python получать доступ к своим файлам ресурсов.
•The {name}-{version}.dist-info/ папки для pip, setuptools содержат  package distribution информацию, которая существует для записывания информации об установленных пакетах.
Наконец, есть также файл с именем distutils-precedence.pth. Этот файл помогает установить приоритет пути для distutils imports и работает вместе с_distutils_hack.  
*Примечание: Вы узнаете об этих дополнительных файлах и папках для полноты картины. Вам не нужно будет их запоминать, чтобы эффективно работать с виртуальными средами. Достаточно иметь в виду, что любые предустановленные пакеты в вашем site-packages/ являются стандартными инструментами, которые делают установку других пакетов более удобной для пользователя.*  
К этому моменту вы увидели все файлы и папки, составляющие виртуальную среду Python, если вы установили ее с помощью встроенного venv.
Имейте в виду, что ваша виртуальная среда представляет собой просто структуру папок, а это означает, что вы можете удалить и создать заново в любое время, когда захотите. Но почему именно такая структура папок и что она делает возможной?
### Изолированная установка Python
Виртуальные среды Python призваны предоставить легкую, изолированную среду Python, которую вы можете быстро создать, а затем отказаться от нее, когда она вам больше не нужна. Структура папок, которую вы видели выше, делает это возможным, предоставляя три ключевых элемента:
1. Копия или символическая ссылка двоичного файла Python
2. Аpyvenv.cfgфайл
3. Каталог site-packages  
Эта структура определяет расположение копии или символической ссылки двоичного файла Python и каталога site-packages, куда Python устанавливает внешние пакеты.  
*Примечание:Является ли исполняемый файл Python в вашей виртуальной среде копией или символической ссылкой исполняемого файла Python, на котором вы создали среду, зависит в первую очередь от вашей операционной системы.*  
Windows и Linux могут создавать символические ссылки вместо копий, тогда как macOS всегда создает копию. Вы можете попробовать влиять на поведение по умолчанию с необязательными аргументами при создании виртуальной среды. Однако в большинстве стандартных случаев вам не придется об этом беспокоиться.
В дополнение к двоичному файлу Python и каталогу site-packages вы получаете pyvenv.cfg файл. Это небольшой файл, содержащий всего пару пар ключ-значение. Однако эти настройки имеют решающее значение для работы вашей виртуальной среды:
```
Конфигурационный файл
home = C:\Users\Name\AppData\Local\Programs\Python\Python310
include-system-site-packages = false
version = 3.10.3
```
Вы узнаете больше об этом файле в следующем разделе, когда будете читать об этом файле.
Предположим, вы внимательно исследуете свою недавно созданную виртуальную среду. В этом случае вы можете заметить, что эта облегченная установка не содержит ни одной доверенной стандартной библиотеки. Кто-то может сказать, что Python без стандартной библиотеки подобен игрушечной машинке без батареек!
Однако если вы запустите интерпретатор Python из своей виртуальной среды, вы все равно сможете получить доступ ко всем возможностям стандартной библиотеки:
```
Python
>>> import urllib
>>> from pprint import pp
>>> pp(dir(urllib))
['__builtins__',
 '__cached__',
 '__doc__',
 '__file__',
 '__loader__',
 '__name__',
 '__package__',
 '__path__',
 '__spec__']
```
В приведенном выше фрагменте кода вы успешно импортируете оба модуля urllib() и pp(). Затем вы используете dir() чтобы осмотреть URLlib модуль.
Оба модуля являются частью стандартной библиотеки, так как же у вас есть доступ к ним, даже если они не находятся в структуре папок вашей виртуальной среды Python?
Вы можете получить доступ к модулям стандартной библиотеки Python, поскольку ваша виртуальная среда повторно использует встроенные модули Python и модули стандартной библиотеки из установки Python, из которой вы создали свою виртуальную среду. В следующем разделе вы узнаете, как виртуальная среда обеспечиваетссылка на стандартную библиотеку вашего базового Python.  
*Примечание:Поскольку для создания виртуальной среды вам всегда нужна существующая установка Python,venv предпочитает повторно использовать существующие модули стандартной библиотеки, чтобы избежать накладных расходов на их копирование в новую виртуальную среду. Это намеренное решение ускоряет создание виртуальных сред и делает их более легкими.*  
Помимо стандартных модулей библиотеки, вы можете опционально предоставить вашей виртуальной среде доступ к site-packages базовой установки через аргумент при создании среды:
```
Windows PowerShell
PS C:\> python -m venv venv --system-site-packages
```
## Как работает виртуальная среда?
Если вы знаете, что такое виртуальная среда Python, но хотите создать облегченную изоляцию, которую она обеспечивает, то вы попали в правильный раздел. 
### Он копирует структуру и файлы
Когда вы создаете виртуальную среду с помощью venv, модуль заново создает файл и структуру папок установки Python в вашей операционной системе. Python также копирует или символизирует в эту структуру папок исполняемый файл Python, с помощью которого вы вызвали venv:
```
venv\
│
├── Include\
│
├── Lib\
│   │
│   └── site-packages\
│
├── Scripts\
│   ├── Activate.ps1
│   ├── activate
│   ├── activate.bat
│   ├── deactivate.bat
│   ├── pip.exe
│   ├── pip3.10.exe
│   ├── pip3.exe
│   ├── python.exe
│   └── pythonw.exe
│
└── pyvenv.cfg
```
Если вы найдете общесистемную установку Python в своей операционной системе и проверите структуру папок там, вы увидите, что ваша виртуальная среда похожа на эту структуру.  
*Примечание:В Windows вы можете заметить, что python.exe в вашей базовой установке Python нет scripts\ но он находится на один уровень выше. В вашей виртуальной среде исполняемый файл намеренно расположен в папке scripts\folder.*    
Это небольшое изменение в структуре папок означает, что вам нужно добавить в оболочку только один каталог.
Хотя в вашей базовой установке Python вы можете найти некоторые дополнительные файлы и папки, вы заметите, что стандартная структура папок такая же, как и в вашей виртуальной среде. venv создает эту структуру папок, чтобы гарантировать, что Python будет работать должным образом изолированно, без необходимости внесения множества дополнительных изменений.
### Он адаптирует процесс поиска префикса
При наличии стандартной структуры папок интерпретатор Python в вашей виртуальной среде может понять, где находятся все нужные файлы. Он делает это лишь с небольшими изменениями в своем процессе поиска префиксов в соответствии со спецификацией venv.
Вместо того чтобы искать модуль os для определения местоположения стандартной библиотеки, интерпретатор Python сначала ищет файл pyvenv.cfg. Если интерпретатор находит этот файл и в нем содержится ключ home, то интерпретатор использует этот ключ для установки значения двух переменных:
1. sys.base_prefix будет содержать путь к исполняемому файлу Python, используемому для создания этой виртуальной среды, который можно найти по пути, заданному ключом home в файле pyvenv.cfg.
2. sys.prefix будет указывать на каталог, содержащий pyvenv.cfg.
Если интерпретатор не находит файл pyvenv.cfg, то он определяет, что работает не в виртуальной среде, и тогда и sys.base_prefix, и sys.prefix будут указывать на один и тот же путь.
### Он ссылается на вашу стандартную библиотеку.
Виртуальные среды Python - это легкий способ предоставить вам изолированную среду Python, которую вы можете быстро создать, а затем удалить, когда она вам больше не нужна. Чтобы сделать это возможным, venv копирует только минимально необходимые файлы.
Исполняемый файл Python в вашей виртуальной среде имеет доступ к стандартным библиотечным модулям той установки Python, на которой основана среда. Python делает это возможным, указывая путь к файлу базового исполняемого файла Python в настройке home в файле pyvenv.cfg:
```
Windows
home = C:\Users\Name\AppData\Local\Programs\Python\Python310
include-system-site-packages = false
версия = 3.10.3
```
Если вы перейдете по пути, указанному в выделенной строке в файле pyvenv.cfg, и просмотрите содержимое папки, то найдете базовый исполняемый файл Python, который вы использовали для создания виртуальной среды. Оттуда можно перейти к папке, содержащей модули стандартной библиотеки:
```
Windows Powershell
PS> ls C:\Users\Name\AppData\Local\Programs\Python\Python310

 Directory: C:\Users\Name\AppData\Local\Programs\Python\Python310

Mode              LastWriteTime      Length Name
----              -------------      ------ ----
d-----     12/19/2021   5:09 PM             DLLs
d-----     12/19/2021   5:09 PM             Doc
d-----     12/19/2021   5:09 PM             include
d-----     12/19/2021   5:09 PM             Lib
d-----     12/19/2021   5:09 PM             libs
d-----     12/21/2021   2:04 PM             Scripts
d-----     12/19/2021   5:09 PM             tcl
d-----     12/19/2021   5:09 PM             Tools
-a----      12/7/2021   4:28 AM       32762 LICENSE.txt
-a----      12/7/2021   4:29 AM     1225432 NEWS.txt
-a----      12/7/2021   4:28 AM       98544 python.exe
-a----      12/7/2021   4:28 AM       61680 python3.dll
-a----      12/7/2021   4:28 AM     4471024 python310.dll
-a----      12/7/2021   4:28 AM       97008 pythonw.exe
-a----      12/7/2021   4:29 AM       97168 vcruntime140.dll
-a----      12/7/2021   4:29 AM       37240 vcruntime140_1.dll

PS> ls C:\Users\Name\AppData\Local\Programs\Python\Python310\Lib

 Directory: C:\Users\Name\AppData\Local\Programs\Python\Python310\Lib

Mode              LastWriteTime      Length Name
----              -------------      ------ ----
d-----     12/19/2021   5:09 PM             asyncio
d-----     12/19/2021   5:09 PM             collections

# ...

-a----      12/7/2021   4:27 AM        5302 __future__.py
-a----      12/7/2021   4:27 AM          65 __phello__.foo.py
```
Python настроен на поиск этих модулей путем добавления соответствующего пути в sys.path. При инициализации Python автоматически импортирует site модуль, который устанавливает значения по умолчанию для этого аргумента.
Пути, к которым ваша сессия Python имеет доступ в sys.path, определяют, из каких мест Python может импортировать модули.
Если вы активируете виртуальную среду и войдете в интерпретатор Python, то сможете убедиться, что путь к папке стандартной библиотеки вашей базовой установки Python доступен:
```
Python
>>> import sys
>>> from pprint import pp
>>> pp(sys.path)
['',
 'C:\\Users\\Name\\AppData\\Local\\Programs\\Python\\Python310\\python310.zip',
 'C:\\Users\\Name\\AppData\\Local\\Programs\\Python\\Python310\\DLLs',
 'C:\\Users\\Name\\AppData\\Local\\Programs\\Python\\Python310\\lib',
 'C:\\Users\\Name\\AppData\\Local\\Programs\\Python\\Python310',
 'C:\\Users\\Name\\path\\to\\venv',
 'C:\\Users\\Name\\path\\to\\venv\\lib\\site-packages']
```
Поскольку путь к каталогу, содержащему модули стандартной библиотеки, доступен в sys.path, вы сможете импортировать любой из них при работе с Python из виртуальной среды.
### Он изменяет ваш PYTHONPATH
Чтобы убедиться, что скрипты, которые вы хотите запустить, используют интерпретатор Python в вашем виртуальном окружении, venv изменяет переменную окружения PYTHONPATH, доступ к которой вы можете получить с помощью sys.path.
Если вы посмотрите на эту переменную без активной виртуальной среды, вы увидите пути по умолчанию для вашей стандартной установки Python:
```
Python
>>> import sys
>>> from pprint import pp
>>> pp(sys.path)
['',
 'C:\\Users\\Name\\AppData\\Local\\Programs\\Python\\Python310\\python310.zip',
 'C:\\Users\\Name\\AppData\\Local\\Programs\\Python\\Python310\\DLLs',
 'C:\\Users\\Name\\AppData\\Local\\Programs\\Python\\Python310\\lib',
 'C:\\Users\\Name\\AppData\\Local\\Programs\\Python\\Python310',
 'C:\\Users\\Name\\AppData\\Roaming\\Python\\Python310\\site-packages',
 'C:\\Users\\Name\\AppData\\Local\\Programs\\Python\\Python310\\lib\\site-packages']
```
Однако если вы активируете виртуальную среду перед запуском другого сеанса интерпретатора и повторно выполните те же команды, то получите другой результат:
```
Python
>>> import sys
>>> from pprint import pp
>>> pp(sys.path)
['',
 'C:\\Users\\Name\\AppData\\Local\\Programs\\Python\\Python310\\python310.zip',
 'C:\\Users\\Name\\AppData\\Local\\Programs\\Python\\Python310\\DLLs',
 'C:\\Users\\Name\\AppData\\Local\\Programs\\Python\\Python310\\lib',
 'C:\\Users\\Name\\AppData\\Local\\Programs\\Python\\Python310',
 'C:\\Users\\Name\\path\\to\\venv',
 'C:\\Users\\Name\\path\\to\\venv\\lib\\site-packages']
```
Python заменил стандартный путь к каталогу site-packages на тот, который находится в вашей виртуальной среде. Это изменение означает, что Python будет загружать любые внешние пакеты, установленные в вашей виртуальной среде. И наоборот, поскольку путь к директории site-packages вашего базового Python больше не находится в этом списке, Python не будет загружать оттуда модули.
Это изменение в настройках пути Python эффективно создает изоляцию внешних пакетов в вашей виртуальной среде.
В качестве опции вы можете получить доступ только для чтения к системному каталогу site-packages вашей базовой установки Python, передав соответствующий аргумент при создании виртуальной среды.
### Изменяет переменную Shell PATH при активации
Для удобства вы обычно активируете виртуальную среду перед работой в ней, хотя это и не обязательно.
Чтобы активировать виртуальную среду, необходимо выполнить скрипт активации:
```
Windows Powershell
PS> venv\Scripts\activate
(venv) PS>
```
Выбор сценария активации зависит от вашей операционной системы и используемой оболочки.
Если вы покопаетесь в структуре папок вашей виртуальной среды, то найдете несколько различных сценариев активации, которые поставляются вместе с ней:
```
Windows
venv\
│
├── Include\
│
├── Lib\
│
├── Scripts\
│   ├── Activate.ps1
│   ├── activate
│   ├── activate.bat
│   ├── deactivate.bat
│   ├── pip.exe
│   ├── pip3.10.exe
│   ├── pip3.exe
│   ├── python.exe
│   └── pythonw.exe
│
└── pyvenv.cfg
```
Все эти сценарии активации имеют одну и ту же цель. Однако они должны предоставлять различные способы достижения этой цели из-за различных операционных систем и оболочек, с которыми работают пользователи.
В сценарии активации происходят два критических действия:
1. Path: Он устанавливает переменную VIRTUAL_ENV в путь к корневой папке вашей виртуальной среды и добавляет относительное расположение исполняемого файла Python в PATH.
2. Командная строка: Изменяет командную строку на имя, которое вы передали при создании виртуальной среды. Оно берет это имя и заключает его в круглые скобки, например (venv).
Эти изменения обеспечивают удобство работы с виртуальными средами в вашей оболочке:
- Путь: Поскольку путь ко всем исполняемым файлам в вашей виртуальной среде теперь находится в начале PATH, ваша оболочка будет вызывать внутренние версии pip или Python, когда вы просто набираете pip или python.
- Командная строка: Поскольку сценарий изменил командную строку, вы быстро узнаете, активирована ли ваша виртуальная среда.
Оба эти изменения являются незначительными адаптациями, которые существуют исключительно для вашего удобства. Они не являются строго необходимыми, но делают работу с виртуальными средами Python более приятной.
Вы можете проверить переменную PATH до и после активации виртуальной среды. Если вы активировали виртуальную среду, то в начале PATH вы увидите путь к папке, содержащей ваши внутренние исполняемые файлы:
```
PS> $Env:Path
C:\Users\Name\path\to\venv\Scripts;C:\Windows\system32;C:\Windows;C:\Windows\System32\Wbem;C:\Users\Name\AppData\Local\Programs\Python\Python310\Scripts\;C:\Users\Name\AppData\Local\Programs\Python\Python310\;c:\users\name\.local\bin;c:\users\name\appdata\roaming\python\python310\scripts
```
Имейте в виду, что результат печати переменной PATH, скорее всего, будет выглядеть совсем иначе. Важно то, что сценарий активации добавил путь к вашей виртуальной среде в начало переменной PATH.
Когда вы деактивируете виртуальное окружение с помощью команды deactivate, ваша оболочка отменяет эти изменения и возвращает PATH и командную строку в прежнее состояние.
Запускается из любого места с абсолютными путями
Чтобы использовать виртуальную среду, ее не нужно активировать. Вы можете работать с виртуальной средой без ее активации, хотя ее активация - это обычное действие, которое часто рекомендуется.
Если вы укажете оболочке только имя исполняемого файла, она будет искать исполняемый файл с таким именем в PATH. Затем он выберет и запустит первый, который соответствует этому критерию.
Сценарий активации изменяет переменную PATH таким образом, чтобы папка binaries вашего виртуального окружения была первым местом, где ваша оболочка ищет исполняемые файлы. Это изменение позволит вам набирать только pip или python для запуска соответствующих программ, расположенных в вашем виртуальном окружении.
Если вы не активировали виртуальное окружение, то для запуска любого скрипта из виртуального окружения вы можете указать абсолютный путь к исполняемому файлу Python внутри виртуального окружения:
```
PS> C:\Users\Name\path\to\venv\Scripts\python.exe
```
Эта команда запустит интерпретатор Python в вашей виртуальной среде точно так же, как если бы вы сначала активировали виртуальную среду, а затем вызвали ее с помощью python.
Встраивание активации виртуальной среды в скрипт - суетливое занятие, которое чаще идет не так, чем не так. Вместо этого, вооружившись знаниями, полученными в этом уроке, вы можете использовать абсолютный путь к интерпретатору Python в вашей виртуальной среде при запуске сценария.
Это можно использовать, например, если вы настраиваете почасовое задание CRON на удаленном Linux-сервере, которое асинхронно проверяет подключение к сайту с помощью внешнего пакета aiohttp, установленного в виртуальной среде:
```
0 * * * *
    /home/name/Documents/connectivity-checker/venv/bin/python
    -m rpchecker
    -u google.com twitter.com
    -a
```
Вам не нужно возиться с активацией виртуальной среды, чтобы использовать нужный интерпретатор Python, имеющий доступ к зависимостям, которые вы установили в виртуальной среде. Вместо этого вы просто передаете абсолютный путь к двоичному файлу этого интерпретатора. Python позаботится обо всем остальном во время инициализации.
Пока вы указываете путь к исполняемому файлу Python, вам не нужно активировать виртуальную среду, чтобы воспользоваться преимуществами ее использования.

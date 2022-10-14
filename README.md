﻿# university and training projects
репозиторий содержит несколько каталогов, представляющие собой различные проекты:
- тренировочные
- университетские


## training_projects (2021+)
проекты, создаваемые либо в качестве фриланса, либо как тестовые задания для приема на работу, либо как просто интересные для выполнения маленькие задачи

### data_sampling_with_plotting (2022)
обработка данных для последующего создания графиков. подробности в файле **tz.docx**

### template_engine (2020)
программа для формирования заявлений по шаблону word. данные для шаблона берутся из таблицы excel. сформированные заявления сохраняются в заранее созданный пустой каталог. представленный и многие другие шаблоны использовались в реальной работе, сократив время выполнения задач сотрудникам компании на тысячи человеко-часов. естественно, все ФИО и названия изменены

в каталоге сама программа **template_engine_mes.py**, шаблон для заявлений **mes_template.docx**, кусок таблицы **mes.xlsx** и пустой каталог **res_mes**

### dungeon_rpg (2022)
простая текстовая rpg, подробности в файле **tz.txt**


## university_projects (2019-2022)
проекты, выполненные в ходе обучение в университете. на момент написания учился по Introducing Python: Modern Computing in Simple Packages B. Lubanovic. рекомендации PEP8 на тот момент не соблюдал

### little_projects (2019)
  маленькие и простенькие проекты, не требующие дополнительных модулей или файлов:
  
  - **krivaya_koha.py** - по введёным параметрам (включая глубину) рисуется и сохраняется в формат png Кривая Коха
  - **elevator.py** - модель работы лифта

### parser (2020)
  программа для парсинга конкретного файла логов (изначальный размер - 450+ мб, здесь выложен его кусок на 100 строк). по итогу проверки файла, формируется отчёт в excel. примерное время выполнения с изначальным размером - 10 минут 

в каталоге сам **parser.py** и **request.log**

### IDS (models) (2021)
в этом каталоге находятся три программы, имитирующие работу системы обнаружения вторжений. первые две программы выполняют аналогичные функции разными способами. речь о **generator.py** и **generator-new.py**

**generator.py** формирует логи, имитирующие логи реального веб-сервера, то есть, записываются посещения страничек сайта пользователей, включая нарушителей, использующих DOS-атаку или SQLi. у программы есть существенный минус - пользователи не работают параллельно. данные записываются в файл test-site.log

эта проблема решается в **generator-new.py**, где используется модуль симуляций, что позволяет работать функциям параллельно, а значит, создавать более реалистичную картину "посещений" сайта

**auditor.py** же является той самой моделью СОВ, которая подключается на проверку к test-site.log, анализируя его на предмет вторжений (DOS и SQLi), предупреждения об атаках выносятся в консоль

данный каталог в общем представляет собой тестовую систему, опыт работы с которой позволил написать свою IPS

### IPS (2021-2022)
в этом каталоге находятся программы, представляющие собой часть работы системы обнаружения и предотвращения вторжений, а также сопровождающее её описание (фактически - выдержки из ВКР)

файлы в каталоге:
- **AUDITOR.py** - собственно, сама СОПВ, должна подключаться к файлу логов сервера Apache на виртуальной машине
- **USERS.py** - программа, создающая множество подключений (настраиваемых, то есть, от простых посещений доступных страничек до DOS-атак или видимости SQLi) к сайту в интернете (в данном случае, к сайту, работающему через pagekite)
- **tor.bat** - создание подключений для Tor (для доступа к сайту с разных IP-адресов)
- **report** - каталог, куда сохраняется отчёт по работе "Аудитора"
- **readme.docx** - краткая выдержка по работе системы из ВКР

   

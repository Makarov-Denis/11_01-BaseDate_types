# Домашнее задание к занятию "`Базы данных, их типы`" - `Макаров Денис`


### Инструкция по выполнению домашнего задания

   1. Сделайте `fork` данного репозитория к себе в Github и переименуйте его по названию или номеру занятия, например, https://github.com/имя-вашего-репозитория/git-hw или  https://github.com/имя-вашего-репозитория/7-1-ansible-hw).
   2. Выполните клонирование данного репозитория к себе на ПК с помощью команды `git clone`.
   3. Выполните домашнее задание и заполните у себя локально этот файл README.md:
      - впишите вверху название занятия и вашу фамилию и имя
      - в каждом задании добавьте решение в требуемом виде (текст/код/скриншоты/ссылка)
      - для корректного добавления скриншотов воспользуйтесь [инструкцией "Как вставить скриншот в шаблон с решением](https://github.com/netology-code/sys-pattern-homework/blob/main/screen-instruction.md)
      - при оформлении используйте возможности языка разметки md (коротко об этом можно посмотреть в [инструкции  по MarkDown](https://github.com/netology-code/sys-pattern-homework/blob/main/md-instruction.md))
   4. После завершения работы над домашним заданием сделайте коммит (`git commit -m "comment"`) и отправьте его на Github (`git push origin`);
   5. Для проверки домашнего задания преподавателем в личном кабинете прикрепите и отправьте ссылку на решение в виде md-файла в вашем Github.
   6. Любые вопросы по выполнению заданий спрашивайте в чате учебной группы и/или в разделе “Вопросы по заданию” в личном кабинете.
   
Желаем успехов в выполнении домашнего задания!
   
### Дополнительные материалы, которые могут быть полезны для выполнения задания

1. [Руководство по оформлению Markdown файлов](https://gist.github.com/Jekins/2bf2d0638163f1294637#Code)

---

### Задание 1. СУБД

Кейс

Крупная строительная компания, которая также занимается проектированием и девелопментом, решила создать правильную архитектуру для работы с данными. Ниже представлены задачи, которые необходимо решить для каждой предметной области.
Какие типы СУБД, на ваш взгляд, лучше всего подойдут для решения этих задач и почему?

1.1. Бюджетирование проектов с дальнейшим формированием финансовых аналитических отчётов и прогнозирования рисков. СУБД должна гарантировать целостность и чёткую структуру данных.

1.1.* Хеширование стало занимать длительно время, какое API можно использовать для ускорения работы?

1.2. Под каждый девелоперский проект создаётся отдельный лендинг, и все данные по лидам стекаются в CRM к маркетологам и менеджерам по продажам. Какой тип СУБД лучше использовать для лендингов и для CRM? СУБД должны быть гибкими и быстрыми.

1.2.* Можно ли эту задачу закрыть одной СУБД? И если да, то какой именно СУБД и какой реализацией?

1.3. Отдел контроля качества решил создать базу по корпоративным нормам и правилам, обучающему материалу и так далее, сформированную согласно структуре компании. СУБД должна иметь простую и понятную структуру.

1.3.* Можно ли под эту задачу использовать уже существующую СУБД из задач выше и если да, то как лучше это реализовать?

1.4. Департамент логистики нуждается в решении задач по быстрому формированию маршрутов доставки материалов по объектам и распределению курьеров по маршрутам с доставкой документов. СУБД должна уметь быстро работать со связями.

1.4.* Можно ли к этой СУБД подключить отдел закупок или для них лучше сформировать свою СУБД в связке с СУБД логистов?

1.5.* Можно ли все перечисленные выше задачи решить, используя одну СУБД? Если да, то какую именно?

Приведите ответ в свободной форме.

Ответы:

1.1 Для четкой структуры и целостности подойдет реляционная СУБД.

1.2 Для гибкой и быстрой на мой взгляд подойдет реляционная СУБД или графовая.

1.3 Для данной задачи необходимо использовать документо-ориентированные СУБД - запрос по ключу, получение значение.

1.4 Для данной задачи по моему мнению подходят графовые СУБД - предназначены для работы с графами, с их узлами, свойствами, и произвольными отношениями между узлами.

---

### Задание 2. Транзакции

2.1. Пользователь пополняет баланс счёта телефона, распишите пошагово, какие действия должны произойти для того, чтобы транзакция завершилась успешно. Ориентируйтесь на шесть действий.

2.1.* Какие действия должны произойти, если пополнение счёта телефона происходило бы через автоплатёж?

Приведите ответ в свободной форме.

Ответ:

Для выполнение транзакции пополнения баланса счета телефона необходимо выполнить следующие 6 действий:

1. Начало транзакции.
2. Проверка соответствия назначенной и внесенной суммы для пополнения.
3. Подтверждение внесенной суммы.
4. Соединение с оператором и его БД и перевод суммы на нужный счет.
5. Подтверждение, что сумма внесена.
6. Закрытие транзакции.

---

### Задание 3. SQL vs NoSQL

3.1. Напишите пять преимуществ SQL-систем по отношению к NoSQL.

3.1.* Какие, на ваш взгляд, преимущества у NewSQL систем перед SQL и NoSQL.

Ответ:

 - Стандартизированный язык - благодаря документации и длительному внедрению в течение многих лет, он предоставляет единую платформу по всему миру для всех своих пользователей
 - Масштабируемость - базы данных SQL могут обрабатывать большие объемы данных и могут быть увеличены или уменьшены в соответствии с требованиями приложения
 - Безопасность - базы данных SQL имеют встроенные функции безопасности, которые помогают защитить данные от несанкционированного доступа, такие как аутентификация пользователя, шифрование и контроль доступа
 - Резервное копирование и восстановление - базы данных SQL имеют встроенные средства резервного копирования и восстановления, которые помогают восстанавливать данные в случае системных сбоев, сбоев или других катастроф
 - Согласованность данных - базы данных SQL обеспечивают согласованность данных в нескольких таблицах за счет использования транзакций, которые гарантируют, что изменения, внесенные в одну таблицу, отражаются во всех связанных таблицах

---

### Задание 4. Кластеры

Необходимо производить большое количество вычислений при работе с огромным количеством данных, под эту задачу выделено 1000 машин.

На основе какого критерия будете выбирать тип СУБД и какая модель распределённых вычислений здесь справится лучше всего и почему?

Приведите ответ в свободной форме.

Ответ:

Исходя из того, что будет 1000 машин, вряд ли они будут обращаться к единому серверу, т.к. сервер возможно и не выдержит такой нагрузки, сколько не расширяй его добавлением ОЗУ, новым процессором и т.п. Здесь понадобится горизонтальная масштабируемость, с чем хорошо справляется СУБД noSQL. В данном случае из-за большого количества вычислений мнекажется что подойдет именно колоночная система, так как она хранит данные не в виде строк, а в виде столбцов, что позволяет ускорять выполнение запросов к большим объемам данных, особенно при работе с аналитическими системами, где требуется обработка большого количества информации.

По модели распределенных вычислений вопрос не очень понятен, т.к. всё это новое. Погугилив информацию нашел вот эту статью (https://aws.amazon.com/ru/what-is/distributed-computing/). Как я понял, с горизонтальным увеличением мощностей вычисления будут распределяться либо равномерно, либо в зависимости от выполняемой задачи. Хотя в данном случае один узел получит трудную задачу и будет долго ее выполнять. А другой узел, получивший легкую задачу и быстро ее выполнивший, будет простаивать. И в данном случае либо придется смириться с этим, либо настраивать узлы так, чтобы освободившийся от легкой задачи узел искал новую задачу или подхватывал помогать решать трудную. Еще вариант и он опять же связан с настройкой. Все эти машины придется делить на узлы. Узлы, которым буду назначаться трудоемкие вычисления, будут состоять из большего количества машин или же более производительных. Хотя можно объединить оба варианта. Ну и для легких задач, соответственно, машины послабее.

Также из представленной ранее статьи мне кажется можно было бы использовать еще трехуровневую архитектуру, или N-уровневую. Ну а если серверов в данной системе не будет по какйо-то причине, то пиринговую, в которой на все компьютеры в сети возлагаются одинаковые обязанности. Разделение на клиентские и серверные компьютеры отсутствует, и любой компьютер может выполнять все функции.

---

Задания,помеченные звёздочкой, — дополнительные, то есть не обязательные к выполнению, и никак не повлияют на получение вами зачёта по этому домашнему заданию. Вы можете их выполнить, если хотите глубже разобраться в материале.

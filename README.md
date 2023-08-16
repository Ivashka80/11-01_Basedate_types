# Домашнее задание к занятию «Базы данных, их типы»

<details>

### Инструкция по выполнению домашнего задания

1. Сделайте fork [репозитория c шаблоном решения](https://github.com/netology-code/sys-pattern-homework) к себе в Github и переименуйте его по названию или номеру занятия, например, https://github.com/имя-вашего-репозитория/gitlab-hw или https://github.com/имя-вашего-репозитория/8-03-hw).
2. Выполните клонирование этого репозитория к себе на ПК с помощью команды `git clone`.
3. Выполните домашнее задание и заполните у себя локально этот файл README.md:
   - впишите вверху название занятия и ваши фамилию и имя;
   - в каждом задании добавьте решение в требуемом виде: текст/код/скриншоты/ссылка;
   - для корректного добавления скриншотов воспользуйтесь инструкцией [«Как вставить скриншот в шаблон с решением»](https://github.com/netology-code/sys-pattern-homework/blob/main/screen-instruction.md);
   - при оформлении используйте возможности языка разметки md. Коротко об этом можно посмотреть в [инструкции по MarkDown](https://github.com/netology-code/sys-pattern-homework/blob/main/md-instruction.md).
4. После завершения работы над домашним заданием сделайте коммит (`git commit -m "comment"`) и отправьте его на Github (`git push origin`).
5. Для проверки домашнего задания преподавателем в личном кабинете прикрепите и отправьте ссылку на решение в виде md-файла в вашем Github.
6. Любые вопросы задавайте в чате учебной группы и/или в разделе «Вопросы по заданию» в личном кабинете.

Желаем успехов в выполнении домашнего задания.

---
</details>

### Задание 1. СУБД

### Кейс
Крупная строительная компания, которая также занимается проектированием и девелопментом, решила создать 
правильную архитектуру для работы с данными. Ниже представлены задачи, которые необходимо решить для
каждой предметной области. 

Какие типы СУБД, на ваш взгляд, лучше всего подойдут для решения этих задач и почему? 
 
1.1. Бюджетирование проектов с дальнейшим формированием финансовых аналитических отчётов и прогнозирования рисков.
СУБД должна гарантировать целостность и чёткую структуру данных.

*Ответ*

<details>

Четкая структура и целостность - тут подойдет реляционная СУБД.
</details>

1.2. Под каждый девелоперский проект создаётся отдельный лендинг, и все данные по лидам стекаются в CRM к 
маркетологам и менеджерам по продажам. Какой тип СУБД лучше использовать для лендингов и для CRM? 
СУБД должны быть гибкими и быстрыми.

*Ответ*

<details>

Здесь я бы выбрал реляционную СУБД или графовую.

</details>

1.3. Отдел контроля качества решил создать базу по корпоративным нормам и правилам, обучающему материалу 
и так далее, сформированную согласно структуре компании. СУБД должна иметь простую и понятную структуру.

*Ответ*

<details>

Документо-ориентированные СУБД - запрос по ключу, получл значение.

</details>

1.4. Департамент логистики нуждается в решении задач по быстрому формированию маршрутов доставки материалов 
по объектам и распределению курьеров по маршрутам с доставкой документов. СУБД должна уметь быстро работать
со связями.

*Ответ*

<details>

Графовые СУБД - предназначены для работы с графами, с их узлами, свойствами, и произвольными отношениями между узлами.

</details>

---

### Задание 2. Транзакции

2.1. Пользователь пополняет баланс счёта телефона, распишите пошагово, какие действия должны произойти для того, чтобы 
транзакция завершилась успешно. Ориентируйтесь на шесть действий.


*Ответ*

<details>

1. Начало транзакции.
2. Проверка соответствия назначенной и внесенной суммы для пополнения.
3. Подтверждение внесенной суммы.
4. Соединение с оператором и его БД и перевод суммы на нужный счет.
5. Подтверждение, что сумма внесена.
6. Закрытие транзакции.

</details>

---

### Задание 3. SQL vs NoSQL

3.1. Напишите пять преимуществ SQL-систем по отношению к NoSQL. 


*Ответ*

<details>

- Стандартизированный язык - благодаря документации и длительному внедрению в течение многих лет, он предоставляет единую платформу по всему миру для всех своих пользователей
- Масштабируемость - базы данных SQL могут обрабатывать большие объемы данных и могут быть увеличены или уменьшены в соответствии с требованиями приложения
- Безопасность - базы данных SQL имеют встроенные функции безопасности, которые помогают защитить данные от несанкционированного доступа, такие как аутентификация пользователя, шифрование и контроль доступа
- Резервное копирование и восстановление - базы данных SQL имеют встроенные средства резервного копирования и восстановления, которые помогают восстанавливать данные в случае системных сбоев, сбоев или других катастроф
- Согласованность данных - базы данных SQL обеспечивают согласованность данных в нескольких таблицах за счет использования транзакций, которые гарантируют, что изменения, внесенные в одну таблицу, отражаются во всех связанных таблицах
   
</details>

---

### Задание 4. Кластеры

Необходимо производить большое количество вычислений при работе с огромным количеством данных, под эту задачу 
выделено 1000 машин. 

На основе какого критерия будете выбирать тип СУБД и какая модель *распределённых вычислений* 
здесь справится лучше всего и почему?


*Ответ*

<details>

Здесь важны следующие пункты:
-  много данных
-  много расчётов
-  частое обновления информации
-  быстро посмотреть информацию
-  быстро выдать результат
  
В данном случае я выберу реляционную СУБД.

</details>

---

Задания,помеченные звёздочкой, — дополнительные, то есть не обязательные к выполнению, и никак не повлияют на получение вами зачёта по этому домашнему заданию. Вы можете их выполнить, если хотите глубже разобраться в материале.

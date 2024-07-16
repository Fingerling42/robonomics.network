---
title: Web3 DevOps-стек робототехники
date: 2024-06-12
published: true
locale: 'ru'
tags: ['DevOps', 'Web3']
cover_image: ../images/web3-devops-stack/web3-devops-stack-Cover.png
description: "DevOps-движение полностью изменило мир IT и наши представления о том как должна быть устроена эффективная разработка непрерывно улучшающихся систем. Мир робототехники только начинает знакомство с этим подходом, поэтому в новой статье мы попробовали изобразить концептуальное будущее DevOps для робототехники на базе Web3 технологий и выбрали пару близких к нам проектов, которые могли бы составить его основу."
abstract: "DevOps-движение полностью изменило мир IT и наши представления о том как должна быть устроена эффективная разработка непрерывно улучшающихся систем. Мир робототехники только начинает знакомство с этим подходом, поэтому в новой статье мы попробовали изобразить концептуальное будущее DevOps для робототехники на базе Web3 технологий и выбрали пару близких к нам проектов, которые могли бы составить его основу."
---

## Истоки Development & Operations

Роботы, как движущиеся и чувствующие внешний мир устройства, являются частным случаем компьютеров. Как часто говорят инженеры, самолёт - это летающий компьютер, подчеркивая значимость бортового вычислительного устройства для поддержания жизнеспособности этой кибер-физической системы. Поэтому мы можем взглянуть на то как развивался мир информационных систем в 21 веке и выявить определённые тренды, которые будет присущи и робототехнике в самое ближайшее время.

Программное обеспечение и применяемые для его разработки практики существенно изменили подходы к работе как в инженерии, так и в любой другой деятельности. В первую очередь изменения коснулись так называемого водопадного подхода, когда любой проект представлялся в виде продолжительных последовательно чередующихся стадий: Требования - Разработка - Верификация - Валидация - Эксплуатация. Со временем оказалось, что разделение на стадии удобно для менеджеров, но не очень соответствует тому как это происходит в жизни и затрудняет быструю адаптацию продуктов в условиях постоянно меняющегося внешнего мира. На смену водопадной модели деятельности (и менеджмента) пришли гибкие методологии, предполагающие синхронную работу над проектом с небольшими интервалами планирования. Вместо больших стадий с вехами появились небольшие спринты с инкрементами - небольшими, но частыми изменениями в разрабатываемых системах с быстрым выходом в релиз. Такой темп работы недостижим, если сопровождать выпуск релиза сложными административными процедурами с ручными проверками. Так возникло движение Development & Operations по внедрению практик передачи ценности (value) от разработчикам к потребителям без потерь и новая профессия инженера DevOps, автоматизирующего процесс быстрого ввода системы в эксплуатацию. 

![devops origins](../images/web3-devops-stack/devops-evolution.png)

Эти практики работы включают в себя автоматизированное тестирование, непрерывную интеграцию, доставку, развёртывание и мониторинг работы программного обеспечения. Изначально они получили распространение в сфере крупных веб-сервисов, обслуживающих миллионы пользователей по всему миру, но со временем, по мере того как инструменты автоматизации стали доступнее (в том числе благодаря Open Source), DevOps стали применяться в более классических видах инженерной деятельности.

## Особенности роботов в отношении DevOps

Роботы, в отличие от неподвижных серверов и дата-центров, движутся в пространстве и чувствуют внешнюю среду. Такого рода устройств становится всё больше и больше. Мы видим как со временем растёт их вычислительная мощность - многие технические решения были бы попросту невозможны без производительного процессора на борту. По мере роста объёмов edge-вычислений (то есть вычислений на самих мобильных устройствах), использование DevOps набирает популярность, что позволяет быстро доносить новые разработанные функции до потребителей. Роботы могут быть непрерывно подключены к сети и оперативно обновлять своё программное обеспечения, используя Docker и другие зарекомендовавшие себя в практической деятельности инструменты.

Впрочем, дополнительные возможности создают и дополнительные риски - наделяя компьютеры способностью к интенсивному взаимодействию с внешней средой и с интернет одновременно, мы создаём и предпосылки для потенциального вреда, который эти устройства могут нанести, если попадут под контроль злоумышленников. Умные устройства, постепенно наполняющие наши дома, могут в один момент стать безумными! Вопрос безопасности тут имеет первостепенное значение в условиях непрерывно меняющегося мира, потому что все эти устройства находятся в непосредственной близости к нашим телам. Ошибки могут стоить слишком дорого.

Что же делает робототехнику особенной и выделяет её от остальных компьютеров? К этим особенностям можно отнести:

1. Разнообразие аппаратных платформ (в отличие от сравнительно небольшого числа типов архитектуры центральных процессоров)
2. Работа в слабо предсказуемых средах, что подразумевает наличие нештатных ситуаций - например, недоступность по каналам связи
3. Ограниченные ресурсы бортовых вычислительных устройств - слабый процессор, сравнительное небольшое количество оперативной памяти и низкая пропускная способность сети
4. Повышенные требования к безопасности
5. Большое количество устройств, которым требуются обновления и новые функции

С учётом этих ограничений мы попробуем сформулировать концептуальную основу DevOps для роботов на базе web3-технологий, как минимум, для написания кода, сборки и деплоя. Мы попробуем представить наиболее интересные Web3-проекты, способные обеспечить функционирование децентрализованного DevOps-конвейера и показать как Робономика может стать органичной его частью на заключительной фазе жизненного цикла - при воплощении программ во внешнем мире.

## Web3 и Blockchain

Когда речь идёт о Web3, то подразумевается прежде всего технология Блокчейн. Это конечно близкие понятия, но всё-же не совсем тождественные. Часто под этим понятием подразумевается целое множество технологий - криптография на эллиптических кривых, p2p-сети, алгоритм консенсуса. Первые два пункта не являются чем-то уникальным и применяются широко в IT-индустрии, тогда как последнее действительно наделяет блокчейн особым свойством, делающим это решение столь мощным инструментом. Но нужен ли нам консенсус для всех случаев жизни (и частей DevOps-конвейера)? Давайте попробуем разобраться.

Консенсус имеет разные значения в разных контекстах, но смысл его всегда неизменен - системы, акторы или автономные агенты, составляющие децентрализованную сеть, приходят согласию по поводу того какой используют в работе протокол и состояние общих данных. Если стороны не приходят к согласию, то это приводит к так называемому Fork’у. Исторически под fork’ом подразумевалось раздвоение цепочки блоков, которое приводило к разделению сети узлов на две части - часть узлов оставалась “верна” старой версии протокола, тогда как остальная часть переходила на новую версию. Это событие всегда имело отрицательный контекст - сообщество вместо консолидации уменьшалось, что делало проект как-бы более слабым. В тоже время, как биологической эволюции, так и в её техно-версии, наблюдаемой нами сейчас в форме экономики, разветвление происходит постоянно и, более того, именно оно приводит к появлению новых форм жизни. Взгляните на древо жизни. Каждая ветка на ней - это произошедший в древние времени Fork - мутация породила новый вид, который стал несовместим со своими соплеменниками. Не будь этого механизма, то жизнь в её современном понимания была бы невозможна. Именно возможность организмов мутировать позволяет приспосабливаться к изменяющимся условиям окружающей среды.

Таким образом, мы приходим к выводу о том, что консенсус - это одновременно хорошо, потому что позволяет согласовывать поведения многих акторов и масштабироваться, но в тоже время и плохо, потому что затрудняет появление нового, ведь отошедшие от консенсуса всегда считаются изгоями и система как бы “выдавливает” их.

В отличие от биологической эволюции, техноэволюцию осуществляем мы, люди, и именно от нас зависит то, каким образом эта эволюция осуществляется. Источником мутаций в технике являются инженеры, применяющие научный метод и творческое мышление для порождения новых, более перспективных и жизнеспособных версий техники. Нам выгодно, чтобы мутации происходили чаще, нам выгодна децентрализация в сфере порождения новых эффективных решений как в отношении техники, так и в отношении организаций. И напротив - ситуация, когда “побеждает” одна точка зрения и достигается полный и безоговорочный консенсус, чревата рисками обрушения всего при определённом стечении обстоятельств. Именно поэтому природа пошла не по пути создания сверх-организмов размером с планету, а по пути децентрализации - когда все живые существа рассредоточены по экологическим нишам и экосистемам, что делает устойчивой жизнь в целом и даже стабилизирует саму планету Земля согласно модели [Маргаритковый мир](https://ru.wikipedia.org/wiki/%D0%9C%D0%B0%D1%80%D0%B3%D0%B0%D1%80%D0%B8%D1%82%D0%BA%D0%BE%D0%B2%D1%8B%D0%B9_%D0%BC%D0%B8%D1%80) (если коротко, то благодаря биосфере и её разнообразию планета становится более устойчивой).

К чему это отступление? Прежде всего хотелось бы донести до читателя мысль о том, что не все данные требуют обязательного консенсуса, поэтому далеко не во всех сценариях целесообразно применять блокчейн. Консенсус нужен в тех случаях, когда мы действуем в условиях когда несогласованные действия могут привести к непоправимым последствиям. Например, он остро необходим на перекрёстке автомобильных дорог. Если нет согласия по части правил дорожного движения на какой цвет можно ехать, а на какой нельзя, то можно представить к чему может довольно скоро привести такая ситуация!

Возвращаясь к основной теме статьи, можно сделать предположение, что консенсус уместен там, где высоки риски и, наоборот, в случаях, когда риски невелики, то уместнее выбрать полностью децентрализованную систему без консенсуса. Разработка кода сама по себе - относительно безопасное мероприятие, пока она остаётся в состоянии исходных или даже исполняемых файлов на сборочном сервере. Однако, когда речь идёт о развёртывании этих файлов в физической инфраструктуре реального мира, то очень важно быть согласованными. Именно поэтому для первых двух пунктов нашего DevOps-стека (разработка и сборка) мы подобрали близкие по духу проекты без консенсуса.

## Первая фаза - Разработка - Radicle

![](../images/web3-devops-stack/1st-phase-development.png)

Итак, в сфере разработки кода нужны полная свобода и децентрализация, чтобы стимулировать генерацию лучших решений напрямую от авторов. К нашему с вами счастью, в индустрии разработки кода и так де-факто победила децентрализованная по своей природе система хранения и управления версиями. Речь, разумеется, о git. git априори не подразумевает наличия единого “источника правды” - любому пользователю, прежде чем воспользоваться кодом, нужно клонировать репозиторий на свой компьютер и работать уже со своей локальной копией. В добавок ко всему, сама структура хранения данных в хранилище является ничем иным как цепочкой блоков (зафиксированных фактов изменений кода - коммитов), которые гарантируют неизменяемость истории. То есть git сам по себе является своеобразным блокчейном, консенсус между которым достигается вручную самими авторами посредством ответвлений и запросов на слияние.

Тем не менее, несмотря на децентрализованную природу git, платформы из мира второго поколения веб-технологий взяли своё. Сейчас разработка кода практически полностью централизована относительно небольшим числом платформ вроде Github, Bitbucket, Gitlab. И произошло это как раз таки за счёт внедрения дополнительных  инструментов: DevOps (CI/CD конвейеры, встроенные функции выявления уязвимостей в зависимостях исходного кода и многое другое) и Social Networking (системы вознаграждения разработчиков, issue tracking, project management). Эти инструменты не входят в состав исходного протокола git и затрудняют миграцию проектов от платформы к платформе.

Именно с целью освободить разработчиков кода от необходимости зависеть от крупных платформ был основан проект [Radicle](https://radicle.xyz/), который мы рассматриваем в качестве первого компонента нашего web3-DevOps-стека. Проект имеет довольно [продолжительную историю](https://docs.radworks.org/community/our-story) и ряд значимых трансформаций на пути к его текущему моменту. Первоначально Radicle был построен поверх только набиравшей тогда популярность Inter Planetary File System (IPFS), но в какой-то момент разработчики поняли, что способы хранения и хеширования данных репозитория кода в IPFS несовместимы со способами хранения в git, что приводило к дублированию информации и избыточному расходованию трафика даже в случае небольших обновлений. Постепенно было принято решение перейти на более минималистичное решение - обмениваться напрямую патчами git, используя нативный [pack протокол](https://git-scm.com/docs/pack-protocol/en), сделать это основным способом передачи данных в сети “хранителей кода”. Это решение послужило началом большого рефакторинга и переписывания проекта с Go на Rust. Новая версия протокола под названием Heartwood черпает вдохновение из таких проектов как Secure Scuttlebutt (SSB) и Bitcoin’s [Lightning Network](https://en.wikipedia.org/wiki/Lightning_Network).

Чуть позже, в 2021 году была основана Децентрализованная Автономная Организация (или просто DAO) Radworks на блокчейне Ethereum, выпущен токен управления RAD и привлечены необходимые средства на дальнейшее развитие проекта. Судя по всему, команда проекта не отрицает значимость социальной и экономической составляющих в разработке кода, но при этом не пытается интегрировать все поддерживающие инструменты внутрь своей имплементации. Одной из такого рода инициатив является их проект и одноимённый смарт-контракт [Drips](https://www.drips.network/), который ориентирован на автоматическое распределение пожертвований между разработчиками открытого исходного кода под слоганом “Fund your dependencies”. В рамках этого смарт-контракта каждый проект разработки может настроить автоматическое перераспределение полученных пожертвований для своего набора зависимостей (пакетов, библиотек).

Совсем недавно, в марте 2024 года вышел релиз 1.0.0 имплементации протокола Heartwood, а значит уже можно рассматривать его для продакшн сценариев децентрализованных конвейеров разработки.

## Вторая фаза - Сборка, тестирование, непрерывная интеграция - Fluence

![web3 build software](../images/web3-devops-stack/2nd-phase-build.png)

Далее в нашем упрощённом DevOps-конвейере следует этап сборки, который, конечно же, не исчерпывается компиляцией кода. На самом деле сюда входит целая россыпь процессов, требующих вычислений разной степени ресурсоёмкости. Причём эти вычисления далеко не всегда приводят к каким-то изменениям во внешнем мире. Иными, словами не каждое изменение кода и запуск сборки приводит в выпуску релиза. Часто CI-конвейеры запускаются по расписанию, а порождаемые ими артефакты имеют крайне небольшой срок жизни и удаляются, если их не добавляют в релиз. Именно по этой причине мы также не рассматриваем данную стадию в жизненном цикле разработки как требующую консенсуса, так же как и многочисленные проекты облачных вычислений через верификацию результатов в блокчейне.

Похожей позиции придерживаются и разработчики [Fluence](https://fluence.dev/). Это очень близкий к Robonomics проект, который также интенсивно использует libp2p как слой транспорта и ipfs как слой хранения в своих сценариях использования, при этом сосредотачиваясь на оркестрации пиров и вычислениях на них без потребности в централизованных платформах. Давайте рассмотрим их подробнее.

Fluence состоит из двух ключевых компонентов - Aqua и Marine. Первый представляет собой предметно-специфичный язык (так называемый, DSL) и служит для управления очерёдностью исполнения заданий на вычислительных устройствах, то есть для оркестрации пиров. С одной стороны, освоение очередного языка может оттолкнуть многих пользователей, с другой стороны это честный шаг, который сразу настраивает на неизбежное будущее. Дело в том, что большинство CI-платформ обычно предлагает для управления и настройки конвейеров конфигурационные файлы в каком-то из распространённых форматов вроде YAML или JSON. Поначалу это действительно удобно и позволяет любому пользователю без навыков программирования начать работу, но со временем, по мере роста потребностей и, соответственно, количества конфигов, отсутствие столько привычных для программистов инструментов приводит к росту boilerplate-кода и невозможности управлять сложностью. Попытки сделать из YAML язык конфигурации с помощью шаблонов тоже не решает проблемы, что способствует появлению Ad-hoc языков описания конфигурации как HCL (HashiCorp Configuration Language). Aqua предлагает сразу решение в виде прикладного языка программирования для потока вычислений, имеющего надёжную теоретическую основу в виде Пи-исчисления, в которое компилируется в Aqua-код для дальнейшего исполнения на пирах. Это делает порог вхождения в технологию чуть выше, но по идее должен обеспечить более стабильную и поддерживаемую работу в будущем. Сейчас Aqua является достаточно низкоуровневым языком, но со временем могут появиться библиотеки, реализующие лучшие практики проектирования потоков вычислений с использованием удобных математических абстракций, что ускорит разработку распределённых вычислений.

Aqua задаёт порядок вычислений, но сами вычисления подготавливаются и осуществляются с помощью Marine - компонента, также разрабатываемого Fluence. Marine представляет собой SDK (Software Developers Kit) - набор инструментов для сборки совместимых  между собой Webassembly модулей, а также Runtime - среду общего назначения для их исполнения. Модули являются относительно независимыми программными компонентами, каждый из которых хранит собственное состояние, но при этом могут взаимодействовать друг с другом с помощью импорта/экспорта функций. Набор взаимодействующих модулей образует собой сервис, который реализует сложное поведение и является актором в Fluence сети пиров.

Совместно Aqua и Marine обеспечивают в полной мере то, что можно назвать мышлением кибер-физической системы - то есть всё многообразие вычислений, помогающее принимать решения о том какие действия предпринять во внешнем мире, чтобы повысить шансы на успех в эволюционной гонке. 

Моделе-ориентированная робототехника нуждается в ресурсоёмких вычислениях. Значительная часть тестов разрабатываемого программного обеспечения для роботов выполняется в симуляторах, а алгоритмы, построенные на обучении с подкреплением, запускают такие виртуальные среды сотни тысяч раз, прежде чем получить желаемое поведение агента. В качестве виртуальных сред могут выступать самые разнообразные движки физики и рендеринга, а также основанные на них игровые движки. В этих средах в последнее время получил распространение паттерн проектирования Entity Component System. К слову, современная версия широко известного в узких кругах симулятора робототехники Gazebo/ex-Ignition от Open Robotics (они же разрабатывают ROS) также [использует ECS](https://gazebosim.org/docs/harmonic/architecture) для повышения производительности и гибкости. Собственно, по словам разработчиков Fluence, их модель исполнения как раз хорошо подходит именно для реализации распределённых архитектур, построенных по такому принципу.

Конечно, чтобы собранное и протестированное программное обеспечение дало свои плоды, оно должно быть развёрнуто на аппаратных платформах. Гипотетически разворачивать программное обеспечение возможно конечно и с помощью Fluence. Собственно, сами разработчики говорят о том, что их стек в том числе позволяет выполнять деплой на пирах и это действительно так. Однако, мы считаем, что в области взаимодействия с внешней средой и физическим оборудованием нужен и важен консенсус.

## Третья фаза - Развёртывание - Robonomics

![robotics deployment art](../images/web3-devops-stack/3rd-phase-deploy.png)

Важной особенностью программного обеспечения является тот факт, то само по себе оно не меняет внешний мир, а служит моделью окружающей реальности и помогает осуществлять какие-то рассуждения о ней - строить гипотезы, предлагать план действий, запускать процессы во внешнем мире с помощью оборудования или людей. Например, issue tracker сам по себе не является системой, меняющий внешний мир, его можно назвать цифровым двойником команды разработки, которая в свою очередь и проводит изменения в жизнь. Благодаря issue tracker команда может может согласовывать действия друг с другом, помогать в этом. Иными словами, issue tracker позволяет поддерживать консенсус внутри команд разработки - кто какие задачи делает и когда - но само изменение проводится людьми.

Когда мы говорим о системах меняющих мир, то подразумеваем физически существующих и действующих в реальном мире агентов - умные устройства, роботы, автономные фабрики. Собственно, Робономика по своей изначальной задумке и является своеобразным мостом от информационных систем и людей к внешнему миру через робототехнические системы. Безопасность тут крайне важна и пренебрежение ей сулит не только потери капиталов, но и настоящие техногенные катастрофы. Несмотря критическую значимость этих систем, первые защищённые децентрализованные хранилища появились всё-таки не в сфере промышленности, а в сфере финансов. Наши счета в банках оказались куда более лакомым кусочком для компьютерных преступников, нежели бытовые приборы, подавляющая часть которых не имела подключения к сети. Технологии обеспечения безопасности банковских информационных систем прошли большой путь - от SWIFT до Ethereum - и теперь постепенно внедряются в другие сектора экономики. Робономика действует в этом фронтире безопасных децентрализованных сетей и мы делегируем ей заключительную часть web3 DevOps-конвейера - деплой.

В общем случае, деплой - это ввод системы в эксплуатации. Более привычным синонимом этого термина является установка (install) - некое событие, после которого произведённая и доставленная в нужное место система (экземпляр определённого вида оборудования, исполняемого файла программного обеспечения) начинает своё функционирование и выполнение роли в системе более высокого уровня. Чем именно хорош в данном случае блокчейн? Прежде всего тем, что выпуская какую-то версию программы во внешний мир, нам всегда важно понимать что именно было выпущено. В ходе разработки версии могут меняться очень часто и это нормально, поэтому фиксировать их в цепочке блоков нецелесообразно. Однако, событие выпуска наружу или релиза требует фиксации, чтобы при получении обратной связи мы могли однозначно понять с какой именно версией исходных кодов или чертежей нам нужно эту обратную связь сопоставить. Блокчейн может служить надёжным хранилищем информации о всех обновлениях программного обеспечения подключённых к нему устройств.

Также установка должна быть согласованной - рассогласования в установке чреваты так называемыми конфигурационным коллизиями. К коллизиям можно отнести несоответствие версий взаимодействующих программных модулей системы, разворачивание разных систем в одной области пространства и тому подобные негативные явления. Собственно, упомянутое выше столкновение автомобилей на нерегулируемом перекрёстке является как раз примером такой коллизии. В случае с разворачиванием программного обеспечения коллизиями могут являться нарушение API, нехватка аппаратных возможностей, запись в запрещённые или небезопасные места в памяти. Робономика может хранить конфигурацию подключённого к ней оборудования и на уровне алгоритма консенсуса запрещать подобные состояния.

Для разворачивания программного обеспечения в парачейне Робономики можно использовать специальный вызов [launch](https://wiki.robonomics.network/docs/launch/), который позволяет осуществлять запуск подключённого к блокчейну узла с дополнительными параметрами. В качестве параметра может выступать уникальный идентификатор в сети дистрибьюции контента IPFS, по которому можно получить образ программного обеспечения, бинарный файл, исходный код конфигурации операционной системы или даже bash-скрипт! Так как каждая транзакция в сети подписывается криптографическим ключом, то по сути такой вызов в парачейне эквивалентен публичной подписи релиза.

Для более сложных сценариев можно использовать [digital twin](https://wiki.robonomics.network/docs/digital-twins/), который позволяет задать таблицу соответствия между произвольными данными длиной в 256 бит и аккаунтом в сети Робономики. Тем самым, можно вести журнал изменений версий конфигурации для аккаунтов устройств в сети Робономики. В традиционных системах конфигурации и развёртывания в качестве узлов обычно указываются хосты - это компьютеры с DNS именем или IP-адресом. В случае web3 хосты идентифицируются благодаря своим публичным криптографическим ключам, к которым привязаны аккаунты. Для изменения конфигурации, можно добавить новый идентификатор контента, из которого устройство получит новую версию ПО и обновится.

## Собираем всё вместе

![web3 devops stack](../images/web3-devops-stack/devop-stack-full-art.png)

Итак, давайте попробуем посмотреть на это свысока. Люди составляют ядро нашей большой кибер-физической системы. Люди хаотичны, непредсказуемы… и это хорошо! Они порождают новые смыслы, идеи, продукты. Они реализуют свою волю по изменению мира. Теперь, в 21 веке изменять мир собственными руками не требуется. Перед человечеством стоят такие задачи, для которых человеческие руки - не слишком подходящий инструмент. Вместо них есть машины, которые и служат сейчас проводником нашей воли. Машины же, напротив, строго детерминированы и предсказуемы. И люди любят это, да. Они любят, когда поезд приходит на станцию вовремя, а качество потребляемых ими продуктов всегда предсказуемо отменное. Для этого люди используют сети. Много сетей! Они порождают идеи в сети Radicle, машины собирают и тестируют их в исполняемые модули в сети Fluence, после чего разворачивают их на роботах в сети Robonomics. Роботы, в свою очередь, осуществляют преобразование среды, а их датчики, также через Robonomics, дают обратную связь людям, чтобы те приняли решение - цикл замыкается. Это цикл непрерывных улучшений, где у каждого своё место. Тут нет противоречий между машиной и человеком - оба они в гармонии создают человечество нового порядка - межпланетное человечество.
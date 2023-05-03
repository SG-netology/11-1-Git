# 11-1-Git

Базы данных, их типы - Сергей Григорьев

Задание 1. СУБД
Кейс
Крупная строительная компания, которая также занимается проектированием и девелопментом, решила создать правильную архитектуру для работы с данными. Ниже представлены задачи, которые необходимо решить для каждой предметной области.
Какие типы СУБД, на ваш взгляд, лучше всего подойдут для решения этих задач и почему?

1.1. Бюджетирование проектов с дальнейшим формированием финансовых аналитических отчётов и прогнозирования рисков. СУБД должна гарантировать целостность и чёткую структуру данных.

SQL, обеспечивается надежность и неизменяемость данных, низкий риск потери информации.

1.2. Под каждый девелоперский проект создаётся отдельный лендинг, и все данные по лидам стекаются в CRM к маркетологам и менеджерам по продажам. Какой тип СУБД лучше использовать для лендингов и для CRM? СУБД должны быть гибкими и быстрыми.

SQL, например, PostgreSQL

1.3. Отдел контроля качества решил создать базу по корпоративным нормам и правилам, обучающему материалу и так далее, сформированную согласно структуре компании. СУБД должна иметь простую и понятную структуру.

NoSQL, возможно, MongoDB

1.4. Департамент логистики нуждается в решении задач по быстрому формированию маршрутов доставки материалов по объектам и распределению курьеров по маршрутам с доставкой документов. СУБД должна уметь быстро работать со связями.

NoSQL, Графовые СУБД, предназначенные для хранения информации, связанной с графами (узлы, вершины, связи между узлами). Хорошо подходят для социальных сетей, где требуется хранить связи между пользователями по разным критериям.

Задание 2. Транзакции
2.1. Пользователь пополняет баланс счёта телефона, распишите пошагово, какие действия должны произойти для того, чтобы транзакция завершилась успешно. Ориентируйтесь на шесть действий.
Рассматриваем транзакцию для БД банка, где находится счет пользователя:
- Проверка является ли пользователь клиентом банка;
- Запрос у пользователя суммы для пополнения счета телефона;
- Проверка есть ли на банковском счету необходимая сумма;
- Перечисление средств на счет телефона;
- Корректировка баланса банковского счета;
- Уведомление пользователя о банковской операции

Задание 3. SQL vs NoSQL
3.1. Напишите пять преимуществ SQL-систем по отношению к NoSQL.

Имеют высокую производительность при работе с сильно структурированными данными и большими объёмами информации;
Имеют лучшую поддержку транзакционности, что позволяет автоматически откатывать изменения при обнаружении проблемных транзакций;
Имеют более развитое индексирование, чем NoSQL-базы, что обеспечивает более высокую производительность при выполнении сложных запросов;
Легкая установка ограничений на доступ к данным для разных пользователей, а также применение различных аутентификационных механизмов для обеспечения безопасности данных;
Имеют большую структурированность и лучшее соответствие этикету ACID;

Задание 4. Кластеры
Необходимо производить большое количество вычислений при работе с огромным количеством данных, под эту задачу выделено 1000 машин.
На основе какого критерия будете выбирать тип СУБД и какая модель распределённых вычислений здесь справится лучше всего и почему?

Можно посмотреть, что используют крупные компании, и попробовать последовать их примеру. Например, eBay, SAP, Adobe, LinkedIn, McAfee, MetLife и Foursquare используют MongoDB. Microsoft, Cloudera, IBM, Intel, Teradata, Amazon, Map R Technologies — пользователи Hadoop. И Hadoop и MongoDB являются популярными решениями для обработки Big Data. И у Hadoop и у MongoDB есть преимущества по сравнению с традиционными реляционными системами управления базами данных, которые включают в себя параллельную обработку, масштабируемость, обработку больших объемов агрегированных данных и экономичность (благодаря открытому исходному коду).

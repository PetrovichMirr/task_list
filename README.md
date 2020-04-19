О проекте
=========

**Введение**

Здравствуйте!  
Меня зовут Сергей Минеев.  
Приложение, размещенное в данном репозитории, представляет собой сайт - пример кода.
Цель его написания - оценка уровня моих знаний, навыков и опыта в области
разработки web-приложений.

При разработке использовался объектно-ориентированный подход.
Можно сказать, что данное приложение похоже на микро-фреймворк, использующий архитектурный паттерн MVC (модель, вид, контроллер).
Естественно, его возможности несоизмеримо малы по сравнению с существующими популярными фреймворками.
При работе над архитектурой приложения источником вдохновения послужил [Laravel](https://laravel.com).

Для демонстрации работы на главной странице сайта сделан список задач в 
соответствии со следующим техническим заданием (из тестового задания вакансии):

*Необходимо создать приложение-задачник.*

*Задачи состоят из:*
- *имени пользователя;*
- *е-mail;*
- *текста задачи;*

*Стартовая страница - список задач с возможностью сортировки по 
имени пользователя, email и статусу выполнения.
Вывод задач нужно сделать страницами по 3 штуки (с постраничной навигацией).
Сортировка (если указана) не должна "сбиваться" при переходе по страницам.
Видеть список задач и создавать новые может любой посетитель без авторизации.*

*При создании задачи нужно предусмотреть проверку коректности заполнения полей:
все поля обязательны для заполнения, поле "е-mail" должно быть 
валидным адресом электронной почты. После создания задачи должно 
вывестись оповещение об успешном добавлении.*

*Для проверки XSS уязвимости нужно создать задачу с тегами в описании задачи 
(добавить в поле описания задачи текст
"&lt;script&gt;alert(‘test’);&lt;/script&gt;", 
заполнить остальные поля).
Задача должна отобразиться в списке задач,
при этом не должен всплыть alert c текстом "test".*

*Создать вход для администратора (логин "admin", пароль "123").
Администратор имеет возможность редактировать текст задачи и 
поставить отметку о выполнении задачи.
Выполненные задачи в общем списке должны выводиться с соответствующей отметкой.*

Помимо реализации вышеописанной задачи на языке разметки
[Markdown](https://ru.wikipedia.org/wiki/Markdown) 
создано описание и документация разработанного проекта.
С помощью парсера Markdown содержимое файлов описания и 
документации конвертируется в HTML и выводится на страницах данного сайта.

**Применённые технические решения**

- Back-end: PHP. Использовались дополнительные PHP-пакеты, сторонние фреймворки и CMS не применялись;
- Front-end: Bootstrap 4;
- База данных: MySQL;
- Менеджер пакетов, управление зависимостями: composer;
- Создание документации API: phpDocumentor.

Пакеты:

- Аутентификация и авторизация пользователей: [cartalyst/sentinel](https://packagist.org/packages/cartalyst/sentinel);
- Парсер содержимого в формате Markdown: [erusev/parsedown](https://packagist.org/packages/erusev/parsedown);
- Конфигурация среды: [vlucas/phpdotenv](https://packagist.org/packages/vlucas/phpdotenv);

Исходный код проекта содержит как обычные комментарии, так и в стиле PHPDoc. ***Покрытие кода тестами не производилось.
Данное приложение - лишь демонстрация кода и не предназначено для использования в реальных проектах!***

При написании документации и раздела "О проекте" использован язык разметки [Markdown](https://ru.wikipedia.org/wiki/Markdown).

**Сроки разработки**

Количество потраченного времени на разработку проекта составило 8 дней (в среднем по 7-9 часов) или около 65-70 часов.
Относительные затраты времени:

- 5% - проектирование архитектуры;
- 70% - разработка ядра;
- 5% - написание тестовых модели и контроллера;
- 10% - создание файлов видов (внешний вид сайта, дизайн);
- 10% - описание проекта, документация (в том числе документация API), установка на удалённые серверы (хостинг, GitHub).
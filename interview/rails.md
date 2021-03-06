# Вопросы по Ruby on Rails с собеседований

1. Что такое ActiveRecord, и какие средства предоставляет для работы с обьектами?

    <details>
      <summary>Ответ</summary>
      ActiveRecord это паттерн программирования. AR является популярным способом доступа к данным реляционных баз данных в объектно-ориентированном программировании. ActiveRecord еще называют буквой M в MVC — которая является слоем в системе, ответственным за представление бизнес-логики и данных.

      Active Record упрощает создание и использование бизнес-объектов, данные которых требуют персистентного хранения в базе данных. Сама по себе эта реализация паттерна Active Record является описанием системы ORM (Object Relational Mapping). Active Record это фреймворк ORM.

      Active Record предоставляет нам несколько механизмов, наиболее важными из которых являются способности для:

      * Представления моделей и их данных.
      * Представления связей между этими моделями.
      * Представления иерархий наследования с помощью связанных моделей.
      * Валидации моделей до того, как они станут персистентными в базе данных.
      * Выполнения операций с базой данных в объектно-ориентированном стиле.

      Подробнее:

      * http://rusrails.ru/active-record-basics
      * https://dic.academic.ru/dic.nsf/ruwiki/1264999
    </details>

1. За что отвечают Model, View, Controller уровни в Rails?

    <details>
      <summary>Ответ</summary>
      MVC — это паттерн программирования, который подразумевает схему разделения данных приложения, пользовательского интерфейса и управляющей логики на три отдельных компонента.
    </details>

1. Как работает роутинг? Что такое ресурсные роуты? Как они формируются?

    <details>
      <summary>Ответ</summary>
      Браузеры запрашивают страницы от Rails, выполняя запрос по URL, используя определенный метод HTTP, такой как GET, POST, PATCH, PUT и DELETE.

      Роутинг распознает запрос по методу и по URL и направляет его в экшн контроллера или в приложение Rack.

      Он также может генерировать пути и URL, избегая необходимость жестко прописывать строки в ваших вьюхах.

      Ресурсный роутинг позволяет быстро объявлять все общие маршруты для заданного ресурсного контроллера. Вместо объявления отдельных маршрутов для экшнов index, show, new, edit, create, update и destroy, ресурсный маршрут объявляет их одной строчкой кода.

      http://rusrails.ru/rails-routing
    </details>

1. Как использовать `content_for` и `yield`?
1. Что такое скоупы (scopes)? Как использовать?
1. Что такое синглтон метод?
1. Что такое ActiveJob? Когда его использовать?
1. Что такое Asset Pipeline?
1. Что такое serializer и для чего он нужен? Где применяется? В чем его основная задача?
1. Что такое presenter и для чего он нужен? Где применяется? В чем его основная задача?
1. Что такое валидации? Как написать свои валидации? Для чего нужны валидации? Где применяются валидации? Примеры Валидаций.
1. Есть ли у Rails механизм, который отслеживает изменения в базе данных?
1. Что такое `Rack`?

    <details>
      <summary>Ответ</summary>
      https://www.8host.com/blog/kratkij-obzor-veb-serverov-dlya-prilozhenij-ruby/

      Rack это промежуточное программное обеспечение, оно делит входящие HTTP-запросы на различные этапы, затем обрабатывает их по частям, после чего посылает ответ веб-приложения (контроллера).

      Программа Rack  состоит из двух отдельных компонентов: обработчика и адаптера, с помощью которых происходит обмен данными между веб-серверами и приложениями (фреймворками).

      Какие серверы есть:

      * Phusion Passenger
      * Puma
      * Thin
      * Unicorn

      Как устроен Rack

      * https://www.youtube.com/watch?v=NJ-ilQMsqMs
      * https://www.youtube.com/watch?v=MHYMObuEahc
      * https://www.youtube.com/watch?v=DzrVB1-KyTU
    </details>

1. Что такое `partial` и для чего используются?

    <details>
      <summary>Ответ</summary>
      partial — это кусочек кода, который можно вынести в отдельный темплейт, для удобства использования и для использования в других представлениях.
    </details>

1. Что такое Haml, Slim? Какие плюсы на ваш взгляд, их использования?

    <details>
      <summary>Ответ</summary>
      Haml и Slim — это шаблонизаторы, используются для удобства использования и минимизации написания кода в представлениях. Сокращает в несколько раз написание кода, нет проблем в закрывании тегов, не получится что тег не закрыт и код не работает. Меньше вероятность что можно ошибиться + лучше читаемость в коде.

      http://slim-lang.com

      https://haml.ru
    </details>

1. Что означает несколько расширений файла example.html.erb?

    <details>
      <summary>Ответ</summary>
      **example** — название файла

      **html** — расширение, которое позволяет использовать стандартный язык разметки HyperText Markup Language

      **erb** — позволяет включить использование кода написанного на языке Ruby вместе с языком разметки
    </details>

1. Что такое ERB? Можете расшифровать аббревиатуру?

    <details>
      <summary>Ответ</summary>
      ERB — Embedded Ruby (встроенный Ruby)
    </details>

1. Знать и рассказать структуру папок Rails приложения.
1. Какие связи для связывания моделей в приложении Rails вы знаете?
1. Привести примеры использования `has_many`, `belongs_to`, `many_to_many`, `has_one`, `has_many :through`?
1. Что лучше выбрать `has_many :through` и `has_and_belongs_to_many`?
1. Что такое `pluralize` и как он может быть полезен на проекте?
1. Что такое `i18n` (интернационазиция)?
1. Что такое `dependent` связь?
1. Что такое `t.references`?
1. Как и чем проверить скорость работы методов? К примеру, что работает быстрее `each`, `proc` или `lambda`?
1. Что такое exception и от чего наследуется?
1. Как сгенерировать модель, конторллер, представление (вьюху)
1. Что такое scaffolding? Зачем он используется и где применяется?
1. Как реализовано кеширование в рельсах?
1. Представьте, что есть огромная табл. Users. Как можно перебрать ее элементы максимально быстро?

    <details>
      <summary>Ответ</summary>
      Быстро можно перебрать с помощью find_each, стандартно по 1000 записей.

      * `batch_size` — сколько обрабатывать записей за раз
      * `start` — с какого id к примеру продолжить работу
      * `finish` — может использоваться совместно с `start`, к примеру чтобы выслать письма только пользователям с первичным ключом от 2000 до 10000:

      https://apidock.com/rails/ActiveRecord/Batches/ClassMethods/find_each

      http://rusrails.ru/active-record-query-interface
    </details>

Где искать ответы:

* http://guides.rubyonrails.org/
* http://rusrails.ru/
* http://ruby-doc.org

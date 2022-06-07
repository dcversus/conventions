
# Технические соглашения
Yet another формат описания технических соглашений by Vasilisa Versus. Использую его, чтобы собрать знания о проекте в одном месте, итеративно проводить рефакторинг, онбоардить новых сотрудников и на его базе фасилитировать обсуждения. Ценность состоит из: подхода к тому как с этим документом работать и самой структуры, которая наследуется из проекта в проект.

## Структура
Каждое правило имеет следующую структуру
```md
## Название секции
Короткое описание секции, что к чему и почему. Если получится выразить в двух-трех тезисах, то идеально!

### Материалы
- [некая рекомендация №1](https://www.amazon.com/Clean-Code-Handbook-Software-Craftsmanship/dp/0132350882)
- [еще одна рекомендация](https://www.netflix.com/pt/title/81435684)
- [третья рекомендация](https://youtu.be/dQw4w9WgXcQ)

### Правила
<details>
  <summary>Правило 1</summary>
  
  Такие правила могут быть спойлерами, внутри которых немного мотивации и примеров
</details>

<details>
  <summary>Правило 2 под спойлером</summary>
  
  Если их не много, то это приемлемо, но вы можете оценить читаемость исходника 
  Еще ниже будет пример собранного документа, который можно копипастить
</details>

- Правило может быть и просто пунктом в списке
- [А еще лучше конечно сделать его ссылкой](/section1/rule4.md)

## Рецепты
<details>
  <summary>Как что-то сделать 1</summary>
  
  Гайд может быть прям очень длинным, включать графику и описания шагов
</details>

<details>
  <summary>Гайд на что-то</summary>
  
  Гайды конечно первые на разнесение в отдельные файлы
</details>

<details>
  <summary>Очередной пример</summary>

  Я лично организовывала такое через яндексовую вики, в гитхабвики и confluence
  Для большого проекта общее количество материалов было не больше 60 (около 2-3к строк)
  Для небольших около 20 (500 строк)
  Начинаю всегда с того чтобы держать в одном файле и разношу по мере необходимости.
</details>
```

## Как использовать
Коротко гайд для старта:
- Копипастим пример ниже в ваш проект или форкаем репу (или перенесите в вашу базу знаний, как удобнее, советую хранить с кодом)
- Проходимся сверху вниз и заполняем секции правил для текущего состояния проекта
- ЕСЛИ уже есть какие-то гайды, то собираем их в одном месте и причесываем. Если нет, то можно запланировать проработку хотя бы тех, которые есть в примере ниже
- Постепенно накапливаем материалы для рекомендаций и обновляем и актуализируем

Документ в худшем случае заводится и овнится одним человеком который контролирует проект и его состояние. Нужно прилагать усилия, чтобы вовлекать его развивать и поддерживать коллективно, это обязательное условие к использованию. Об этом можно много писать, но если коротко критично минимально на документе завязать несколько процессов: онбоардинг, код ревью и обсуждение подходов к разработке.

### Подходы к разработке с соглашениями
Интуитивно любые обсуждения к тому как работаем, будут вестись везде, где это только возможно, что ок, но постепенно будет накапливаться ощущение бесполезности усилий. Конструктивнее подталкивать коллег все фиксировать в некий единый источник истины - возник дискомфорт в работе? Что-то не нравится? Оформи минимально proposal в документ с соглашениями, мы его там на месте обсудим и примем. Сам процесс выслушивания, фиксации и принятия очень стимулирует того, кто столкнулся с чем-то в работе. Это критично важно.

Я предлагаю почаще подталкивать окружающих к тому, чтобы все мысли, идеи и проблемы максимально фиксировались. Нельзя допускать того, чтобы команда постоянно тонула в ощущении безысходности и существовала в страхе конфликта. Когда правила изложены в документе, то они обезличены, а значит можно оспаривать и предлагать что-то еще, без страха столкнуться с тем, что это адресно заденет и будет воспринято как что-то личное. Сравните с кейсом, когда в процессе код-ревью вам пишут `переименуй переменную, мы пишем в camelCase` VS `Мы пишем в camelCase [ссылка на правило]`. Точно также это касается и обсуждений в slack, если вы будете использовать документ как медиатор, то это снизит градус накала и позволит выстроить конструктивный диалог.

### Код-ревью с соглашениями
Изначально документ проектировался как гайд к код-ревью и решал проблему конфликтов в обсуждениях PR. Все соглашения можно разделить на те, которые можно автоматизировать и те, которые мы должны проверять об человека. 

Для начала стоит в целом определиться какую роль в вашем проекте играет код-ревью и зачем оно вам. Потом можно собрать основные замечания которые вы там встречаете и выписать их в этом документе. 

Я предлагаю кидать ссылку при ревью на доку в ситуациях типовых проблем. Если кто-то не согласен с этим подходом, то в рамках задачи делает в соотв. с документом, но дальше предлагает изменить документ.

### Онбоардинг с соглашениями
Если вы часто нанимаете и типовым образом погружаете людей в проект, то гайд со схожей структурой у вас образуется сам собой. Я рекомендую исходить из объяснения того, как решается несколько типовых задач. А также дополнительно показать как именно эти соглашения можно менять, можно вовлечь на частном примере или показать историю изменений файла/обсуждения. Уверяю, что это сыграет очень сильную роль в будущем новичка в вашем проекте.

В дальнейшем, первые недели данный документ станет частым местом для CTRL+F новичка в вашем проекте. По моим наблюдениям погружение можно снизить с 2-4 недель до нескольких дней благодаря такому документу (или иному единственному источнику истинны).

# Пример соглашений
Я распишу несколько разделов для ознакомления, оставляя все в виде списков без детализации. 

## Структура
Самый сложный раздел, для каждого проекта полностью специфичен.

Если у вас новый проект на реакте возьмите и сошлитесь здесь на [FSD](https://github.com/feature-sliced/documentation), если angular то строго используйте [официальные](https://angular.io/guide/file-structure) [гайдлайны](https://angular.io/guide/architecture).

Если старый проект, то приложите сюда [граф импортов проекта](https://github.com/pahen/madge). Опишите типовые элементы системы, напр. компоненты/страницы/сервисы и для каждого опишите зачем он нужен, как устроен. Опишите структуру директорий. Это минимально.

### Материалы 
- https://feature-sliced.design/
- https://ru.hexlet.io/courses/js-frontend-architecture
- https://www.youtube.com/watch?v=VegNqfiS6k8

### Правила
- Все вне директории legacy должно полностью следовать FSD 
- Файлы и директории строго именуем в snake_case
- Любые helpers / utils файлы вне common запрещены

### Рецепты
- Как создать типовой UI компонент
- Добавляем новую страницу
- Как сделать свой хук

## Зависимости
### Рецепты
- Как добавить новый пакет
- Изменение размера бандла, как оценить с новой зависимостью

### Правила
- Добавление новой зависимости вместе с продуктовым PR запрещено, добавляем отдельным предварительным PR и согласуем с лидом
- Добавление depricated авторами зависимостей запрещено
- Запрещено добавлять дублирующие зависимости
- Новый пакет обязательно должен поставляться в виде es module

## Компоненты
При написании react-компонентов мы предпочитаем писать компоненты с помощью функций, а для вынесения частей бизнес кода хуки или чистые функции. 

### Материалы
- https://ru.reactjs.org/docs/hooks-intro.html
- https://jaketrent.com/post/naming-event-handlers-react

### Рецепты
- Пишем сториз для сторибука
- Разметка для трекеров. Аналитика
- Экспорт иконок из Figma
- Добавляем растровые картинки
- Замеряем ререндеры компонента

### Правила
- Любой новый UI компонент должен содержать сториз
- Запрещен закомментированный код
- Запрещены console.log или любой код для отладки
- Работа с асинхронными операциями используем только async/await
- Распаралеливаем запросы там где это возможно
- Код, кроме реекспорта, в index.ts файлах запрещен
- Запрещено передавать неиспользуемые пропсы
- Запрещены default экспорты
- Бразуерное апи должно вызываться только внутри useLayoutEffect
- Правила eslint запрещено отключать

## Стили
Мы используем css-modules всегда, глобальные стили запрещены. Используем общие миксины там где это возможно. Мы используем CSS Custom Properties, а все доступные переменные с дизайн-токенами можно посмотреть в локально развернутом сторибуке. Эти переменные доступны глобально: для их использования не нужно ничего импортировать.

### Материалы
- https://andrew-r.ru/notes/bem-vs-css-modules/
- https://ru.bem.info/methodology/css/
- https://css-tricks.com/the-shapes-of-css/
- https://alligator.io/css/currentcolor/
- https://ishadeed.com/article/css-color/

### Рецепты
- Какие миксины у нас есть и как их используем
- Добавляем новый миксин

### Правила
- Разрешен только один файл стилей на директорию
- Запрещена адаптивность посредством media запросов (используем js вместо этого)
- Везде где можно используем дизайн токены
- Корневой элемент всегда именуем root
- Глобальные стили строго запрещены
- Используем currentColor для цвета svg иконок
- Правила stylelint запрещено отключать

## Работа с данными
Используем redux в связке с redux-toolkit. Само хранилище описано и собирается в /store нашего проекта, есть “общая часть” в /store /general. Бизнес части описываются в слайсах в рамках фич. Общая часть строго не зависит от слайсов.

### Рецепты
- Как добавить новый слайс

### Правила
- перед инициализация нужно обязательно ресетить стейт
- импортировать хранилище разрешено только в страницах и фичах

## Сеть
Сервис - абстракция для работы с данными. Сервисы могут работать с аналитикой, нашим api или предоставлять интерфейс доступа к иным данным (например маппинг роутинга).

Сервис состоит из файла с методами (имя сервиса) и адаптера. Адаптер содержит в себе методы преобразования полученных данных, его наличие обязательно если вы собираетесь как-то изменить полученные с сервера данные перед тем как разместить их в нашем сторе.

Для сервиса который работает с сетью также обязательно наличие мок реализации, это необходимо для корректной работы блоков в сторибуке.

### Рецепты
- Разработка сервиса
- Реализуем мок

### Правила
- Адаптер imgproxy обязателен если в ответе есть url графики
- Наличие мок реализации обязательно

## Обработка ошибок
### Рецепты
- Правильно реагируем на сетевые ошибки в интерфейсе

### Правила
- Запрещено заглушать ошибки, интерфейс должен реагировать на них
- Наличие непредсказуемых ошибок в консоли запрещено

## Доступы
### Рецепты
- Как ограничить доступ к роуту
- Скрываем виджет или блок в зависимости от ролей
- Добавляем новую роль пользователя
- Как посмотреть страницу с другим набором ролей

### Правила
- При работе с ролями используем только хук usePermission, напрямую обрабатывать обьект пользователь запрещено

## Дебаг
### Рецепты
- Как смотреть ошибки в sentry
- Как смотреть логи
- Где смотрим графики и что они значат
- Деплой хотфикса

## Секреты
### Рецепты
- Добавляем новый секрет

### Правила
- Все секреты должны быть в vault

## Тенанты
### Рецепты
- Какой бывает специфика в разных деплоях
- Брендируем стили
- Добавляем специфичный виджет в тенант

## I18N
У нас нет локализаций. Тексты размещаются inline.

### Правила
- в UI компонентах строки запрещены, все текста передаются пропсами

## A11Y
Мы стремимся делать интерфейс доступным. A11y. Цели покрывать весь интерфейс доступностью - нет, но базовые вещи уже нужно начинать делать. Например следует использовать семантические HTML-элементы там, где возможно.
### Материалы по теме
- https://www.sberbank.ru/ru/person/specialbank/digitalguide
- https://a11yproject.com/
- https://a11y-style-guide.com/style-guide/
- https://www.sarasoueidan.com/blog/keyboard-friendlier-article-listings/
- https://www.youtube.com/watch?v=KAK-WAb9vow
- https://www.24a11y.com/2018/accessible-svg-icons-with-inline-sprites/
- https://www.w3schools.com/html/html5_semantic_elements.asp
- https://www.freecodecamp.org/news/semantic-html5-elements/
- https://cloudfour.com/thinks/autofill-what-web-devs-should-know-but-dont/
- https://developer.mozilla.org/en-US/docs/Web/HTML/Attributes/autocomplete

### Рецепты
- Как кастомный компонент сделать на базе нативного аналога
- Как сделать доступную модалку

### Правила
- aria-label, aria-disabled и tabIndex должны быть размещены по возможности везде где это требуется
- Inline-компоненты (ссылки, лейблы, ...) не должны иметь размер шрифта
- Интерактивные компоненты (инпуты, кнопки, ...) должны иметь стили для :hover, :active, :focus и :disabled
- Интерактивные компоненты (инпуты, кнопки, ...) должны иметь обводку при :focus
- Интерактивные компоненты (инпуты, кнопки, ...) должны иметь cursor: pointer по умолчанию и cursor: defaultв состоянии :disabled.
- SVG-иконки должны быть доступными
- Для подтверждения формы использовать событие onSubmit, для отмены/очистки - использовать событие onReset
- Используем по возможности autoFocus
- Блокируем фокус в рамках модальных окон
- Для кнопок используем <button>, для ссылок <a>

## SEO
### Материалы
- https://habr.com/en/post/282880/

### Рецепты
- Прогононяем демостенд в lighthouse

### Правила
- Внешние ссылки обязаны содержать `rel="noopener noreferrer"`

## A/B-тестирование и feature-флаги
Для раскатки функционала для части пользователей у нас есть два механизма: фичефлаги и AB-тесты.
  
Примерное правило для выбора между ними: если есть АБ-тест, то разработку следует делать через него. Если АБ- теста нет или он закончился – фичефлаг.

При этом обычно AB-тесты – инструмент аналитиков и продакт-менеджеров/продакт-овнеров, и инициатива разработки через AB-тестирование исходит от них. Фичефлаги используются, например, если требуется выкатить какой-нибудь функционал (или часть функционала) на прод, но чтоб у пользователей не было к нему доступа, или для постепенной выкатки функционала после завершения АБ-теста.
  
### Материалы
- https://habr.com/en/post/282880/

### Рецепты
- Разработка с использованием эксперимента
- Заводим флаг в flipper

### Правила
- Фичефлаг должен иметь префикс вида tckt-XXXX-* и ссылаться на конкретный тикет в jira описывающий поведение флага

## Автотестирование
### Рецепты
- Добавляем data-qa-id
- Пишем e2e тест
- Пишем unit тест
- Новый скриншотный тест
- Обновляем скриншотные тесты

### Правила
- Если обновлены UI компоненты обязательно обновляем сторишоты


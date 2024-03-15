# Вывод дерева метаданных конфигурации 1С и открытие модулей в VSC

[Дальнейшие планы (roadmap)](#что-ещё-планируется-roadmap)

## Возможности расширения

* Расширение ищет в открытой папке пары файлов ConfigDumpInfo.xml и Configuration.xml (для XML формата) и файл Configuration.mdo (для EDT формата) выгруженных конфигураций 1С и для каждого варианта строит дерево метаданных в панели VS Code. Для задания глубины просмотра подкаталогов существует настройка "Search Depth". По умолчанию значение настройки равно трём. **Особенно важной эта настройка становится для формата EDT [см.статью в wiki](https://github.com/zerobig/vscode-1c-metadata-viewer/wiki/%D0%9D%D0%B5-%D0%BD%D0%B0%D1%85%D0%BE%D0%B4%D0%B8%D1%82-%D0%BF%D1%80%D0%BE%D0%B5%D0%BA%D1%82-%D0%B2-%D1%84%D0%BE%D1%80%D0%BC%D0%B0%D1%82%D0%B5-EDT)**
* Открывает текстовые модули 1С (*.bsl) через контекстное меню у соответствующих элементов.
* У метаданных для которых есть возможность создания предопределенных элементов можно открыть панель существующих в конфигурации элементов.

![Скриншот дерева метаданных](/resources/screenshot_0.png)

* Открывает формы объектов и табличные документы в режиме просмотра.

![Скриншот предпросмотра формы](/resources/screenshot_2.png)
![Скриншот табличного документа](/resources/screenshot_1.png)

## Метаданные и модули

### Метаданные:

<details>
  <summary>Развернуть</summary>

  * Подсистемы
  * Параметры сеанса
  * Роли
  * Общие реквизиты
  * Планы обмена
  * Подписки на события
  * Регламентные задания
  * Общие формы
  * Web-сервисы
  * Http-сервисы
  * WS-ссылки
  * Стили
  * Константы
  * Справочники
  * Документы
  * Журналы документов
  * Перечисления
  * Отчеты
  * Обработки
  * Планы видов характеристик
  * Планы счетов
  * Планы видов расчета
  * Регистры сведений
  * Регистры накопления
  * Регистры бухгалтерии
  * Регистры расчета
  * Бизнес-процессы
  * Задачи
  * Внешние источники данных

</details>

### Модули:

<details>
  <summary>Развернуть</summary>

  * Модуль приложения
  * Модуль сеанса
  * Общий модуль
  * Модуль объекта
  * Модуль менеджера
  * Модуль формы
  * Модуль команды
  * Модуль записи
  * Модуль менеджера значения (для констант)

</details>

## Что ещё планируется (roadmap)

- [x] Работа с форматом выгрузки EDT - [#3](https://github.com/zerobig/vscode-1c-metadata-viewer/issues/3)
- [ ] Возможность чтения метаданных без файла ConfigDumpInfo.xml
- Предпросмотр форм:
  - [ ] Поле radio button
  - [ ] Поле декорации (картинка)
  - [ ] Рефакторинг поля ввода - кнопки, обязательность заполнения и т.д.
  - [ ] Наполнение командных панелей форм и табличных частей
  - [ ] Просмотр свойств элементов форм
  - [ ] Возможность просмотра событий привязанных к элементам форм и переход на процедуры модуля формы
  - [ ] Дальнейшая работа над внешним видом форм. Выравнивание и т.д.
- [ ] Интеграция элементов дерева с данными об ошибках в связанных модулях - [#6](https://github.com/zerobig/vscode-1c-metadata-viewer/issues/6)
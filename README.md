# Вывод дерева метаданных конфигурации 1С и открытие модулей в VSC

Расширение анализирует файл ConfigDumpInfo.xml выгруженной конфигурации 1С и строит дерево метаданных в панели VS Code.

![Скриншот дерева метаданных](/resources/screenshot.png)

Открывает текстовые модули 1С (*.bsl) через контекстное меню у соответствующих элементов.

## Метаданные и модули

### Типы метаданных

* Константы
* Справочники
* Документы
* Перечисления
* Отчеты
* Обработки
* Регистры сведений
* Регистры накопления

### Модули

* Модуль приложения
* Модуль сеанса
* Общий модуль
* Модуль объекта
* Модуль менеджера
* Модуль формы
* Модуль команды
* Модуль записи
* модуль менеджера значения (для констант)

## Что ещё планируется

* Расширение количества обрабатываемых типов метаданных
* Открытие модуля без контекстного меню по двойному щелчку когда модуль у элемента конфигурации один
* Редактирование свойств метаданных в отдельной панели
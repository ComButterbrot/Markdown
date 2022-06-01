# **Контрол "Таблица" (class Controls/grid:View)** #

**В этой статье:**
- Иерархия контрола "Таблица"
- Пример таблицы
- Опции
- Поля
- Методы
- События
- Полезные ссылки

**Иерархия контрола "Таблица":**
- модуль **[Controls](https://wasaby.dev/docs/js/Controls?v=22.4100)** - готовый набор визуальных компонентов, отвечающих корпоративным стандартам и позволяющих быстро спроектировать визуальную составляющую веб-приложения;
- библиотека **[Controls/grid](https://wasaby.dev/docs/js/Controls/grid?v=22.4100)** - библиотека контролов, которые реализуют плоский список, отображающийся в форме таблицы;
- класс **Controls/grid:View** - контрол "Таблица", позволяющий отображать данные из различных источников в виде таблицы.

**Пример таблицы**

|**id**|**Фамилия**| **Имя** |**Город**|
|:-----|:----------|:--------|:--------|
|  1   |  Иванов   | Иван    | Москва  |
|  2   |  Петров   | Пётр    | Москва  |
|  3   |  Сергеев  | Сергей  |  Тула   |
|  4   | Григорьев | Дмитрий | Кострома|
|  5   |  Викторов | Виктор  | Иваново |

**Опции**

Опции - это объекты, в которых хранятся параметры, переданные при инициализации контрола. Опции доступны только на чтение, и менять их можно только через родительский контрол. Изменение объекта опций подобно изменению аргументов, переданных в функцию. Подробнее про опции можно прочитать в соответствующей [статье](https://wasaby.dev/doc/platform/ui-library/options/).

Примеры использования опций:

- [draggingTemplate](https://wasaby.dev/docs/js/Controls/grid/View/options/draggingTemplate/?v=22.3100#option) (шаблон перемещения элементов, интерфейс IDraggable), использование базового шаблона перемещения элементов:
    
        <!-- WML -->
        <Controls.list:View
            source="{{_viewSource}}"
            keyProperty="id"
            on:dragStart="_onDragStart()"
            itemsDragNDrop="{{true}}">
            <ws:draggingTemplate>
                <ws:partial template="Controls/dragnDrop:DraggingTemplate"
                    mainText="{{draggingTemplate.entity.getOptions().mainText}}"
                    image="{{draggingTemplate.entity.getOptions().image}}"
                    additionalText="{{draggingTemplate.entity.getOptions().additionalText}}">
                </ws:partial>
            </ws:draggingTemplate>
        </Controls.list:View>
    
        // JavaScript
        _viewSource: null,
        _onDragStart: function(event, items) {
            var mainItem = this._items.getRecordById(items[0]);
            return new Entity({
                items: items,
                mainText: mainItem.get('FIO'),
                additionalText: mainItem.get('title'),
                image: mainItem.get('userPhoto')
            });
        },
        _beforeMount: function() {
        this._viewSource= new Source({...});
        }

- [excludedKeys](https://wasaby.dev/docs/js/Controls/grid/View/options/excludedKeys/?v=22.3100#option) (набор ключей исключенных элементов, интерфейс IPromisedSelectable), создание списка и выбор всех элементов, кроме двух:
    
        <!-- WML -->
        <Controls.operations:Controller
            bind:selectedKeys="_selectedKeys"
            bind:excludedKeys="_excludedKeys" />
    
        // JavaScript
        _selectedKeys: null,
        _excludedKeys: null,
        _beforeMount: function() {
            this._selectedKeys = [null];
            this._excludedKeys = [1, 2];
        }

- [filter](https://wasaby.dev/docs/js/Controls/grid/View/options/filter/?v=22.3100#option) (конфигурация объекта фильтра, интерфейс IFilter), отображение в списке двух элементов на основании конфигурации объекта фильтра:
    
        <!-- WML -->
        <Controls.list:View
            keyProperty="id"
            filter="{{_filter}}"
            source="{{_source}}" />
    
        // JavaScript
        this._filter = {id: ['1', '2']};
        this._source = new Memory({
            keyProperty: 'id',
            data: [
                {
                    id: '1',
                    title: 'Yaroslavl'
                },
                {
                    id: '2',
                    title: 'Moscow'
                },
                {
                    id: '3',
                    title: 'St-Petersburg'
                }
            ]
        });

Список опций контрола "Таблица" в формате "Опция - Назначение - Интерфейс" доступен по [ссылке](https://wasaby.dev/docs/js/Controls/grid/View#option).

**Поля**

Поле является переменной, объявленной непосредственно в контроле. В зависимости от типа требуемых данных поля подразделяются на:
- текстовые;
- числовые;
- поля ввода даты и времени;
- специализированные.

Значение поля устанавливается опцией [value](https://wasaby.dev/docs/js/Controls/input/Text/options/value/?v=22.4100):
    
    // TypeScript
    export default class extends Control {
        protected _template: TemplateFunction = Template;
        protected myText: "Hello, world!";
    }
    
    <!-- WML -->
    <Controls.input:Text bind:value="myText" />

Список полей контрола "Таблица" в формате "Поле - Назначение - Класс" доступен по [ссылке](https://wasaby.dev/docs/js/Controls/grid/View#field).

**Методы**

Метод - это функция или процедура, принадлежащая какому-либо классу или объекту. Метод состоит из некоторого количества операторов для выполнения определённой задачи и работы с аргументами. В зависимости от уровня доступа выделяют следующие методы:
- открытый (public);
- защищённый (protected);
- закрытый (private).

Примеры методов:

- [afterMount](https://wasaby.dev/docs/js/Controls/grid/View/methods/_afterMount/?v=22.3100) (protected, хук жизненного цикла контрола). Параметры: options (опции контрола), context (поле контекста, запрошенное контролом). Возвращает: void.

- [beginEdit](https://wasaby.dev/docs/js/Controls/grid/View/methods/beginEdit/?v=22.3100#field) (public, редактирование по месту). Параметры: options (опции контрола). Возвращает: Controls/_baseList/interface/IEditableList/TAsyncOperationResult.typedef. Пример:
    
        <!-- WML -->
        <Controls.list:View name="list" />
    
        // JavaScript
        foo: function() {
            this._children.list.beginEdit({
                item: this._items.at(0)
            });
        }

- [loadCSS](https://wasaby.dev/docs/js/Controls/grid/View/methods/loadCSS/?v=22.3100#field) (public, загрузка стилей и тем контрола). Параметры: themeName (имя темы), themes (массив тем для скачивания), styles (массив стилей для скачивания). Возвращает: Promise<void>. Пример:
    
        import('Controls/_popupTemplate/InfoBox')
        .then((InfoboxTemplate) => InfoboxTemplate.loadCSS('saby__dark'))
    
Список методов контрола "Таблица" в формате "Метод - Назначение - Класс/Интерфейс" доступен по [ссылке](https://wasaby.dev/docs/js/Controls/grid/View#method).

**События**

Событие - это сообщение, которое возникает в различных точках исполняемого кода при выполнении определённых условий. События предназначены для определения реакции программного обеспечения.

Список событий контрола "Таблица" в формате "Событие - Назначение - Интерфейс" доступен по [ссылке](https://wasaby.dev/docs/js/Controls/grid/View#event).

**Полезные ссылки:**
- [Руководство разработчика](https://wasaby.dev/doc/platform/controls/list/)
- [Свойства и опции](https://wasaby.dev/doc/platform/ui-library/options/)
- [Поля ввода](https://wasaby.dev/doc/platform/controls/input-elements/input/)


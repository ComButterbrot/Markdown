# **Контрол "Таблица" (class Controls/grid:View)** #

**В этой статье:**
- [Иерархия контрола "Таблица"](https://github.com/ComButterbrot/Markdown/blob/main/T3%20-%20View.md#:~:text=%D0%98%D0%B5%D1%80%D0%B0%D1%80%D1%85%D0%B8%D1%8F%20%D0%BA%D0%BE%D0%BD%D1%82%D1%80%D0%BE%D0%BB%D0%B0%20%22%D0%A2%D0%B0%D0%B1%D0%BB%D0%B8%D1%86%D0%B0%22%3A)
- [Пример таблицы](https://github.com/ComButterbrot/Markdown/blob/main/T3%20-%20View.md#:~:text=%D0%B2%20%D0%B2%D0%B8%D0%B4%D0%B5%20%D1%82%D0%B0%D0%B1%D0%BB%D0%B8%D1%86%D1%8B.-,%D0%9F%D1%80%D0%B8%D0%BC%D0%B5%D1%80%20%D1%82%D0%B0%D0%B1%D0%BB%D0%B8%D1%86%D1%8B)
- [Опции](https://github.com/ComButterbrot/Markdown/blob/main/T3%20-%20View.md#:~:text=%D0%98%D0%B2%D0%B0%D0%BD%D0%BE%D0%B2%D0%BE-,%D0%9E%D0%BF%D1%86%D0%B8%D0%B8,-%D0%9E%D0%BF%D1%86%D0%B8%D0%B8%20%2D%20%D1%8D%D1%82%D0%BE%20%D0%BE%D0%B1%D1%8A%D0%B5%D0%BA%D1%82%D1%8B)
- [Поля](https://github.com/ComButterbrot/Markdown/blob/main/T3%20-%20View.md#:~:text=%D0%BF%D0%BE%20%D1%81%D1%81%D1%8B%D0%BB%D0%BA%D0%B5.-,%D0%9F%D0%BE%D0%BB%D1%8F,-%D0%9F%D0%BE%D0%BB%D0%B5%20%D1%8F%D0%B2%D0%BB%D1%8F%D0%B5%D1%82%D1%81%D1%8F%20%D0%BF%D0%B5%D1%80%D0%B5%D0%BC%D0%B5%D0%BD%D0%BD%D0%BE%D0%B9)
- [Методы](https://github.com/ComButterbrot/Markdown/blob/main/T3%20-%20View.md#:~:text=%D0%BF%D0%BE%20%D1%81%D1%81%D1%8B%D0%BB%D0%BA%D0%B5.-,%D0%9C%D0%B5%D1%82%D0%BE%D0%B4%D1%8B,-%D0%9C%D0%B5%D1%82%D0%BE%D0%B4%20%2D%20%D1%8D%D1%82%D0%BE%20%D1%84%D1%83%D0%BD%D0%BA%D1%86%D0%B8%D1%8F)
- [События](https://github.com/ComButterbrot/Markdown/blob/main/T3%20-%20View.md#:~:text=%D0%BF%D0%BE%20%D1%81%D1%81%D1%8B%D0%BB%D0%BA%D0%B5.-,%D0%A1%D0%BE%D0%B1%D1%8B%D1%82%D0%B8%D1%8F,-%D0%A1%D0%BE%D0%B1%D1%8B%D1%82%D0%B8%D0%B5%20%2D%20%D1%8D%D1%82%D0%BE%20%D1%81%D0%BE%D0%BE%D0%B1%D1%89%D0%B5%D0%BD%D0%B8%D0%B5)
- [Полезные ссылки](https://github.com/ComButterbrot/Markdown/blob/main/T3%20-%20View.md#:~:text=%D0%BF%D0%BE%20%D1%81%D1%81%D1%8B%D0%BB%D0%BA%D0%B5.-,%D0%9F%D0%BE%D0%BB%D0%B5%D0%B7%D0%BD%D1%8B%D0%B5%20%D1%81%D1%81%D1%8B%D0%BB%D0%BA%D0%B8%3A,-%D0%A0%D1%83%D0%BA%D0%BE%D0%B2%D0%BE%D0%B4%D1%81%D1%82%D0%B2%D0%BE%20%D1%80%D0%B0%D0%B7%D1%80%D0%B0%D0%B1%D0%BE%D1%82%D1%87%D0%B8%D0%BA%D0%B0)

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

Другие примеры доступны по [ссылке](https://wasaby.dev/docs/js/Controls/grid/View#examples).

**Опции**

Опции - это объекты, в которых хранятся параметры, переданные при инициализации контрола. Опции доступны только на чтение, и менять их можно только через родительский контрол. Изменение объекта опций подобно изменению аргументов, переданных в функцию. Подробнее про опции можно прочитать в соответствующей [статье](https://wasaby.dev/doc/platform/ui-library/options/).

Примеры использования опций:

- [draggingTemplate](https://wasaby.dev/docs/js/Controls/grid/View/options/draggingTemplate/?v=22.3100#option) (шаблон перемещения элементов, интерфейс [IDraggable](https://wasaby.dev/docs/js/Controls/interface/IDraggable?v=22.3100)), использование базового шаблона перемещения элементов:
    
        <!-- WML -->
        <Controls.list:View
            source="{{_viewSource}}"
            keyProperty="id"
            on:dragStart="_onDragStart()"
            itemsDragNDrop="{{true}}">
            <ws:draggingTemplate> //использование опции draggingTemplate
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

- [excludedKeys](https://wasaby.dev/docs/js/Controls/grid/View/options/excludedKeys/?v=22.3100#option) (набор ключей исключенных элементов, интерфейс [IPromisedSelectable](https://wasaby.dev/docs/js/Controls/interface/IPromisedSelectable?v=22.3100)), создание списка и выбор всех элементов, кроме двух:
    
        <!-- WML -->
        <Controls.operations:Controller
            bind:selectedKeys="_selectedKeys"
            bind:excludedKeys="_excludedKeys" />
    
        // JavaScript
        _selectedKeys: null,
        _excludedKeys: null,
        _beforeMount: function() {
            this._selectedKeys = [null];
            this._excludedKeys = [1, 2]; //параметры выборки (указание порядковых номеров исключаемых элементов)
        }

- [filter](https://wasaby.dev/docs/js/Controls/grid/View/options/filter/?v=22.3100#option) (конфигурация объекта фильтра, интерфейс [IFilter](https://wasaby.dev/docs/js/Controls/interface/IFilter?v=22.3100)), отображение в списке двух элементов на основании конфигурации объекта фильтра:
    
        <!-- WML -->
        <Controls.list:View
            keyProperty="id"
            filter="{{_filter}}"
            source="{{_source}}" />
    
        // JavaScript
        this._filter = {id: ['1', '2']}; //параметры выборки (указание id требуемых элементов)
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
    
    <!-- WML -->
    <Controls.input:Text bind:value="myText" /> //определение значения поля опцией value
    
    // TypeScript
    export default class extends Control {
        protected _template: TemplateFunction = Template;
        protected myText: "Hello, world!";
    }

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
    
Примеры событий:

- [dragStart](https://wasaby.dev/docs/js/Controls/grid/View/events/dragEnter/?v=22.4100#method) (происходит при начале перемещения элемента, интерфейс [IDraggable](https://wasaby.dev/docs/js/Controls/interface/IDraggable?v=22.3100)), перемещение в список объектов определённого типа:
    
        <!-- WML -->
        <Controls.list:DataContainer source="{{_firstSource}}" keyProperty="id">
            <Controls.list:View
                on:dragStart="_dragStart()"
                itemsDragNDrop="{{true}}" />
        </Controls.list:DataContainer>
        <Controls.list:DataContainer source="{{_secondSource}}" keyProperty="id">
            <Controls.list:View
                on:dragEnter="_dragEnter()"
                itemsDragNDrop="{{true}}" />
        </Controls.list:DataContainer>
    
        // JavaScript
        _dragStart: function(event, items) {
            return new TasksItemsEntity({
                items: items
            });
        },
        _dragEnter: function(event, entity) {
            var result = false;
            if (entity instanceof TasksItemsEntity) {
                result = new Record({...});
            }
            return result;
        },
        _beforeMount: function() {
            this._firstSource = new Source({...});
            this._secondSource = new Source({...});
        }
    
- [filterChanged](https://wasaby.dev/docs/js/Controls/grid/View/events/filterChanged/?v=22.4100#method) (происходит при изменении фильтра, интерфейс [IFilterChanged](https://wasaby.dev/docs/js/Controls/interface/IFilterChanged/?v=22.4100)), изменение фильтра:
    
        <!-- WML -->
        <Controls.filter:Controller on:filterChanged="filterChanged()" filter="{{ _filter }}"/>
        {{ _filterString }}

        // JavaScript
        _filter: null,
        _beforeMount: function() {
            this._filter = {
                city: 'Yaroslavl'
            }
        },
        filterChanged: function(e, filter) {
            this._filter = filter; //самостоятельное обновление фильтра по причине отсутствия связи между опцией filter и состоянием
            this._filterString = JSON.stringify(this._filter, null, 4);
        }
    
- [selectedKeysChanged](https://wasaby.dev/docs/js/Controls/grid/View/events/selectedKeysChanged/?v=22.4100#method) (происходит при изменении набора выбранных элементов списка, интерфейс [IPromisedSelectable](https://wasaby.dev/docs/js/Controls/interface/IPromisedSelectable/?v=22.4100)), привязка обновлений при изменении selectedKeys:
    
        <!-- WML -->
        <Controls.operations:Controller on:selectedKeysChanged="onSelectedKeysChanged()" bind:selectedKeys="_selectedKeys" bind:excludedKeys="_excludedKeys">
        <Controls.operations:Panel source="{{ _panelSource }} />
        </Controls.operations:Controller>
                                       
        // JavaScript
        _beforeMount: function() {
            this._selectedKeys = [];
            this._excludedKeys = [];
        },
        onSelectedKeysChanged: function(e, selectedKeys, added, deleted) {
            this._panelSource = this._getPanelSource(selectedKeys); //состояние не требует обновления вручную по причине привязки
        }                                   
    
Список событий контрола "Таблица" в формате "Событие - Назначение - Интерфейс" доступен по [ссылке](https://wasaby.dev/docs/js/Controls/grid/View#event).

**Полезные ссылки:**
- [Руководство разработчика](https://wasaby.dev/doc/platform/controls/list/)
- [Свойства и опции](https://wasaby.dev/doc/platform/ui-library/options/)
- [Поля ввода](https://wasaby.dev/doc/platform/controls/input-elements/input/)


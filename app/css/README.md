Директории и файлы LESS
===============

Внутри симантической директори лучше всего создавать файлы (модули) с префиксом семантичской директории. Пример создания блока с приветствием: box/box-intro.less.

Внутри отдельных модулей box, nav, form и т.д. можете писать, как считаете нужным, однако, один файл - один модуль.

box-intro.less: 

```less
.box-intro {
  background: #dedede;
  padding: 10px;
  h1 {
    font-size: 40px;
  }
  p {
    margin: 2em 0;
  }
}
```



## Директории

* *box* - функциональный блок, такой как "Один журнал", "сниппет товара" и т.д.  
* *elem* - повторяющийся элемент в разных блоках, формах, да где угодно. Примеры элемента "рейтинг", "показать все"  
* *form* - форма  
* *icons* - иконки на сайта  
* *bootstrap* - переопределяется базовый бутстрап. Тут формируется структура и адаптируются элементы основного бутстрапа  
* *list* - списки. Списки новостей, вакансий, да всего чего угодно, что можно вывести списком  
* *nav* - подраздел списков, очень большой. Поэтому для них выделена отдельная директирия  
* *plugins* - стили для разнообразных плагинов на сайте

Конечно же, корневых директорий может быть сколько угодно и создаваться под любые нужды, к примеру:
* *page* - страницы с уникальным дизайном и оформлением
* *gallery* - галереи. Можно сюда засунуть и слайдер
* *modal* - виды модальных окон
* ....


### Корневые файлы
* *styles.less* - тут подключается весь набор стилей. Больше ничего тут не писать
* *styles.css* - расходник. Ничего сюда не писать
* *styles.css.map* - мапа для стилей
* *hacks.less* (отсутствует по умолчанию) - хаки для браузеров. Все хаки писать тут.

### Директория css/system

Если вы, по какой-то причине не стали устанавливать Bootstrap, то будет создана эта директория. В ней будут содежраться:

* variables.less - переменные для проекта
* mixins.less (пусто)- миксины
* structure.less (пусто) - файл для подключения сетки
* type.less (пусто) - переопределение базовых тегов
* utilities.less (пусто) - дополнительные классы, которые могут понадобиться в верстке. Смотреть Bootstrap.


### Файлы _.less

Эти файлы импорта в основной файл less. Писать туда ничего не надо, так как одновляются они автоматически, когда создаются или удаляются файлы в этой директории


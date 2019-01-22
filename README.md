# GoodCar.rent project docs

Car rent management app (WIP, not ready yet)

## Documentation

* System: 
    * [models](system/system-models.md)
    * [API](system/system-api.md)
* Domain-specific:
    * [models](domain-specific/domain-models.md)
    * [API](domain-specific/domain-api.md)

----

# User Stories

## Регистрация пользователя

Пользователь создает аккаунт на сервисе через форму регистрации, вносит необходимые данные в поля форм, прикрепляет фото документов и отправляет анкету на проверку.

Система проверяет анкету, и отправляет пользователю уведомление о готовности его аккаунта к работе.

## Поиск бронирования

Пользователь заходит на сайт системы и вводит данные в форму поиска: где нужен автомобиль, с какой даты и по какую.

Система выдает список автомобилей, доступных на выбранную дату.

Пользователь использует фильтры для настройки списка: выбирает класс автомобиля, тип трансмиссии и другие опции.

После выбора автомобиля система предлагает пользователю забронировать его, укомплектовав дополнительными опциями: детское кресло, доп водитель, и тп.

Пользовтаель выбирает место передачи, 

## Dev

Обработка запроса на бронирование:

* фильтруем записи о машинах: получаем перечень машин, потенциально доступных для бронирования в заданном регионе;

* для каждой машины получаем записи о бронировании в указанный временной период - дата бронирования от начальной даты, или дата окончания меньша начальной даты: смотрим количество таких записей. Если записей нет - то машина доступна.


## Future ideas

Управление техническим обслуживанием автомобилей

# LT-TakeSim
### Мобильный сервис по заказу сим-карт.
- Приложение позволяет выбрать красивый номер телефона
- Найти выгодный тариф
- Оформить E-Sim
- Заказать доставку в любой город России.
### Приложение доступно в Google Play по [ссылке](https://play.google.com/store/apps/details?id=com.kifmellow.lider_telecom).


## Реализовано REST API для взаимодействия с базой данных.

- Пример POST-запроса на адрес http://takesim.pythonanywhere.com/api/order/ для оформления заявки: 
```
{
    "sim_iccid": "0000000099",
    "cdek": "г. Москва, Куйбышевская, 9",
    "fio": "Артемьева Ангелина Александровна",
    "type": "ESim"
}
```

Пример ответа:

```
{
    "id": 1689562358,
    "sim_iccid": "0000000099",
    "cdek": "г. Москва, Куйбышевская, 9",
    "fio": "Артемьева Ангелина Александровна",
    "type": "ESim",
    "status": "NEW",
    "create_date": "2023-08-16"
}
```
- Пример GET-запроса на адрес http://127.0.0.1:8000/api/sim/ для получения списка сим-карт.

Пример ответа:

```
{"msisdn": "89992229999",
"iccid": "0000000009",
"tariff": {
    "operator": "БИЛАЙН",
    "price": 500,
    "minutes": 600,
    "internet": 35,
    "name": "Гибкое решение за 500"
    },
"status": "AVAILABLE",
"region": "Москва",
"load_date": "2023-08-16",
"price": 0,
"type": "COMMON",
"other": "Прочая информация"}

```

## Документация
- Документация к API доступна по [ссылке](https://takesim.pythonanywhere.com/redoc/).

## Технологии
- [Python 3.10](https://www.python.org/downloads/)
- [Django 3.2](https://www.djangoproject.com/)
- [MySQL](https://dev.mysql.com/doc/)

## Доработка
- Необходим рефакторинг кода
- Настройка CI/CD

### Автор
- Ангелина Артемьева, github: [LinaArtmv](https://github.com/LinaArtmv)

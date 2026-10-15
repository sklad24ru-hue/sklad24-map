# Карта отзывов

Нейтральная внешняя карта отзывов с интерактивными объектами, рейтингами и фильтрами.

## Production-архитектура

- Хостинг: GitHub Pages.
- Движок интерактивной карты: MapLibre GL JS.
- Картографическая подложка: Yandex Tiles API.
- При отсутствии или ошибке подложки: интерактивный список объектов без карты.
- Данные объектов и отзывов: `map-data.json`.
- Google Apps Script формирует публичный снимок данных.
- GitHub Actions проверяет снимок, хранит последний валидный `map-data.json` и деплоит GitHub Pages.
- GitHub Actions добавляет официальный логотип Яндекса из архива, на который ссылается документация Tiles API.
- Telegram открывает обычный HTTPS-адрес GitHub Pages.
- Внешний интерфейс нейтральный и не содержит внутреннего бренда.
- В публичные данные не должны попадать ответственные сотрудники, внутренние токены и служебные поля.

## Yandex Tiles API

Для production нужен отдельный ключ Tiles API с ограничением по HTTP Referer:

`sklad24ru-hue.github.io`

Страница использует сферическую проекцию Web Mercator:

`projection=web_mercator`

Это необходимо для прямого подключения raster tiles к MapLibre.

Пока Apps Script v3.40 ещё не развёрнут, frontend поддерживает старый Yandex JavaScript API только как переходный режим без простоя. После появления `yandexTilesApiKey` используется Tiles API.

GitHub Pages:

https://sklad24ru-hue.github.io/sklad24-map/

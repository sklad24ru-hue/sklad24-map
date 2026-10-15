# Мониторинг отзывов

Внешний мониторинг отзывов с интерактивной картой объектов.

## Архитектура

- Frontend: Yandex Maps JavaScript API 3.0; Leaflet + OpenStreetMap используется только как аварийный fallback до настройки/при недоступности Яндекс API.
- Данные: `map-data.json` (включая публичный клиентский ключ Яндекс JS API с обязательным ограничением по HTTP Referer).
- Google Apps Script публикует свежий `map-data.json` в этот репозиторий.
- Telegram открывает обычный HTTPS-адрес GitHub Pages.
- В публичные данные не должны попадать ответственные сотрудники, токены, внутренние ключи и служебные поля.

GitHub Pages-интерфейс мониторинга доступен по адресу:

https://sklad24ru-hue.github.io/sklad24-map/


Pages deployment enabled: 2026-10-15.

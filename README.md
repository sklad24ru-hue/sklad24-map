# Sklad-24 Map

Публичная интерактивная карта объектов Склад-24.

## Архитектура

- Frontend: Leaflet + OpenStreetMap
- Данные: `map-data.json`
- Google Apps Script публикует свежий `map-data.json` в этот репозиторий.
- Telegram открывает обычный HTTPS-адрес GitHub Pages.
- В публичные данные не должны попадать ответственные сотрудники, токены, внутренние ключи и служебные поля.

После включения GitHub Pages карта будет доступна по адресу:

https://sklad24ru-hue.github.io/sklad24-map/


Pages deployment enabled: 2026-10-15.

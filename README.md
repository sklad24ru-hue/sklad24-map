# Склад-24 · Мониторинг отзывов

Внешний мониторинг отзывов Склад-24 с интерактивной картой объектов.

## Архитектура

- Frontend: Leaflet + OpenStreetMap
- Данные: `map-data.json`
- Google Apps Script публикует свежий `map-data.json` в этот репозиторий.
- Telegram открывает обычный HTTPS-адрес GitHub Pages.
- В публичные данные не должны попадать ответственные сотрудники, токены, внутренние ключи и служебные поля.

GitHub Pages-интерфейс мониторинга доступен по адресу:

https://sklad24ru-hue.github.io/sklad24-map/


Pages deployment enabled: 2026-10-15.

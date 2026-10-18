# Dev Tools Pro v2

Професионални уеб инструменти за разработчици и системни администратори.
Всичко работи **100% локално** в браузъра.

## Какво е новото (v2)

- 🏠 **Dashboard** с бърз достъп до всички инструменти
- 🔍 **Търсене** в навигацията (клавиш `/`)
- 📂 **Категории** в менюто (Текст, Сигурност, Dev, Работа)
- 🧭 **Единна навигация** между всички страници
- 🔒 `config.json` — смени паролата преди production
- 🗺️ Обновен sitemap с всички инструменти
- ♻️ Премахнато дублиране (`dev-tools.html` → redirect към `index.html`)

## Структура

| Файл | Описание |
|------|----------|
| `index.html` | Основен dashboard + вградени инструменти |
| `commandhub.html` | Ubuntu & PowerShell команди |
| `encrypt.html` | AES криптиране на файлове |
| `yaml-checker.html` | YAML front matter checker |
| `bash-prompt.html` | Генератор на bash prompt |
| `md_editor.html` | Разширен Markdown редактор |
| `premahva-exif-gps-xmp.html` | Премахване на EXIF/GPS/XMP |
| `config.json` | Парола за CommandHub (смени я!) |

## Сигурност

`config.json` съдържа `adminPassword` за CommandHub.
Това е **клиентска** защита — всеки може да види паролата в DevTools.
За реална сигурност използвай сървърна автентикация.

Преди публикуване смени:
```json
"adminPassword": "твоята-силна-парола"
```

## Автор

Федя Серафиев — https://fedia.eu/

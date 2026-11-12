# Dev Tools Pro v2.2

Професионални уеб инструменти за разработчици и системни администратори.
Всичко работи **100% локално** в браузъра — данните не напускат устройството.

**Адрес:** https://dev.serafiev.com/

## Какво е новото (v2.2)

- 🏠 **Миграция на домейна**: всички връзки водят до `dev.serafiev.com`, а към главния сайт — `serafiev.com`
- 🎨 **Единен бранд**: професионална favicon (SVG + PNG + ICO) и apple-touch-icon на всички страници, без различни emoji икони
- 🖼️ **og-image.png** (1200×630) за красиви споделяния в социални мрежи и чат applications
- 🔍 **SEO одит**: canonical URL, meta description и Open Graph тагове на всяка страница
- 🧭 **Hub-навигация**: линк към главния сайт от всички под-страници
- 📋 **YAML Checker по актуалната схема на serafiev.com**: шаблоните ползват `series`, `part`, `order`, `lang`, `heroImage` — точно каквото очаква Astro колекцията; `pubDate`/`updatedDate` се попълват с текущото време при зареждане; командите са `npm run dev` / `npm run build && npx wrangler deploy`
- 🐛 **Fix**: CommandHub каноничен URL (стария `komandi.pages.dev`), placeholder `YOURDOMAIN.com` в JSON-LD, дублиращ се fixed header в Encryptor-а, невалиден `<button>` вътре в `<a>` в YAML Checker-а
- 🗑️ Премахнат стария дубликат „Брояч на думи.html" и `.wrangler/` кеш файлове
- 🔒 Разширени security headers: `X-Frame-Options`, `Permissions-Policy` + кеш правила за favicon/og изображения

## Какво е новото (v2.1)

- 🔤 **Транслитерация** е първи инструмент и е отворен по подразбиране при зареждане
- ⭐ **Често използвани** раздел в навигацията с най-важните инструменти
- 🆕 **Брояч на думи** (word-count.html) добавен в менюто
- 🧭 **Единна хъб-навигация** на всички под-страници
- 🔍 Търсене в навигацията (клавиш `/`)

## Структура

| Файл | Описание |
|------|----------|
| `index.html` | Основна страница с вградени инструменти (транслитерация, emoji, пароли, hash, base64, JSON, цветове, линкове, .htaccess, yt-dlp) |
| `yaml-checker.html` | YAML front matter checker за serafiev.com, TrainBrakes и Здраве & Красота |
| `md_editor.html` | Разширен Markdown редактор с preview и препоръки |
| `word-count.html` | Брояч на думи с SEO/SERP проверка |
| `premahva-exif-gps-xmp.html` | Премахване на EXIF/GPS/XMP от снимки и невидими маркери от текст |
| `commandhub.html` | Ubuntu & PowerShell команди (sync през Cloudflare Worker) |
| `encrypt.html` | AES-256-GCM криптиране на файлове |
| `bash-prompt.html` | Генератор на bash prompt (PS1) |
| `dev-tools.html` | Пренасочване към `index.html` (за съвместимост със стари линкове) |
| `favicon.svg` / `favicon.ico` / `favicon-*.png` | Единният бранд на сайта |
| `apple-touch-icon.png` | Икона за iOS/Android начален екран |
| `og-image.png` | Картина за споделяне (Open Graph) |
| `_redirects` | 301 пренасочвания (старият `dev-tools.html` и кирилиският дубликат към `word-count.html`) |
| `config.json` | Парола за CommandHub (смени я!) |

## Подредба в навигацията (по най-използвани)

1. 🔤 Транслитерация (по подразбиране отворена)
2. 📋 YAML Checker
3. 📝 MD Editor
4. 🔡 Брояч на думи
5. 🖼️ EXIF/GPS Cleaner
6. 😀 Emoji Library

След тях: Пароли, SHA-256, Base64, JSON, Цветове, Моите линкове, URL → .htaccess, YouTube → MP3.

Разширени: CommandHub, File Encryptor, Bash Prompt.

## Сигурност

`config.json` съдържа `adminPassword` за CommandHub.
Това е **клиентска** защита — всеки може да види паролата в DevTools.
За реална сигурност използвай сървърна автентикация.

Преди публикуване смени:
```json
"adminPassword": "твоята-силна-парола"
```

## Автор

Федя Серафиев — https://serafiev.com/

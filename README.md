# IdeaValuate UZ Platform (Vercel + Render)

Платформа оценки и продажи бизнес-идей для рынка Узбекистана с интерактивной CRM-воронкой.

## Структура проекта

- `public/index.html` — Фронтенд-дашборд в 1 клик (деплой на **Vercel**).
- `server.py` — FastAPI бэкенд с поддержкой Perplexity API (деплой на **Render**).
- `vercel.json` — конфигурация маршрутизации для Vercel.
- `render.yaml` — Blueprint для мгновенного развертывания на Render.
- `requirements.txt` — Python-зависимости.

## Как задеплоить:

### 1. На Vercel (Фронтенд):
- Создайте проект в Vercel, выбрав корень `ideavaluate-app`.
- Vercel автоматически подхватит `public/index.html`.

### 2. На Render (Бэкенд):
- Создайте новый **Web Service** на `render.com`.
- Укажите Start Command: `uvicorn server:app --host 0.0.0.0 --port $PORT`
- Добавьте в Environment Variables:
  - `PERPLEXITY_API_KEY`: ваш ключ из кабинета Perplexity.

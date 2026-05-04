# 🤖 LexAI Chat

Чат-виджет на базе **n8n + GPT-4o-mini**, опубликованный как статический сайт на GitHub Pages.

## Стек

| Компонент | Технология |
|-----------|-----------|
| AI-агент | GPT-4o-mini (OpenAI) |
| Оркестрация | n8n — Webhook GET → AI Agent → Respond to Webhook |
| Память | Simple Memory (n8n) |
| Фронтенд | Vanilla HTML / CSS / JS |
| Хостинг | GitHub Pages |

## Быстрый старт

1. Откройте `index.html` в любом редакторе
2. Найдите строку и вставьте URL вашего n8n Webhook:
   ```js
   const WEBHOOK_URL = 'https://your-n8n.example.com/webhook/your-path';
   ```
3. Загрузите файл в репозиторий
4. Включите GitHub Pages: **Settings → Pages → main → / (root) → Save**

Сайт будет доступен по адресу:
```
https://ilyagogorev-blip.github.io/lexai-chat
```

## Структура n8n workflow

```
Webhook (GET)
    └── AI Agent (GPT-4o-mini + Simple Memory)
            └── Respond to Webhook
```

## CORS

В настройках ноды **Webhook** в n8n добавьте разрешённый origin:
```
https://ilyagogorev-blip.github.io
```

## Лицензия

MIT


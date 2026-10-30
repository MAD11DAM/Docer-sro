# Простой проект Docker

Это учебный проект: Docker запускает веб-сервер Nginx и показывает простую HTML-страницу.

## Что находится в проекте

- `Dockerfile` — инструкция для сборки Docker-образа.
- `index.html` — страница сайта.

## Запуск

Откройте терминал в папке проекта и выполните:

```bash
docker build -t my-simple-site .
docker run -d --name my-simple-site -p 8080:80 my-simple-site
```

Откройте в браузере: <http://localhost:8080>

Чтобы остановить и удалить контейнер:

```bash
docker stop my-simple-site
docker rm my-simple-site
```

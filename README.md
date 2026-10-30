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

## Как работает Dockerfile

1. `FROM nginx:alpine` загружает лёгкий образ Nginx.
2. `COPY` помещает страницу сайта в папку, из которой Nginx раздаёт файлы.
3. `EXPOSE 80` указывает порт веб-сервера внутри контейнера.

## Загрузка проекта на GitHub

Создайте новый пустой репозиторий на GitHub. Затем в терминале из папки проекта выполните команды, заменив `ВАШ_ЛОГИН` и `ИМЯ_РЕПОЗИТОРИЯ` на свои данные:

```bash
git init
git add Dockerfile index.html README.md
git commit -m "Добавлен простой Docker-проект"
git branch -M main
git remote add origin https://github.com/ВАШ_ЛОГИН/ИМЯ_РЕПОЗИТОРИЯ.git
git push -u origin main
```

# 🚀 FastAPI + Nginx в Docker

Пример простого проекта, демонстрирующего, как развернуть FastAPI-приложение с HTML-шаблонами за Nginx-прокси в Docker.

## 🔧 Стек технологий

- [FastAPI](https://fastapi.tiangolo.com/) — асинхронный Python-фреймворк
- [Nginx](https://nginx.org/) — веб-сервер и обратный прокси
- [Docker](https://www.docker.com/) + [Docker Compose](https://docs.docker.com/compose/) — для контейнеризации

## 🗂️ Структура проекта

```
fastapi-nginx-docker/
├── app/
│   ├── main.py
│   ├── templates/
│   │   ├── index.html
│   │   └── about.html
│   └── Dockerfile
├── nginx/
│   └── default.conf
├── docker-compose.yml
└── README.md
```

## ⚙️ Как запустить проект

> Убедитесь, что у вас установлен [Docker Desktop](https://www.docker.com/products/docker-desktop)

1. **Клонируйте репозиторий:**

```bash
git clone https://github.com/Antongo22/fastapi-nginx-docker.git
cd fastapi-nginx-docker
```

2. **Соберите и запустите контейнеры:**

```bash
docker-compose up --build
```

3. **Откройте в браузере:**

- [http://localhost/](http://localhost/) — главная страница
- [http://localhost/about](http://localhost/about) — страница "О нас"

## 📦 Сервисы в docker-compose

| Сервис | Назначение             | Порт |
|--------|------------------------|------|
| app    | FastAPI-приложение     | 8000 |
| nginx  | Реверс-прокси          | 80   |

## ✨ Возможности

- Обработка HTML-шаблонов через Jinja2
- Чистая маршрутизация с FastAPI
- Reverse proxy через Nginx
- Готово к деплою на VPS / сервер

## 📌 Примеры маршрутов

| Метод | URL             | Описание             |
|-------|------------------|----------------------|
| GET   | `/`              | Главная страница     |
| GET   | `/about`         | Страница "О нас"     |


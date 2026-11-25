# Taski

Taski — веб-приложение для планирования задач (трекер). Позволяет создавать, редактировать и удалять задачи, а также отмечать их как выполненные.

## Стек

**Backend** — Django + Django REST Framework:

- Django 5.1.1
- djangorestframework 3.15.2
- django-cors-headers 4.6.0

**Frontend** — SPA на React 18:

- React 18.2, axios, Bootstrap 5, reactstrap
- сборка через react-scripts (Create React App)

## Структура проекта

```
taski/
├── backend/     # Django-приложение (REST API + админка)
└── frontend/    # React SPA
```

## Запуск в режиме разработки

### Backend

```bash
cd backend
python -m venv venv
source venv/bin/activate
pip install -r requirements.txt
python manage.py migrate
python manage.py runserver
```

### Frontend

```bash
cd frontend
npm install
npm run start
```

Фронтенд проксирует запросы к API на `http://127.0.0.1:8000`.

## Деплой

Для продакшена используется связка Gunicorn (WSGI-сервер) + Nginx (веб-сервер и обратный прокси).

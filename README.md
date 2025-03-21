# API для социальной сети Yatube
## Описание
Этот проект предоставляет API для взаимодействия с социальной сетью Yatube. API позволяет выполнять следующие действия:
1) Просмотр, создание, редактирование и удаление публикаций.
2) Добавление, просмотр и удаление комментариев к публикациям.
3) Просмотр информации о сообществах (группах).
4) Подписка на других пользователей.
5) Аутентификация и авторизация с использованием JWT-токенов.

## Установка
Клонируйте репозиторий:
  git clone ...
Создайте и активируйте виртуальное окружение:
  python -m venv venv
  venv\Scripts\activate
Установите зависимости:
  pip install -r requirements.txt
Примените миграции:
  python manage.py migrate
Запустите сервер разработки:
  python manage.py runserver


## Примеры запросов к API
1. Получение списка публикаций
Запрос:
GET /api/v1/posts/
2. Создание публикации
Запрос:
POST /api/v1/posts/
Тело запроса:
{
  "text": "Новая публикация",
  "group": 1
}
3. Добавление комментария
Запрос:
POST /api/v1/posts/1/comments/
Тело запроса:

{
  "text": "Новый комментарий"
}
4. Подписка на пользователя
Запрос:
POST /api/v1/follow/
Тело запроса:
{
  "following": "username_to_follow"
}

5. Получение JWT-токена
Запрос:
POST /api/v1/jwt/create/
Тело запроса:
{
  "username": "your_username",
  "password": "your_password"
}

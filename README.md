# Проект YaMDb
IP - 84.201.140.189
![example workflow](https://github.com/marbaswp/yamdb_final/actions/workflows/yamdb_workflow.yml/badge.svg?branch=master&event=push)

Проект YaMDb собирает отзывы пользователей на произведения. Сами произведения в YaMDb не хранятся, здесь нельзя посмотреть фильм или послушать музыку.

Добавлять произведения, категории и жанры может только администратор.

Благодарные или возмущённые пользователи оставляют к произведениям текстовые отзывы и ставят произведению оценку в диапазоне от одного до десяти (целое число); из пользовательских оценок формируется усреднённая оценка произведения — рейтинг (целое число). На одно произведение пользователь может оставить только один отзыв.

Пользователи могут оставлять комментарии к отзывам.

Добавлять отзывы, комментарии и ставить оценки могут только аутентифицированные пользователи.
___
### Стэк технологий:
* Python
* Django
* Django Rest Framework
* PostgreSQL
* Nginx
* Gunicorn
* Docker
* Docker-compose
___
### Как запустить проект:
Клонировать репозиторий и перейти в него в командной строке:
```
git clone git@github.com:MarbasWP/yamdb_final.git
cd yamdb_final
```
Развернуть докер контейнеры:

```
sudo docker-compose up
```
Выполнить миграции и собрать статику:

```
docker-compose exec web python manage.py migrate
docker-compose exec web python manage.py createsuperuser
docker-compose exec web python manage.py collectstatic --no-input
```
___
### Примеры использования api:

Получение произведений:
```
GET /api/v1/titles/
```
Добавление произведения:
```
POST /api/v1/titles/
```
___
### Документация и возможности API:
К проекту подключен redoc. 
Для просмотра документации используйте эндпойнт redoc/ 
Пример обращения: http://localhost/redoc/


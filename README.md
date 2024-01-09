# Описание проекта
Сайт с возможностью публикации фотографий котов и их достижений.

# Возможности
Публикация и редактирование профиля кота.
Размещение фото и достижений кота.

# Технологии
React
Django
DRF
Nginx
Gunicorn
Docker
Docker-compose
CI/CD
Github Actions

# Установка.
### Клонировать репозиторий:
git clone git@github.com:Alex-085/kittygram_final.git

# Подготовка проекта к созданию образов контейнеров и запуску на удалённом сервере:
Написать Dockerfile для образа "kittygram_backend".
Создайть файл .env в корне проекта с переменными окружения:
POSTGRES_USER=kittygram_user
POSTGRES_PASSWORD=kittygram_password
POSTGRES_DB=kittygram
DB_HOST=db
DB_PORT=5432
DB_NAME=kittygram
SECRET_KEY=django-insecure-cg6*%6d51ef8f#4!r3*$vmxm4)abgjw8mo!4y-q*uq1!4$-89$
DEBUG=False
ALLOWED_HOSTS='127.0.0.1,localhost,fedor-aaappp.ddns.net'

Написать docker-compose.yml и docker-compose.production.yml.
Добавить volume для статических файлов админки и фронтенда (static_volume).
Добавить volume для хранения файлов, загруженных пользователями (media).
Подключить файл .env к контейнерам db и backend (env_file: .env).

# Настройка CI/CD.
### Создать файл .github/workflows/main.yml workflow для тестирования кода, сборки образов, статики, выполнения миграций.

### Подготовить удалённый сервер к публикации проекта Kittygram:
Создать директорию kittygram/ в домашней директории сервера.
Скопировать "docker-compose.production.yml" и ".env" в папку kittygram/
Настроить файл конфигурации Nginx для Kittygram.

# Задеплоить проект.
git add .
git commit -m "Add ___ commit"
git push

### И далее проект доступен на:
https://github.com/Alex-085/
Автор: Александр Кудрявцев

# Сервер магазина

Проект для изучения Django. Взято с Stepik.

#### Стек:

- [Python](https://www.python.org/downloads/)
- [PostgreSQL](https://www.postgresql.org/)
- [Redis](https://redis.io/)

## Локальная разработка

Все команды выполняются из корневой директории проекта после установки зависимостей.

1. Создайте и активируйте виртуальное окружение:
   ```bash
   python3.9 -m venv ../venv
   source ../venv/bin/activate
   ```
   
2. Установите пакеты:
   ```bash
   pip install --upgrade pip
   pip install -r requirements.txt
   ```
   
3. Выполните миграции и загрузите фикстуры:
   ```bash
   ./manage.py migrate
   ./manage.py loaddata <путь_к_фикстурам>
   ./manage.py runserver 
   ```
   
4. Запустите [Redis Server](https://redis.io/docs/getting-started/installation/):
   ```bash
   redis-server
   ```
   
5. Запустите Celery:
   ```bash
   celery -A store worker --loglevel=INFO
   ```

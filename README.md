# Docker Проект

Этот репозиторий содержит Docker образы для Nginx и Django REST API сервера.

## Задание 1/2 :

### Описание
Создан Docker image с http сервером Nginx, который отображает пользовательскую страницу приветствия.

Создан Docker контейнер для Django проекта с использованием SQLite в качестве базы данных.
### Команды

1. **Сборка Docker образа**:
   ```shell
   docker build -t my-nginx .
2. **Запуск контейнера**:
   ```shell
   docker run -d -p 8000:8000 my-nginx
   ```

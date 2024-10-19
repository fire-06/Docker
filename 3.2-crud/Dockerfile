# Используем базовый образ Python
FROM python:3.10-slim

# Устанавливаем рабочую директорию
WORKDIR /app

# Копируем файл зависимостей
COPY stocks_products/requirements.txt .


# Устанавливаем зависимости
RUN pip install --no-cache-dir -r requirements.txt \
    && pip install django-filter
# Копируем весь проект
COPY . .

WORKDIR /app/stocks_products
# Применяем миграции
RUN python manage.py migrate

# Открываем порт 8000 для приложения
EXPOSE 8000

# Запускаем Django сервер
CMD ["python", "manage.py", "runserver", "0.0.0.0:8000"]

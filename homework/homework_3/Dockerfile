# Официальный образ Python в качестве базового
FROM python:latest

# Рабочая директория внутри контейнера
WORKDIR /app

# Копируем зависимости и код приложения
COPY requirements.txt .
COPY memory_info.py .

# Устанавливаем зависимости
RUN python3 -m pip install -r requirements.txt -U

# Создаём папку для результата (сюда будет примонтирована папка хоста)
RUN mkdir -p data

# Запуск приложения
ENTRYPOINT ["python3", "memory_info.py"]

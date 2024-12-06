# Используем базовый образ Python
FROM python:3.9-slim

# Устанавливаем рабочую директорию внутри контейнера
WORKDIR /app

# Копируем файл requirements.txt и устанавливаем зависимости
COPY requirements.txt ./
RUN apt-get update && apt-get install -y libglib2.0-0 libgl1-mesa-glx
RUN pip install --no-cache-dir -r requirements.txt

# Копируем исходный код приложения
COPY src/ ./src/

# Создаём директорию для логов внутри контейнера
RUN mkdir logs

# Запускаем приложение
CMD ["python", "./src/plot.py"]

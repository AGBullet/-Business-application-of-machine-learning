# Используем базовый образ Python
FROM python:3.9-slim

# Устанавливаем рабочую директорию внутри контейнера
WORKDIR /app

# Копируем файл requirements.txt и устанавливаем зависимости
COPY requirements.txt ./
RUN pip install --no-cache-dir -r requirements.txt

# Копируем исходный код приложения
COPY src/ ./src/

# Копируем дополнительные файлы (если есть)
# В данном случае нет дополнительных файлов

# Запускаем приложение
CMD ["python", "./src/features.py"]

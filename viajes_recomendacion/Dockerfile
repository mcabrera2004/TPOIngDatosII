# Usar imagen base de Python 3.10
FROM python:3.10-slim

# Establecer directorio de trabajo
WORKDIR /app

# Copiar requirements.txt e instalar dependencias
COPY requirements.txt .
RUN pip install --no-cache-dir -r requirements.txt

# Copiar el resto del código
COPY . .

# Variables de entorno para MongoDB Atlas (se configurarán en docker-compose)
ENV MONGO_URI=""
ENV DB_NAME="viajes_db"

# Puerto para la API Flask
EXPOSE 5000

# Comando para ejecutar la aplicación (ajustar según tu script principal)
CMD ["python", "main.py"]
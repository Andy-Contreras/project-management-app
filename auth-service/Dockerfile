# base con python 3.10, version liviana
FROM python:3.10-slim
# directorio donde correra nuestra app
WORKDIR /app
# copiamos primero despendencias (optimiza el cache)
COPY requirements.txt requirements.txt
# instalamos dependencias 
RUN pip install --no-cache-dir -r requirements.txt
# Copiamos el resto del codigo
COPY . .
# indicamos que este conectener escuha en el puerto 8000
EXPOSE 8000
# el comando por defecto, correr Django 
CMD ["python", "manage.py", "runserver", "0.0.0.0:8000"]

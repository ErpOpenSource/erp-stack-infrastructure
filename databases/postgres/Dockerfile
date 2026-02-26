FROM postgres:16-alpine

# Instalamos dependencias si fueran necesarias (ej. extensiones postgis)
# Por ahora mantenemos la imagen ligera con alpine.

# Copiamos scripts de inicialización
COPY ./init /docker-entrypoint-initdb.d/

# Exponemos el puerto estándar
EXPOSE 5432
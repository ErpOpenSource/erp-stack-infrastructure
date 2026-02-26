FROM redis:7-alpine

# Copiamos nuestra configuración personalizada
COPY redis.conf /usr/local/etc/redis/redis.conf

# Ejecutamos redis con la config cargada
CMD [ "redis-server", "/usr/local/etc/redis/redis.conf" ]

EXPOSE 6379
# Dockerfile
FROM redis:7.2-alpine

# Copy custom config into the container
COPY redis.conf /usr/local/etc/redis/redis.conf

# Start Redis with the custom config
CMD ["redis-server", "/usr/local/etc/redis/redis.conf"]
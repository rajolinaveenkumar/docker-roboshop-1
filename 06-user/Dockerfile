FROM node:18.19.1-alpine3.19
EXPOSE 8080

# Create system user and group
RUN addgroup -S roboshop && adduser -S roboshop -G roboshop

WORKDIR /opt/server
RUN chown roboshop:roboshop /opt/server

# Switch to roboshop user
USER roboshop

# Copy source code
COPY scripts/* . 
RUN npm install

# Environment variables (can override during run)
ENV MONGO=true \
    REDIS_URL="redis://redis:6379" \
    MONGO_URL="mongodb://mongodb:27017/users"

# Start the app
CMD ["node", "server.js"]

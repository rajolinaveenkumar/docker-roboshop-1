FROM node:18.19.1-alpine3.19
EXPOSE 8080
RUN addgroup -S roboshop && adduser -S roboshop -G roboshop
# RUN addgroup -S <group-name> && adduser -S <user-name> -G <group-name>
WORKDIR /opt/server
RUN chown roboshop:roboshop /opt/server
# chown <user>:<group> <path>
USER roboshop
COPY scripts/* .
RUN npm install
ENV DB_HOST="mongodb"
CMD ["node", "server.js"]


### IMP NOTES
# What it does:
# addgroup -S roboshop:
# ➤ Creates a system group named roboshop.

# adduser -S roboshop -G roboshop:
# ➤ Creates a system user named roboshop
# ➤ Assigns it to the group roboshop.

# System users (-S) are for services, not for login. They usually have no password and no home directory.
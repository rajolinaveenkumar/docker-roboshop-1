FROM mongo:7.0.21
RUN rm -rf /etc/mongod.conf.orig
COPY mongod.conf.orig /etc/
COPY *.js /docker-entrypoint-initdb.d/

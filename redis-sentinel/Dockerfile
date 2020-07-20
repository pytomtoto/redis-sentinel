FROM redis:5-alpine
 
RUN mkdir -p /redis
 
WORKDIR /redis
 
COPY sentinel.conf .
 
RUN chown redis:redis /redis/* 
 
EXPOSE 26379
 
CMD ["redis-server","/redis/sentinel.conf","--sentinel"]
# Docker Activemq 
[![Docker Image CI](https://github.com/jannctu/docker-activemq/actions/workflows/docker-image.yml/badge.svg)](https://github.com/jannctu/docker-activemq/actions/workflows/docker-image.yml)
[![Docker Pulls](https://img.shields.io/docker/pulls/jannctu/docker-activemq.svg?maxAge=2592000)](https://hub.docker.com/r/jannctu/docker-activemq/)

ActiveMQ Docker for highly flexible customization.

Docker Hub: https://hub.docker.com/r/jannctu/docker-activemq

### Build Docker Image 
```
docker build -t jannctu/docker-activemq:latest .
```
### Run using `docker-compose`
```
docker-compose up -d 
```


### Build and RUN
```
docker-compose -f docker-compose-build.yml up -d 
```

### Port Map 
```
# 61616 is for openwire / tcp 
# 5672 is for AMQP 
# 61613 is for stomp
# 1883 is for MQTT
# 8161 is for admin console (web) 
# 61614 is for websockets
```

### Default Users 
* ADMINISTRATORS :  
    - admin:admin
* PUBLISHERS :
    - admin:admin
    - publisher:publisher
* CONSUMERS : 
    - admin:admin
    - publisher:publisher
    - consumer:consumer
* GUESTS :
    - guest:guest
* WEB CONSOLE: 
    - admin-admin
    - user-user 


### Customization 
The best way to customize ActiveMQ is by creating the config files. Please refer to the `conf` directory. For further details configuration please refer to the offical ActiveMQ [documentation](https://activemq.apache.org/using-activemq).

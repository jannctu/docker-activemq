# Docker Activemq 

ActiveMQ Docker for highly flexible customization.

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
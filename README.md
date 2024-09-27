# 1. Setup
This project makes use of RabbitMQ. In order for it to work, you need to make sure that you run RabbitMQ in a docker container. You can use the following commands to run a docker container with RabbitMQ:

pull rabbitmq
```
docker pull rabbitmq:3-management
```

start a container with the pulled RabbitMQ image:

```
docker run --rm -it -p 15672:15672 -p 5672:5672 rabbitmq:3-management
```

# 2. Usage 
- Run the `ConfigServerApplication`
- Change the configuration in `myservice-dev.yml`
- post to: `http://localhost:8888/actuator/refresh`

# Microservices Demo App

- Please enter the correct credentials in twitter4j.properties file.
- Then run TwitterToKafkaServiceApplication inside IntelliJ, or run with mvn spring-boot:run command
- Check docker-compose folder, and run kafka cluster using docker-compose -f common.yml -f kafka_cluster.yml up command
- Then check the docker containers using docker ps command
- Use standalone kafkacat or docker container(https://hub.docker.com/r/confluentinc/cp-kafkacat) to install kafkacat
- Then check the kafka cluster information using kafkacat -L -b localhost:19092 command

## Start docker-compose
```bash
docker-compose -f common.yml -f kafka_cluster.yml -f services.yml up -d
or 
docker-compose up -d
```

## Stop docker-compose
```bash
docker-compose -f common.yml -f kafka_cluster.yml -f service.yml down
or 
docker-compose down
```

## Maven Skip Tests
```bash
mvn install -DskipTests
```

## Permitions check-com.microservices.demo.kafka.consumer.config-server-started file
```bash
chmod +x check-com.microservices.demo.kafka.consumer.config-server-started.sh 
```

##Clear Docker
```bash
docker rmi $(docker images -a -q)
docker volume prune 
docker system prune
docker network prune
```  

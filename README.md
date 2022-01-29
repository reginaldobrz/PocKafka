# PocKafka
A POC to Produce and consume some messages using KAFKA.
This POC is a .netCore 6 Console app to Produce some messages and consume this messages using KAFKA.

First of all you need to setup the ZOOKEEPER and KAFKA by docker.

* ZOOKEEPER -
````
docker pull confluentinc/cp-zookeeper
````

  * Now you need to configure the connection by running this command line:
````
<docker network create kafka>
````
````
<docker run -d --network=kafka --name=zookeeper -e ZOOKEEPER_CLIENT_PORT=2181 - e ZOOKEEPER_TICK_TIME=2000 -p 2181:2181 confluentinc/cp-zookeeper>
````

* KAFKA
````
docker pull confluentinc/cp-kafka
````
  * Now you need to configure the connection by running this command line:

````
<docker run -d --network=kafka --name=kafka -p 9092:9092 -e KAFKA_ZOOKEEPER_CONNECT=zookeeper:2181 - e KAFKA_ADVERTISED_LISTENERS=PLAINTEXT://localhost:9092 confluentinc/cp-kafka>
````


After that, just run the application and see the magic happens, good luck!

Easy hamm? 😎

<p align="center"><img src="https://i.pinimg.com/originals/4e/9e/6f/4e9e6f979347906a426adcbe57fd3259.gif" alt="PRs welcome!" />



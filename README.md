# rabbitmq-tutorial
 Rabbitmq + Java + Docker 

## Introduction

Using Java + Docker + RabbitMQ, explaining from the simplest to the more complex scenario that you can implement it.

All scenarios and code are in src/main/java/ in their respective folder.

It's represent one of the protocols that RabbitMQ supports, I will create one repo with RabbitMQ streams in a short future!

### Starting Up 

This project includes gradle dependencies to include the libraries requires to make rabbitmq works(amqp-client and slf4j).

Instead of taking care by ourselves of the rabbitmq server installation, I suggest run the rabbitmq image in Docker: 
```
docker run --name rabbitmq -p 5672:5672 rabbitmq
```
this will gives us a ready environment to work in only one command!

note: Default ports for rabbitmq is 5672

## Scenarios (don't forget to run your docker image first)

### Simple Sender and Receiver

The simplest scenario.

You have the Recv.java that will be running and logging the message you will send from Send.java

The flow will be something like: Send.java -> (Docker) RabbitMQ Server -> Recv.java

And that its! simple, right?

### Work Queues (Task Queues)

We will simulate a long/complex task, and will see how Work Queues will schedule the task. 
The Work Queue will be used to distribute time-consuming tasks among multiple workers.


....

# WIP 
#Seven Essential Services Recruiting Task
##1. What is this project?
This project is made out of two microservices that run inside a docker container. The first service acts as a money transaction producer, whilst the other consumes those messages from an AMQP (advanced message queuing protocol), in this case RabbitMQ, and saves them to a database.I will not be going deeper into RabbitMQ, if you are interested you can visit the official documentation here.
##2. Installation instructions
###2.a Prerequisites:
• Docker (Get it here)
• Make sure ports 8080, 8081, 3306, 5672, 15672 are not in use!
• That’s it, docker does the rest for you. Cool right!?
###2.b Running the project
####1. Clone the project to your workspace.
####2. Open a console/terminal and cd to the cloned project
( make sure you’re in the root of the project( example@linux /Nsoft-Zadatak$ ).
####3.Type (sudo) docker-compose up
That should be it, the services should be up and running. The first build takes time so please be patient.
##3. Using the services
###1. Sending a transaction message:
Go to http://localhost:8080/transaction?amount=&currency=EUR
(Only supports EUR as a currency)
###2. To view the balance of the account go to:
http://localhost:8081/details
##4. Tech specs:
• Programming language used: Java 8
• Frameworks: Spring Web
• Backend: MariaDB

# infytel-cloudConfig
cloud config for spring micro services

https://microservices.io/patterns/index.html



Many challenges of microservices can be solved by using appropriate design patterns. We have already seen some of them in the course. The challenges can be addressed by the patterns such as:

As the number of microservices increases, managing them and scaling them becomes difficult

Load Balancing pattern (Ribbon), Messaging Patterns

Failure points are more

Circuit Breaker Pattern, Fallback pattern (Hystrix)

Since the attack area increases, security challenges also increase

Spring-Cloud-Security, Spring-Cloud-OAuth2

Since the number of microservices are high, keeping track of what is happening where becomes difficult

Service Discovery(Eureka Dashboard), Circuit Breaker ( Hystrix, Turbine ), Distributed Tracing Pattern (Zipkin)

We need to monitor the different services and find out which are up, which are down, which need scaling, etc

Service Discovery(Eureka Dashboard), Circuit Breaker ( Hystrix, Turbine ), Distributed Tracing Pattern (Zipkin)

Log data will be immense and we need to find out meaningful information from them

Distributed Tracing ( Sleuth, ELK Stack )

A single faulty service can bring down all the other services

Circuit Breaker ( Hystrix )

Coordinating with external services is a challenge

API Gateway, Backend For Frontend

Managing databases becomes increasingly difficult

Single DB, DB Per Service, API composition, Saga, CQRS

Since each service may use different technology stack, deploying them also becomes a challenge

Multiple service instances per host, Service instance per host , Service instance per Container 






#The microservices can also be packaged in the below ways:

container-less : The executable is a JAR or WAR but the dependent frameworks are separate. For example, it does not include Tomcat, Jboss, etc

self-contained: This contains the executable as well as the frameworks.

in-container: The executable, frameworks and the entire JVM is packaged in one go, using a container technology like Docker, Kubernetes, etc

The best way is to go for in-container as this ensures that the development, testing, deployment environments are same for every one and it is best from Devops perspective.








#ProblemStatement:
As part of this course, you will be developing a SIM activation portal as the final project.

SIM activation portal automates the SIM activation process for the customers.

While purchasing the SIM, customer has to provide customer details such as first name, last name, email, dob etc.. along with ID proof to the provider. Customer gets a starter SIM kit with SIM details.

Customer can activate the SIM through the portal by providing the SIM number which is present in the starter kit along with service number (mobile number).

SIM activation process involves following steps.

SIM validation

Show special offer

Customer validation based on email and date of birth

Customer details and email confirmation

Update address details

Customer ID proof validation

Summary of the request details to proceed with SIM activation.

Implementation
 Develop a SIM activation portal by identifying and implementing required microservices for the given user stories.

Download user stories document here

Required UI ( developed using Bootstrap, jQuery and HTML5) is provided. Download it here

You will have to implement services and test the end-to-end flow for user stories.

 Include below given features

Route requests through API Gateway 

Provide security to REST points

Implement fallback mechanism at service and gateway level

Use Feign client for services interaction

Use centralized configuration 

Trace the requests and log the details into a file              

Implement a feature to monitor the services 

For better understanding, application flow is provided through video in the next page.


#More
http://localhost:1111/application/default

create bootstrap properties in all microservices for the purpose of cloud config

We can access the configuration files by using endpoint on the config server in any one of the below patterns:

http://<config_server_host>:<port>:/<application>-<profile>.yml
http://<config_server_host>:<port>/<application>-<profile>.properties



http://localhost:5555/eureka/apps

for Randomport: ${PORT:${SERVER_PORT:0}}

AMQP 

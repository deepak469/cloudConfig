# infytel-cloudConfig
cloud config for spring micro services


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

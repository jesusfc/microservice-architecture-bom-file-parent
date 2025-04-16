# SpringBoot 3 - Bom File Dependencies Management and Modules

Bom file for unification of dependencies in a microservices architecture

## Modules
- Spring Cloud Config Server (port: 8888)
- Spring Cloud Gateway (port: 8080)
- Spring Cloud Circuit Breaker (port: 8090)
- Spring Cloud Eureka Server (port: 8761) (http://localhost:8761/)
- Spring Api Rest Service 1 (port: 8081)
- Spring Api Rest Service 2 (port: 8082)
- Spring Api Rest Service 3 (port: 8083)
- Spring Api Rest Service 4 (port: 8084)
- Artemis JMS (port: 8161) with Docker (http://localhost:8161/console/artemis)
- ZipKin Distributed Tracing (port: 9411) with Docker (http://localhost:9411/zipkin/)

## Dependencias
- Started Web
- DevTools
- Actuator
- Project Lombok
- JUnit
- Mockito

# Building Docker images with Maven
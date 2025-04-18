# SpringBoot 3 - Bom File Dependencies Management and Modules

Bom file for unification of dependencies in a microservices architecture

### Project Structure

- This is a multi-module Spring Boot project using a BOM (Bill of Materials) approach
- Parent POM manages dependencies and plugins for all modules

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

### Code Style

- Java 17 features are used throughout the project
- Lombok is used to reduce boilerplate code
- Spring Boot 3.4.0 is the foundation for all services

### Logging

- Logback with Logstash encoder is used for structured logging
- Configure logging levels in application.properties/yml files

### Distributed Tracing

- Zipkin is used for distributed tracing (http://localhost:9411/zipkin/)
- Micrometer Tracing Bridge (Brave) is used for instrumentation

### Messaging

- Both ActiveMQ (JMS) and Kafka are used for messaging
    - ActiveMQ console: http://localhost:8161/console/artemis
- Message structures should be consistent across services

### Reactive Programming

- WebFlux services use the reactive programming model
- Use Mono for single results and Flux for multiple results
- Avoid blocking operations in reactive code

### Circuit Breaking

- Spring Cloud Circuit Breaker is used for resilience patterns
- Configure circuit breakers for external service calls

### Service Discovery

- Eureka is used for service registration and discovery
- Register all microservices with Eureka for dynamic service discovery

### Configuration Management

- Spring Cloud Config Server centralizes configuration
- Environment-specific configurations are stored in the config server

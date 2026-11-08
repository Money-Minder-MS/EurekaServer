# EurekaServer — Service Discovery

Netflix Eureka registry for the **Money Minder MS** microservices system. Every
service registers here on startup so the API Gateway and the services can find
each other by name instead of by hard-coded host and port.

## Tech stack

Java · Spring Boot · Spring Cloud Netflix Eureka Server

## Run

```bash
mvn spring-boot:run
```

- Registry dashboard: http://localhost:8761
- Port: `8761`

This server does not register with itself (`register-with-eureka=false`).

## Part of Money Minder MS

A Spring Cloud microservices platform for personal-finance management. The full
architecture and the list of services are documented in the
[API-Gateway README](https://github.com/Money-Minder-MS/API-Gateway). Start the
services in this order: **EurekaServer → Config-Server → business services → API-Gateway**.

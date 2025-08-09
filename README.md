# API Gateway with Spring Cloud Gateway

[![Java](https://img.shields.io/badge/Java-17%2B-blue)](https://openjdk.org/)
[![Maven](https://img.shields.io/badge/Maven-3.8%2B-C71A36)](https://maven.apache.org/)
[![Spring Boot](https://img.shields.io/badge/Spring%20Boot-3.x-brightgreen)](https://spring.io/projects/spring-boot)
[![Spring Cloud](https://img.shields.io/badge/Spring%20Cloud-2023.x-brightgreen)](https://spring.io/projects/spring-cloud)
[![License: MIT](https://img.shields.io/badge/License-MIT-yellow.svg)](LICENSE)

A lightweight, high-performance **API Gateway** built with **Spring Cloud Gateway** to simplify and secure communication in microservices architectures.  
It acts as a single entry point for all client requests, handling routing, load balancing, security, and monitoring—so your services can stay focused on business logic.



## 📖 Overview

In a distributed microservices setup, clients often need to call multiple services to complete a task. An API Gateway eliminates this complexity by providing a unified interface.  
This project uses **Spring Cloud Gateway** to deliver a reactive, scalable, and easily configurable gateway solution for your applications.



## ✨ Features

- **Routing** – Define routes for incoming requests and direct them to the correct downstream services.
- **Filters** – Apply pre- and post-filters to manipulate requests and responses for tasks like authentication, rate limiting, and logging.
- **Load Balancing** – Integrate with service discovery to balance traffic across microservice instances.
- **Resilience** – Use circuit breakers and other fault-tolerance patterns to handle failures gracefully.
- **Monitoring** – Integrate with monitoring tools to track metrics and ensure system health.



## 🚀 Getting Started

### Prerequisites

Ensure you have the following installed before proceeding:

- **Java 17+** → [Download OpenJDK](https://openjdk.org/)
- **Apache Maven** → [Installation Guide](https://maven.apache.org/install.html)

### Installation

1. **Clone the repository**
   ```
   git clone https://github.com/shubham225/api-gateway.git
   ```

2. **Navigate to the project directory**
   ```
   cd api-gateway
   ```

3. **Build the project**
   ```
   mvn clean install
   ```

### Running the Application

1. Start the Spring Cloud Gateway application:
   ```
   java -jar target/api-gateway.jar
   ```

2. Access the gateway via your configured routes.



## ⚙️ Configuration

The gateway configuration is defined in the `application.yml` file.  
You can customize:

- Routes
- Filters
- Load balancing settings
- Other application properties

### Example Configuration

```yaml
spring:
  cloud:
    gateway:
      routes:
        - id: user-service
          uri: http://localhost:8081
          predicates:
            - Path=/users/**
          filters:
            - PrefixPath=/api/V1

server:
  port: 8080
```

In this example:
- Requests to `/users/**` are routed to `http://localhost:8081`
- The prefix `/users` is stripped before forwarding
- A **rate limiter** is applied (5 requests/sec with a burst capacity of 10)



## 📜 License

This project is licensed under the **MIT License** – see the [LICENSE](LICENSE) file for details.

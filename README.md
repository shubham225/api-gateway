# API Gateway with Spring Cloud Gateway

This repository contains a project for building an API Gateway using Spring Cloud Gateway.

## Overview

An API Gateway is an essential component in microservices architecture, acting as a single entry point for clients to access various microservices. Spring Cloud Gateway provides a powerful and flexible way to build API gateways.

## Features

- **Routing**: Define routes for incoming requests and route them to appropriate downstream services.
- **Filters**: Implement filters to manipulate requests and responses, enabling functionalities such as authentication, rate limiting, logging, and more.
- **Load Balancing**: Integrate with service discovery mechanisms for load balancing across instances of microservices.
- **Resilience**: Utilize built-in resilience features such as circuit breakers to handle failures gracefully.
- **Monitoring**: Integrate with monitoring tools to gather metrics and monitor the health of the gateway and downstream services.

## Getting Started

### Prerequisites

Before you begin, ensure you have the following prerequisites installed:

- **Java Development Kit (JDK) 17**: Make sure you have Java 17 installed on your system. You can download it from the [official website](https://www.oracle.com/java/technologies/javase-jdk17-downloads.html) or use a package manager for your operating system.
- **Apache Maven**: This project uses Maven as the build system. You can download Maven from the [official website](https://maven.apache.org/download.cgi) or install it using a package manager.

### Installation

1. Clone this repository:

    ```bash
    git clone https://github.com/shubham225/api-gateway.git
    ```

2. Navigate to the project directory:

    ```bash
    cd api-gateway
    ```

3. Build the project:

    ```bash
    mvn clean install
    ```

### Usage

1. Run the Spring Cloud Gateway application:

    ```bash
    java -jar target/api-gateway.jar
    ```

2. Access the gateway endpoints using the configured routes.

## Configuration

The configuration for Spring Cloud Gateway is defined in `application.yml` file. You can customize routes, filters, load balancing settings, and other properties according to your requirements.

## License

This project is licensed under the MIT License - see the [LICENSE](LICENSE) file for details.

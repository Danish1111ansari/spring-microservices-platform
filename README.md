# 🚀 Spring Microservices Platform

A comprehensive microservices ecosystem built with Spring Boot, featuring authentication, API Gateway, event-driven architecture, analytics, and containerization.

![Microservices Architecture](https://img.shields.io/badge/Architecture-Microservices-blue)
![Spring Boot](https://img.shields.io/badge/Spring-Boot-green)
![Docker](https://img.shields.io/badge/Docker-Containerized-blue)
![Kafka](https://img.shields.io/badge/Apache-Kafka-orange)


## 📋 Table of Contents
- [Architecture](#-architecture)
- [Features](#-features)
- [Tech Stack](#-tech-stack)
- [Quick Start](#-quick-start)
- [Services](#-services)
- [API Documentation](#-api-documentation)
- [Development](#-development)
- [Configuration](#-configuration)
- [Contributing](#-contributing)
- [License](#-license)
- [Authors](#-authors)
- [Acknowledgments](#-acknowledgments)


## 🏗️ Architecture

```mermaid
graph TB
    CL[Client] --> GW[API Gateway]
    GW --> AUTH[Auth Service]
    GW --> PATIENT[Patient Service]
    GW --> BILLING[Billing Service]
    GW --> ANALYTICS[Analytics Service]
    
    AUTH --> KAFKA[Kafka]
    PATIENT --> KAFKA
    BILLING --> KAFKA
    KAFKA --> ANALYTICS
    
    PATIENT --> POSTGRES[(PostgreSQL)]
    BILLING --> POSTGRES
    AUTH --> POSTGRES
    ANALYTICS --> POSTGRES
    
    style GW fill:#e1f5fe
    style AUTH fill:#f3e5f5
    style PATIENT fill:#e8f5e8
    style BILLING fill:#fff3e0
    style ANALYTICS fill:#fff0f0```


    ## ✨ Features

| Feature | Description | Status |
|---------|-------------|--------|
| 🔐 **JWT Authentication** | Secure token-based authentication with role-based access | ✅ Implemented |
| 🚪 **API Gateway** | Single entry point with dynamic routing & JWT validation | ✅ Implemented |
| 📡 **gRPC Integration** | High-performance RPC communication between services | ✅ Implemented |
| 🔄 **Event-Driven Architecture** | Kafka for asynchronous communication & event streaming | ✅ Implemented |
| 📊 **Real-time Analytics** | Kafka consumer for data processing & business insights | ✅ Implemented |
| 🐳 **Docker Containerization** | Full containerization with Docker Compose | ✅ Implemented |
| 🗄️ **Multi-Database Support** | PostgreSQL for different service data storage | ✅ Implemented |
| 🔒 **Role-based Authorization** | Fine-grained access control with user roles | ✅ Implemented |
| 📈 **Data Streaming** | Real-time data processing from multiple sources | ✅ Implemented |
| 🛡️ **Spring Security** | Comprehensive security configuration | ✅ Implemented |
| 🔍 **Service Discovery** | Dynamic service registration and discovery | ✅ Implemented |
| 📝 **API Documentation** | Comprehensive API docs with OpenAPI | ✅ Implemented |


## 🛠️ Tech Stack

### 🎯 Backend Framework
- **Spring Boot 3.x** - Main application framework
- **Spring Security 6.x** - Authentication & authorization
- **Spring Cloud Gateway** - API Gateway implementation
- **Spring for Apache Kafka** - Event streaming & messaging
- **Spring Data JPA** - Database operations & ORM
- **Spring gRPC** - High-performance RPC communication

### 💾 Data & Communication
- **PostgreSQL** - Primary relational database
- **Apache Kafka** - Event streaming platform
- **gRPC** - Inter-service communication
- **JWT (JJWT)** - Token-based authentication
- **Liquibase** - Database migration & versioning

### 🐳 Infrastructure & DevOps
- **Docker** - Containerization platform
- **Docker Compose** - Multi-container orchestration
- **Maven** - Dependency management & build tool
- **Java 21** - Primary programming language

### 📡 Messaging & Events
- **Kafka Streams** - Real-time stream processing
- **Spring Cloud Stream** - Event-driven microservices
- **Avro Schema** - Efficient data serialization

### 🔧 Development Tools
- **Lombok** - Reduced boilerplate code
- **MapStruct** - Object mapping library
- **JUnit 5** - Unit testing framework
- **Testcontainers** - Integration testing
- **JaCoCo** - Code coverage reporting

### 🎨 Frontend & API
- **REST APIs** - Standard HTTP endpoints
- **OpenAPI 3** - API documentation
- **gRPC Protobuf** - Protocol buffer definitions


# Spring Boot Microservices Project with Config Server, MySQL, MongoDB, and Resilience4j

This project is a **Spring Boot microservices-based application** built using **Java 17** and **Spring Boot 3.5.3**, demonstrating:

* Service decoupling
* Centralized configuration
* Resilience and fault tolerance
* RESTful communication
* Robust validation and exception handling

---

## Microservices Included

### ⚙️ Config Server

* Uses **Spring Cloud Config Server**
* Loads centralized `application.yml` from a **GitHub-backed remote repository**
* Supplies configuration to all microservices dynamically

### 👤 User Service

* Java 17 + Spring Boot + Spring Data JPA
* Stores user data in **MySQL**
* Implements full **CRUD operations**
* Configuration loaded via Config Server
* Structured validation using DTO (`UserRequest`)
* Custom `ApiResponse` for successful responses
* Global exception handler

### 📦 Product Service

* Java 17 + Spring Boot + Spring Data MongoDB
* Stores product data in **MongoDB**
* Full **CRUD operations**
* Integrates **Resilience4j** (Circuit Breaker, Retry, TimeLimiter)
* Uses fallback methods for graceful degradation
* Validates requests via `ProductDTO`
* Config Server integration

---

## Technologies Used

* Spring Boot 3.5.3
* Spring Cloud Config Server
* Spring Data JPA (MySQL)
* Spring Data MongoDB
* Resilience4j (circuit breaker, retry, fallback)
* RESTful APIs (via `RestTemplate`)
* Jakarta Bean Validation
* Global Exception Handling (`@ControllerAdvice`)
* Lombok
* Maven
* GitHub as config repo backend

---

## Features

* ✅ Microservices with isolated responsibilities
* ✅ Externalized configuration using GitHub-backed Config Server
* ✅ Centralized error and success response structure
* ✅ Input validation using DTO classes
* ✅ Resilience and fault tolerance with fallback
* ✅ Clean folder structure and modular design

---

## Project Structure

```
spring-microservices-project/
├── config-server/
├── user-service/
├── product-service/
├── config-repo/ (GitHub-linked external config files)
└── README.md
```

---

## Getting Started

1. Clone the repository and set up MongoDB and MySQL
2. Run the **config-server**
3. Start **user-service** and **product-service**
4. Test endpoints via **Postman or browser**
5. Simulate MongoDB/MySQL failure to test **fallbacks**

---

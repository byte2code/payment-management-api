# Payment Management API

Spring Boot REST API for managing payment records with JPA, MySQL persistence, layered DAL/service design, and custom exception handling.

## Overview

This project demonstrates a compact Spring Boot payment-management API built with a layered architecture. It is designed as a learning project that shows how a controller, service layer, and DAL implementation can work together with JPA and Hibernate to store and retrieve payment records from a relational database.

## Concepts and Features Covered

- Spring Boot REST API setup
- JPA and Hibernate-based persistence
- Layered controller, service, and DAL design
- `GET` endpoint for retrieving a payment by ID
- `GET` endpoint for listing all payments
- `GET` endpoint for filtering payments by type
- `GET` endpoint for searching payments by description keyword
- `POST` endpoint for saving a payment
- Custom exception handling for missing, duplicate, and invalid input cases

## Tech Stack

- Java 17
- Spring Boot 3
- Spring Web
- Spring Data JPA
- Hibernate
- MySQL
- Maven
- JUnit 5

## Project Structure

```text
payment-management-api/
├── CHANGELOG.md
├── README.md
├── pom.xml
├── mvnw
├── mvnw.cmd
└── src/
    └── main/
        ├── java/com/cn/cnpayment/
        │   ├── controller/
        │   ├── dal/
        │   ├── entity/
        │   ├── exception/
        │   ├── service/
        │   └── CnPaymentApplication.java
        └── resources/
            └── application.yml
```

## How to Run

1. Open a terminal in the project root.
2. Update the MySQL connection values in `src/main/resources/application.yml` if needed.
3. Run `./mvnw test`.
4. Run `./mvnw spring-boot:run`.
5. Use the API under `http://localhost:8080/payment`.

Available endpoints:

- `GET /payment/id/{id}`
- `GET /payment/allPayments`
- `GET /payment/paymentType/{paymentType}`
- `GET /payment/description/{keyword}`
- `POST /payment/save`

Example request body:

```json
{
  "id": 1,
  "paymentType": "Credit",
  "description": "Online order payment"
}
```

## Learning Highlights

- Demonstrates how to separate persistence concerns into a dedicated DAL layer
- Shows how Hibernate sessions can be used through `EntityManager`
- Introduces custom exceptions for not-found, duplicate, and invalid-input scenarios
- Connects a simple REST API to a real MySQL-backed persistence flow

## GitHub Metadata

- Suggested repository description: `Spring Boot REST API for payment record management with JPA, MySQL persistence, layered DAL/service design, and custom exception handling.`
- Suggested topics: `java`, `java-17`, `spring-boot`, `spring-data-jpa`, `hibernate`, `mysql`, `rest-api`, `payment-management`, `maven`, `learning-project`, `portfolio-project`

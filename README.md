# Online Platform Buy&Sell EHA Pro Microservice

## Overview
**Online Platform Buy&Sell EHA Pro Microservice** is a scalable e-commerce platform designed for buying and selling products. Built using a microservice architecture, this platform offers modular, independently scalable services, such as user authentication, product catalog, shopping cart, and order management.

## Architecture
The project follows a microservices architecture where each core feature (user management, product catalog, etc.) is a separate service, independently deployable and scalable. Below is an initial high-level system architecture (detailed diagrams will be added as development progresses).

### System Boundary Architecture - Microservices Landscape
(*Diagrams will be added soon to visualize service interactions, API Gateway flow, and database architecture.*)

## Key Features
- **Microservice Architecture**: Separate, independently scalable services for each core function.
- **User Authentication**: Secure login and registration using JWT.
- **Product Catalog**: Search, filter, and browse products by category.
- **Shopping Cart**: Add, update, and remove items from the cart.
- **Order Management**: Place orders, track order status and history.
- **API Gateway**: A centralized entry point for managing API requests and routing them to appropriate services.
- **Service Discovery**: Dynamic service discovery for load balancing and fault tolerance.

## Technologies Used
- **Java** and **Kotlin**: Core languages for backend services.
- **Spring Boot**: To build and manage services.
- **Spring Cloud**: For service discovery and configuration management.
- **React**: For the frontend interface (planned).
- **PostgreSQL**: Primary relational database.
- **MongoDB**: NoSQL database for storing product images and reviews.
- **Hibernate**: For ORM support.
- **JWT**: For secure user authentication.
- **Eureka**: Service registry and discovery.
- **API Gateway**: Central entry point for client requests.
- **Docker**: Containerization of services.
- **AWS**: For hosting and deploying services (planned).

## Tech Stack
- **Backend**:
    - **Java 17**: Primary programming language.
    - **Spring Boot**: Core framework for developing microservices.
    - **Spring Cloud**: Enables service discovery, API Gateway, and centralized configuration.
    - **Spring Security**: Provides security for microservices, including JWT-based authentication.
- **Databases**:
    - **PostgreSQL**: Relational database for structured data.
    - **MongoDB**: NoSQL database for storing unstructured or semi-structured data.
- **Build and Deployment**:
    - **Maven**: Build and dependency management tool.
    - **Docker**: Containerization for scalable deployment.
- **Testing**:
    - **JUnit** and **MockMVC**: For unit and integration tests.
    - **Testcontainers** (planned): For containerized integration testing with databases.

## Planned Functionalities
- **Multi-language support** for international users.
- **OAuth2 Integration**: To allow login with third-party providers (Google, Facebook, etc.).
- **Resilience4J**: For circuit breaker pattern and fault tolerance.
- **Caching with Redis**: For faster response times on frequently accessed data.
- **Centralized Logging and Monitoring**: Using ELK stack (Elasticsearch, Logstash, and Kibana) and Prometheus/Grafana for metrics.
- **CI/CD Pipeline**: Automated deployment and testing setup with GitHub Actions.

## Microservices Overview

The platform consists of multiple independent microservices, each responsible for a specific part of the application’s functionality:

1. **User Service**:
    - Handles user registration, login, profile management.
    - Integrates JWT-based authentication with Spring Security.

2. **Product Catalog Service**:
    - Manages product information, including categories, descriptions, and pricing.
    - Provides search and filtering options for users.

3. **Shopping Cart Service**:
    - Allows users to add, update, and remove items from their shopping cart.
    - Calculates total price based on cart contents.

4. **Order Service**:
    - Manages order creation, status tracking, and order history.
    - Integrates with the Payment Service for order payments.

5. **Payment Service**:
    - Processes payments and interacts with third-party payment providers.
    - Ensures secure handling of payment data.

6. **Recommendation Service** (optional):
    - Provides personalized recommendations based on user history and preferences.
    - Uses data from Order Service and Product Catalog Service.

7. **Notification Service**:
    - Sends notifications for order updates, promotions, and other events.
    - Integrates with other services for real-time messaging.

8. **Admin Service**:
    - Allows administrators to manage users, products, and orders.
    - Restricted access for authorized admin roles only, with enhanced security.

This structure enables scalability, fault tolerance, and flexibility, allowing each service to be independently deployed and scaled.

### Current Database Structure
The following tables are currently part of our database schema:
- **Products**: Stores product information.
- **Categories**: Manages product categories.
- **Users**: Holds user account details.
- **Orders**: Stores order information.
- **Order Items**: Manages items within each order.

## Getting Started
### Prerequisites
- **Java 17**
- **Maven**
- **Docker** (for containerized deployment)

### Setup
1. Clone the repository:
 ```bash
   git clone <git@github.com:emrahhakanagan/Online-Platform-Buy-Sell-EHA-Pro-Microservice.git>
 ```


2. Navigate to the project directory:
```bash
   cd buyandsell-eha-pro-microservice
 ```

3. Build the project:
```bash
  mvn clean install
 ```

4. Run the application:
```bash
  mvn spring-boot:run
 ```

## Future Improvements
* Scalability Enhancements: Kubernetes integration for orchestration.
* Advanced Security: Role-based access control (RBAC) and two-factor authentication (2FA).
* Analytics and Insights: Adding dashboards for analyzing customer behavior and platform usage trends.
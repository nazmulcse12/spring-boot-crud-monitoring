# Spring Boot CRUD Application

This project is a simple CRUD (Create, Read, Update, Delete) application built with Spring Boot and an H2 in-memory database. It provides a RESTful API for managing `Product` entities.

## Project Structure

```
spring-boot-crud-app
├── src
│   └── main
│       ├── java
│       │   └── com
│       │       └── example
│       │           └── crudapp
│       │               ├── CrudAppApplication.java
│       │               ├── controller
│       │               │   └── ProductController.java
│       │               ├── entity
│       │               │   └── Product.java
│       │               ├── repository
│       │               │   └── ProductRepository.java
│       │               └── service
│       │                   └── ProductService.java
│       └── resources
│           ├── application.yml
│           ├── data.sql
│           └── schema.sql
├── docker
│   ├── grafana
│   │   └── dashboards
│   │       └── spring-boot-dashboard.json
│   └── prometheus
│       └── prometheus.yml
├── target
├── Dockerfile
├── docker-compose.yml
├── pom.xml
└── README.md
```

## Features

- **CRUD Operations**: Create, read, update, and delete products.
- **H2 Database**: Uses an in-memory H2 database for data storage.
- **Docker Support**: Easily deploy the application using Docker.
- **Monitoring**: Integrates with Prometheus and Grafana for monitoring application metrics.

## Getting Started

### Prerequisites

- Java 17 or higher
- Maven
- Docker and Docker Compose

### Build the Application

1. Clone the repository:
   ```
   git clone <repository-url>
   cd spring-boot-crud-app
   ```

2. Build the application using Maven:
   ```
   mvn clean package
   ```

### Run the Application with Docker

1. Start the services using Docker Compose:
   ```
   docker-compose up --build
   ```

2. Access the application at `http://localhost:8080`.

3. Access Prometheus at `http://localhost:9090`.

4. Access Grafana at `http://localhost:3000` (default login: admin/admin).

### API Endpoints

- **Create Product**: `POST /products`
- **Get All Products**: `GET /products`
- **Get Product by ID**: `GET /products/{id}`
- **Update Product**: `PUT /products/{id}`
- **Delete Product**: `DELETE /products/{id}`

## License

This project is licensed under the MIT License. See the LICENSE file for details.
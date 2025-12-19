# EasyShop API

## Overview

EasyShop is a e-commerce backend API built with **Spring Boot**, **MySQL**, and **JWT-based authentication**. The API focuses on secure user authentication, role-based authorization, and full CRUD functionality for categories and products.

This project was developed as part of the **Year Up United Capstone Program** and is designed to demonstrate backend development practices, including dependency injection and API testing.

---

## Tech Stack

* Java 11+
* Spring Boot
* Spring Security (JWT Authentication)
* MySQL 8.0+
* Maven
* Insomnia (API testing)

---

## Setup Instructions

### Prerequisites

* Java 11 or higher
* MySQL 8.0 or higher
* Maven
* IntelliJ IDEA (or any Java IDE)

### Database Setup

1. Create the database:

```sql
CREATE DATABASE easyshop;
```

2. Update `application.properties`:

```properties
spring.datasource.url=jdbc:mysql://localhost:3306/easyshop
spring.datasource.username=your_username
spring.datasource.password=your_password
```

---

## Running the Application

1. Clone the repository
2. Open the project in IntelliJ IDEA
3. Run `EasyshopApplication.java`
4. The API will start at:

```
http://localhost:8080
```

---

## API Endpoints

### Authentication

| Method | Endpoint  | Description                   |
| ------ | --------- | ----------------------------- |
| POST   | /register | Register a new user           |
| POST   | /login    | Login and receive a JWT token |

### Categories

| Method | Endpoint         | Access     |
| ------ | ---------------- | ---------- |
| GET    | /categories      | Public     |
| GET    | /categories/{id} | Public     |
| POST   | /categories      | Admin only |
| PUT    | /categories/{id} | Admin only |
| DELETE | /categories/{id} | Admin only |

### Products

| Method | Endpoint       | Access     |
| ------ | -------------- | ---------- |
| GET    | /products      | Public     |
| GET    | /products/{id} | Public     |
| POST   | /products      | Admin only |
| PUT    | /products/{id} | Admin only |
| DELETE | /products/{id} | Admin only |

#### Optional Query Parameters

* `cat` – Category ID
* `minPrice`
* `maxPrice`
* `subCategory`

---

## Authentication & Authorization

Admin endpoints require a valid JWT token.

### Admin Login Example

```json
POST /login
{
  "username": "admin",
  "password": "password"
}
```

### Authorization Header

```
Authorization: Bearer {your_token}
```

---

## Testing

Insomnia collection used to validate all API endpoints with successful responses

* User registration and login
* JWT authentication and authorization
* Category CRUD operations
* Product CRUD operations

✅ **All required tests passing**

---

## Screenshots

### Insomnia Test Results

Example:

<img width="987" height="808" alt="Screenshot 2025-12-19 at 8 05 46 AM" src="https://github.com/user-attachments/assets/c0c5b699-279f-474b-a40a-1293d91e44aa" />



src="https://github.com/user-attachments/assets/810e1d5b-924c-42a4-a1bd-b70a488b599a" />

/screenshots/insomnia-tests.png
```

### Application Startup

// screenshot of the Spring Boot application running successfully in IntelliJ.

```


---


```

---

## Known Issues

* Product images may not display (image assets not included)
* This does not affect API functionality


---


## Acknowledgments

* Year Up United
* Capstone project starter code and requirements

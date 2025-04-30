# 4.02 Level 1 - CRUD with H2 Database

## Overview

This project demonstrates the implementation of a simple **CRUD** application using **Spring Boot** and an **H2 database**. The application performs operations on an entity called "Fruita" (Fruit), following the **MVC (Model-View-Controller)** design pattern. 

---

## 📦 Project Setup

Generate the Spring Boot project using (https://start.spring.io/) with the following configuration:

- **Project**: Maven or Gradle
- **Language**: Java
- **Spring Boot Version**: Latest stable release
- **Group**: `cat.itacademy.s04.t02.n01`
- **Artifact**: `S04T02N01`
- **Name**: `S04T02N01`
- **Description**: `S04T02N01GognomsNom`
- **Package Name**: `cat.itacademy.s04.t02.n01`
- **Packaging**: Jar
- **Java Version**: 11 (minimum)

### Dependencies

- Spring Web
- Spring Boot DevTools
- Spring Data JPA
- H2 Database

---

## ⚙️ Configuration

In the `application.properties` file (located in `src/main/resources`), add the following configuration for the H2 database:

```properties
spring.datasource.url=jdbc:h2:mem:testdb
spring.datasource.driverClassName=org.h2.Driver
spring.datasource.username=sa
spring.datasource.password=password
spring.jpa.database-platform=org.hibernate.dialect.H2Dialect
spring.h2.console.enabled=true
```

This configuration sets up an in-memory H2 database and enables the H2 console for easy access to the database.

---

## 📂 Project Structure

The project follows the MVC pattern, and the following package structure is used:

```
cat.itacademy.s04.t02.n01
├── controllers
├── model
├── services
├── repository
└── exception
```

- Controllers: `cat.itacademy.s04.t02.n01.controllers`
- Model: `cat.itacademy.s04.t02.n01.model`
- Services: `cat.itacademy.s04.t02.n01.services`
- Repository: `cat.itacademy.s04.t02.n01.repository`
- Exceptions: `cat.itacademy.s04.t02.n01.exception`

---

## 🛠️ CRUD Operations

The application exposes the following endpoints for CRUD operations:

### 1. Add a new fruit

- Method: `POST`
- URL: `/fruita/add`

This endpoint accepts a POST request to add a new fruit to the database.

### 2. Update a fruit
   
- Method: `PUT`
- URL: `/fruita/update`

This endpoint accepts a PUT request to update the details of an existing fruit.

### 3. Delete a fruit

- Method: `DELETE`
- URL: `/fruita/delete/{id}`

This endpoint accepts a DELETE request to remove a fruit from the database, where {id} is the ID of the fruit to delete.

### 4. Get a fruit by ID

- Method: `GET`
- URL: `/fruita/getOne/{id}`

This endpoint accepts a GET request to retrieve a specific fruit by its ID.

### 5. Get all fruits

- Method: `GET`
- URL: `/fruita/getAll`


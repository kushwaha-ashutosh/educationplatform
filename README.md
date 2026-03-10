# 🎓 Online Education Platform

> A full-stack online education platform built with **Spring Boot** that enables students to access courses, instructors to manage learning content, and administrators to manage the system efficiently.

---

## 📋 Table of Contents

- [Overview](#overview)
- [Features](#features)
- [Architecture](#architecture)
- [Tech Stack](#tech-stack)
- [Installation](#installation)
- [Configuration](#configuration)
- [API Endpoints](#api-endpoints)
- [Learning Objectives](#learning-objectives)
- [Contributing](#contributing)
- [License](#license)

---

## 📖 Overview

This project demonstrates backend development concepts such as REST APIs, authentication, database management, and scalable application architecture. It provides a robust backend system for managing online courses, users, and enrollments.

---

## 🚀 Features

- 🔐 **User Authentication & Authorization** — Secure login and role-based access control
- 📚 **Course Management System** — Create, update, and organize course content
- 🎯 **Student Enrollment & Progress Tracking** — Track learning milestones and completion
- 🧑‍🏫 **Instructor Dashboard** — Manage and publish courses effortlessly
- 🔒 **Secure Backend API** — Protected endpoints with proper authentication
- 🗄️ **Database-Driven Management** — Efficient storage and retrieval of course and user data

---

## 🏗️ Architecture

```
Client (Frontend)
        │
        ▼
Spring Boot REST API
        │
        ▼
   Service Layer
        │
        ▼
  Database (MySQL)
```

The application follows a layered architecture:

| Layer | Responsibility |
|---|---|
| **Controller** | Handles HTTP requests and routes them appropriately |
| **Service** | Contains business logic and orchestrates operations |
| **Repository** | Manages data persistence via JPA/Hibernate |
| **Database** | MySQL stores all application data |

---

## ⚙️ Tech Stack

| Category | Technology |
|---|---|
| **Backend** | Spring Boot |
| **Language** | Java |
| **Database** | MySQL |
| **ORM** | JPA / Hibernate |
| **Build Tool** | Maven |
| **API Type** | RESTful APIs |

---

## 📦 Installation

### Prerequisites

- Java 17+
- Maven 3.6+
- MySQL 8.0+

### Steps

**1. Clone the repository**

```bash
git clone https://github.com/kushwaha-ashutosh/educationplatform.git
```

**2. Navigate to the project directory**

```bash
cd educationplatform
```

**3. Configure database settings**

Update `src/main/resources/application.properties` with your database credentials (see [Configuration](#configuration)).

**4. Run the project**

```bash
mvn spring-boot:run
```

The application will start at `http://localhost:8080`.

---

## 🔧 Configuration

Edit `src/main/resources/application.properties`:

```properties
# Database Configuration
spring.datasource.url=jdbc:mysql://localhost:3306/educationplatform
spring.datasource.username=your_username
spring.datasource.password=your_password
spring.datasource.driver-class-name=com.mysql.cj.jdbc.Driver

# JPA / Hibernate
spring.jpa.hibernate.ddl-auto=update
spring.jpa.show-sql=true
spring.jpa.properties.hibernate.dialect=org.hibernate.dialect.MySQL8Dialect

# Server Port
server.port=8080
```

---

## 📡 API Endpoints

### Authentication

| Method | Endpoint | Description |
|---|---|---|
| `POST` | `/api/auth/register` | Register a new user |
| `POST` | `/api/auth/login` | Authenticate and get token |

### Courses

| Method | Endpoint | Description |
|---|---|---|
| `GET` | `/api/courses` | Get all courses |
| `GET` | `/api/courses/{id}` | Get course by ID |
| `POST` | `/api/courses` | Create a new course |
| `PUT` | `/api/courses/{id}` | Update a course |
| `DELETE` | `/api/courses/{id}` | Delete a course |

### Enrollments

| Method | Endpoint | Description |
|---|---|---|
| `POST` | `/api/enrollments` | Enroll in a course |
| `GET` | `/api/enrollments/student/{id}` | Get enrollments by student |
| `PUT` | `/api/enrollments/{id}/progress` | Update progress |

---

## 📚 Learning Objectives

This project demonstrates:

- ✅ Backend application development using **Spring Boot**
- ✅ **REST API** design and best practices
- ✅ Database integration with **JPA/Hibernate**
- ✅ **Role-based access control** and authentication
- ✅ Scalable and maintainable application architecture

---

## 🤝 Contributing

Contributions are welcome! Here's how to get started:

1. **Fork** the repository
2. Create a new branch: `git checkout -b feature/your-feature-name`
3. Make your changes and **commit**: `git commit -m 'Add some feature'`
4. **Push** to the branch: `git push origin feature/your-feature-name`
5. Open a **Pull Request**

Feel free to open [issues](https://github.com/kushwaha-ashutosh/educationplatform/issues) for bugs or feature requests.

---

## 📄 License

This project is open source and available under the [MIT License](LICENSE).

---

<p align="center">Made with ❤️ by <a href="https://github.com/kushwaha-ashutosh">Ashutosh Kushwaha</a></p>

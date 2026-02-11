Secure Employee Management REST API
------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------

Spring Boot + Data JPA + MySQL + Spring Security

A fully secured RESTful Employee Management API developed using modern Spring technologies. The application demonstrates CRUD operations, database integration, and HTTP Basic Authentication security implementation.

------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------
# 🚀 Technologies Used


»Spring Boot 4

»Spring Data JPA

»Hibernate (ORM)

»MySQL Database

»Spring Security (Basic Authentication)

»Lombok

»Postman (API Testing)

-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------

# 📖 Application Overview



This project is designed to showcase:

»RESTful API development using Spring Boot

»CRUD operations with Spring Data JPA

»MySQL database connectivity

»Secure API endpoints using Spring Security

»Clean layered architecture implementation

»All REST endpoints are protected using HTTP Basic Authentication.

------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------

# 🏛️ Application Architecture


The project follows a structured layered architecture:

Controller  →  Service  →  Repository  →  Database


## 🔹 Controller Layer

»Handles incoming HTTP requests

»Returns appropriate HTTP responses



## 🔹 Service Layer

»Contains business logic

»Acts as a bridge between Controller and Repository



## 🔹 Repository Layer

Extends JpaRepository

Performs CRUD operations on the database



## 🔹 Entity Layer

»Maps Java classes to database tables using JPA annotations

-------------------------------------------

# 🗄️ Database Configuration


### Step 1: Create Database

` ` `
CREATE DATABASE springbootdatajparestsecurity;
` ` `

### Step 2: Configure application.properties
spring.datasource.url=jdbc:mysql://localhost:3306/springbootdatajparestsecurity
spring.datasource.username=root
spring.datasource.password=your_password

spring.jpa.hibernate.ddl-auto=update
spring.jpa.show-sql=true
spring.jpa.database-platform=org.hibernate.dialect.MySQLDialect

-----

# 🔒 Spring Security Setup
@Configuration
@EnableWebSecurity
public class SecurityConfig {

    @Bean
    public SecurityFilterChain securityFilterChain(HttpSecurity http) throws Exception {
        http.authorizeHttpRequests(auth -> auth.anyRequest().authenticated());
        http.csrf(csrf -> csrf.disable());
        http.httpBasic(Customizer.withDefaults());
        return http.build();
    }
}

-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------
# 🔐 Security Highlights

»All API endpoints require authentication

»Implements HTTP Basic Authentication

»CSRF disabled for REST testing

»Spring Boot auto-generates a temporary password at startup

------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------

# Example console output:

Using generated security password: xxxxxxxx-xxxx-xxxx

Default Credentials (Generated at Runtime)

Username: user

Password: Generated password shown in console

--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------

# 🌐 REST API Base URL
` ` `
http://localhost:8080/api
` ` `

------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------
# FINAL OUTPUTS:


### 1️⃣ Add Employee

POST /api/add

<img width="1443" height="831" alt="image" src="https://github.com/user-attachments/assets/ce037831-16c2-4802-9c53-30d02eb0033a" />


### 2️⃣ Update Employee
PUT /api/update?empId=1

<img width="1442" height="796" alt="image" src="https://github.com/user-attachments/assets/a7f4b69f-33a2-43ac-93bf-49443e017d85" />

### 3️⃣ Get All Employees
GET /api/getall

<img width="1443" height="880" alt="image" src="https://github.com/user-attachments/assets/88206fbe-975b-4668-9748-0929dfe7dca2" />

### 4️⃣Delete Employee
DELETE /api/delete/{id}
<img width="1439" height="835" alt="image" src="https://github.com/user-attachments/assets/184e8a27-05b9-4b87-8d7c-ca6cdf69bdbe" />


# 🔐 Secure Employee Management REST API

A fully secured RESTful Employee Management API built using Spring Boot and modern backend technologies.

---

## 🛠 Technologies Used

| Technology        | Purpose                     |
|-------------------|----------------------------|
| Spring Boot       | Application framework      |
| Spring Data JPA   | Database interaction       |
| Hibernate         | ORM                        |
| MySQL             | Database                   |
| Spring Security   | Authentication             |
| Lombok            | Boilerplate reduction      |
| Postman           | API Testing                |

---

## ▶️ How To Run

### 1️⃣ Clone Repository
git clone https://github.com/your-username/project-name.git


### 2️⃣ Create MySQL Database
CREATE DATABASE springbootdatajparestsecurity;

### 3️⃣ Update Database Credentials
Open application.properties and configure:
spring.datasource.url=jdbc:mysql://localhost:3306/springbootdatajparestsecurity
spring.datasource.username=root
spring.datasource.password=your_password

### 4️⃣ Run the Application

Run the project using:

IntelliJ / Eclipse
OR Command line:

mvn spring-boot:run

### 5️⃣ Test APIs Using Postman

Enable Basic Authentication and use:
Username: user
Password: Generated password from console

# 🎯 Key Learning Outcomes

»Implemented secure REST APIs

»Integrated Spring Security with HTTP Basic Authentication

»Performed CRUD operations using Spring Data JPA

»Understood layered architecture (Controller → Service → Repository)

»Tested APIs using Postman

#  ⭐ Conclusion
This project demonstrates:

»Spring Boot REST API development
»Secure endpoint configuration
»MySQL database integration
»Complete CRUD functionality


















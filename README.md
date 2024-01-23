# JwtLogin - Java Spring Boot Authentication with JWT Tokens

## Overview

JwtLogin is a Java Spring Boot project that provides a secure authentication mechanism using JWT (JSON Web Tokens). The project incorporates Spring Boot, Lombok, JPA, and MySQL to create a robust and scalable authentication system. Instead of traditional application.properties, configuration settings are handled through the application.yaml file.

## Features

- **JWT tokens:** Secure user authentication with JWT tokens
- **User roles:** user, moderator, and admin
- **MySQL:** MySQL database integration
- **CORS:** (Cross-Origin Resource Sharing) enabled for all IP addresses
- **MVC:** (Model-View-Controller) architecture for REST API endpoints
- **Functionality:** Sign in and sign up functionality
- **Filter Chains:** Usage of the latest security technology with Filter Chains

## Prerequisites

Before running the JwtLogin application, ensure you have the following installed:

- Java Development Kit (JDK) 8 or later
- MySQL Database
- Maven

## Installation and Setup

1. Clone the repository:
   
```bash
git clone https://github.com/Dexpomar32/JwtLogin.git
cd JwtLogin
```

2. Configure the database in application.yaml:

```yaml
spring:
  datasource:
    url: jdbc:mysql://localhost:3306/your_database
    username: your_username
    password: your_password
```

3. Adjust other settings in application.yaml for Hibernate and JWT access tokens.
4. Build and run the application using Maven:

```bash
mvn clean install
java -jar target/JwtLogin-1.0-SNAPSHOT.jar
```

5. Access the application at http://localhost:8080.

## Configuration

- `application.yaml:` Handles general application settings, database configuration, Hibernate properties, and JWT access token settings.
- `WebConfig class:` Enables CORS for all IP addresses.

## Security Configuration

- `WebSecurityConfig class:` Configures and enables authentication using the latest security technology with Filter Chains.

## API Endpoints

The REST API follows the MVC architecture and provides the following endpoints:

- **POST /auth/signup:** Sign up a new user.
- **POST /auth/signin:** Sign in with valid credentials.

## Usage

1. Sign up for a new account using the `/auth/signup` endpoint.
2. Sign in with your credentials using the `/auth/signin` endpoint.
3. Access other secured endpoints based on your assigned role (user, moderator, or admin).

## License

This project is licensed under the [MIT License](LICENSE), making it open and free for anyone to use and modify.

## Contributing

Contributions are welcome! Feel free to open issues or submit pull requests to improve `JwtLogin`.

# Spring Boot Book API

A simple REST API for managing books built with Spring Boot. This project demonstrates the basic setup of a Spring Boot application with REST endpoints and JPA integration.

## Features

- CRUD operations for books
- In-memory H2 database
- RESTful endpoints
- Spring Data JPA integration
- Basic error handling

## Tech Stack

- Java 23
- Spring Boot 3.4.0
- Spring Data JPA
- H2 Database
- Maven

## Project Structure

```
src
├── main
│   ├── java
│   │   └── com
│   │       └── example
│   │           └── bookapi
│   │               ├── BookapiApplication.java
│   │               ├── controller
│   │               │   └── BookController.java
│   │               ├── model
│   │               │   └── Book.java
│   │               └── repository
│   │                   └── BookRepository.java
│   └── resources
│       └── application.properties
└── test
    └── java
        └── com
            └── example
                └── bookapi
                    └── BookapiApplicationTests.java
```

## Prerequisites

Before you begin, ensure you have met the following requirements:

- Java Development Kit (JDK) 23 or later
- Maven 3.6.x or later
- Your favorite IDE (IntelliJ IDEA, Eclipse, or VS Code)

## Getting Started

### Clone the Repository

```bash
git clone https://github.com/yourusername/spring-boot-book-api.git
cd spring-boot-book-api
```

### Build the Project

```bash
mvn clean install
```

### Run the Application

```bash
mvn spring-boot:run
```

The application will start on `http://localhost:8080`

## API Endpoints

### Get All Books
```
GET /api/books
```

Response:
```json
[
    {
        "id": 1,
        "title": "Spring Boot in Action",
        "author": "Craig Walls",
        "isbn": "978-1617292545"
    }
]
```

### Get a Single Book
```
GET /api/books/{id}
```

Response:
```json
{
    "id": 1,
    "title": "Spring Boot in Action",
    "author": "Craig Walls",
    "isbn": "978-1617292545"
}
```

### Create a New Book
```
POST /api/books
Content-Type: application/json

{
    "title": "Spring Boot in Action",
    "author": "Craig Walls",
    "isbn": "978-1617292545"
}
```

## Database

The application uses an H2 in-memory database. You can access the H2 console at:
```
http://localhost:8080/h2-console
```

Connection details:
- JDBC URL: `jdbc:h2:mem:bookdb`
- Username: `sa`
- Password: (leave empty)

## Running Tests

```bash
mvn test
```

## Contributing

1. Fork the repository
2. Create your feature branch (`git checkout -b feature/amazing-feature`)
3. Commit your changes (`git commit -m 'Add some amazing feature'`)
4. Push to the branch (`git push origin feature/amazing-feature`)
5. Open a Pull Request

## License

This project is licensed under the MIT License - see the [LICENSE.md](LICENSE.md) file for details.

## Acknowledgments

- [Spring Boot Documentation](https://docs.spring.io/spring-boot/docs/current/reference/html/)
- [Spring Data JPA](https://docs.spring.io/spring-data/jpa/docs/current/reference/html/)
- [H2 Database](https://www.h2database.com/html/main.html)

## Contact

Project Link: [https://github.com/erik-ng-3006/springbootdemo](https://github.com/erik-ng-3006/springbootdemo)
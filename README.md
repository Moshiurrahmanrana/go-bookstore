# Go Bookstore API

A simple RESTful API for managing a bookstore built with Go (Golang). This project demonstrates basic CRUD operations using Go, Gorilla Mux for routing, and a database backend.

## Features

- Create, Read, Update, and Delete (CRUD) operations for books
- RESTful API endpoints
- JSON request/response handling
- Database integration

## Prerequisites

Before you begin, ensure you have the following installed:
- Go (version 1.16 or higher)
- Git
- A database system (the project uses GORM, which supports multiple databases)

## Getting Started

1. Clone the repository:
```bash
git clone https://github.com/moshiurrahmanrana/go-bookstore.git
cd go-bookstore
```

2. Install dependencies:
```bash
go mod download
```

3. Configure your database connection in the appropriate configuration file.

4. Run the application:
```bash
go run main.go
```

The server will start on `http://localhost:8080`

## API Endpoints

### Books

- `GET /book` - Get all books
- `GET /book/{bookId}` - Get a specific book by ID
- `POST /book` - Create a new book
- `PUT /book/{bookId}` - Update a book
- `DELETE /book/{bookId}` - Delete a book

### Example Request

To create a new book:
```bash
curl -X POST http://localhost:8080/book \
-H "Content-Type: application/json" \
-d '{
    "name": "The Go Programming Language",
    "author": "Alan A. A. Donovan",
    "publication": "Addison-Wesley"
}'
```

## Project Structure

```
go-bookstore/
├── pkg/
│   ├── controllers/    # HTTP request handlers
│   ├── models/         # Database models
│   └── utils/          # Utility functions
├── main.go            # Application entry point
└── README.md          # This file
```

## Contributing

1. Fork the repository
2. Create your feature branch (`git checkout -b feature/amazing-feature`)
3. Commit your changes (`git commit -m 'Add some amazing feature'`)
4. Push to the branch (`git push origin feature/amazing-feature`)
5. Open a Pull Request

## License

This project is licensed under the MIT License - see the LICENSE file for details.

## Acknowledgments

- [Gorilla Mux](https://github.com/gorilla/mux) for routing
- [GORM](https://gorm.io/) for database operations

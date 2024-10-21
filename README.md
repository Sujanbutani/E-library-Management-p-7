# E-Library Management API

This is the backend API for the E-Library Management Application built with Node.js, Express, and MongoDB. The application allows users to manage books, borrow/return them, and handle user authentication with JWT tokens.

## Features

- User Authentication: Register and login with JWT tokens.
- Book Management: Create, Read, Update, Delete books.
- Borrow/Return Books: Borrow and return books with user tracking.
- MongoDB: Store book data and user information.

## Technologies Used

- Node.js
- Express
- MongoDB
- Mongoose
- JSON Web Token (JWT)
- Bcrypt.js
- dotenv
- nodemon

## Installation

1. Clone the repository:

   ```bash
   git clone https://github.com/Sujanbutani/E-library-Management-p-7.git

2. Install dependencies:

    ```bash
    npm install

3. .env file

     ```
    MONGODB_URI=your_mongo_db_connection_string
    PORT=5000
    JWT_SECRET=your_jwt_secret
    JWT_EXPIRE=token expire time
    ```

4. Start the development server:

   ```bash
   npm start
   The server should now be running at http://localhost:5000
   ```

## API Endpoints

### User Authentication
1. Register User (Post) :- localhost:5000/api/auth/register
2. Login User (Post) :- localhost:5000/api/auth/login

### Book Management
1. Book Api (Post) :- localhost:5000/api/books
    - Requires JWT token in the Authorization header.
2. Book Api (Get - Allevent) :- localhost:5000/api/books/<book_id>
3. Book Api (Update) :- localhost:5000/api/events/<event_Id>
4. Book Api (Delete) :- localhost:5000/api/events/<event_Id>
5. Borrow Api (Post) :- localhost:5000/api/borrow/<book_id>/borrow
6. Return Api (Post) :- localhost:5000/api/borrow/<book_id>/return

## Environment Variables
- PORT: The port for the server to listen on.
- MONGODB_URI: Your MongoDB connection string.
- JWT_SECRET: Secret key for signing JWT tokens.
- JWT_EXPIRE : token expire time.

# Error Handling
- 400 Bad Request: If the required fields are missing or invalid input is provided.
- 404 Not Found: If a requested resource (like a book or user) is not found.
- 500 Internal Server Error: For unexpected server errors.
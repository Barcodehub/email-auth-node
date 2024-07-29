# Authentication System and Password Reset via Email

## Description

This project is a robust backend application developed with Node.js and Express, implementing JWT (JSON Web Token) authentication and user management. It uses MongoDB as a database and offers features such as user registration, login, password recovery, and password reset with email confirmation.

## Configuration

Create a `.env` file in the project root and configure the environment variables (see Configuration section).
  ```
PORT=3000
MONGO_URI=your_mongodb_uri
JWT_SECRET=your_jwt_secret
JWT_EXPIRE=30d
SMTP_HOST=your_smtp_host
SMTP_PORT=your_smtp_port
SMTP_EMAIL=your_email
SMTP_PASSWORD=your_password
FROM_EMAIL=sender_email
FROM_NAME=Your_app_name
  ```
Make sure to replace the values with your specific configuration.

## Usage

The API provides the following endpoints:

- `POST /api/auth/register`: Registers a new user
- `POST /api/auth/login`: Logs in and returns a JWT token
- `POST /api/auth/forgotpassword`: Requests a password reset
- `PUT /api/auth/resetpassword/:resettoken`: Resets the password with a valid token


## Security

- Passwords are hashed before being stored in the database.
- JWT is used for user authentication.
- Password reset tokens have a short expiration for security.


# Secrets App

## Introduction

Secrets is a web application where users can register, log in, and share their secrets anonymously. The application uses Node.js, Express, PostgreSQL, and EJS for the server-side, and bcrypt for hashing passwords.

## Features

- User registration
- User login
- Password hashing for secure authentication
- Session management
- Simple user interface with EJS templates

## Prerequisites

Before you begin, ensure you have met the following requirements:

- Node.js and npm installed
- PostgreSQL installed and running

## Installation

1. Clone the repository:

    ```bash
    git clone https://github.com/yourusername/secrets-app.git
    cd secrets-app
    ```

2. Install the dependencies:

    ```bash
    npm install
    ```

3. Set up the PostgreSQL database:

    ```sql
    CREATE DATABASE secrets;
    \c secrets
    CREATE TABLE users (
        id SERIAL PRIMARY KEY,
        email VARCHAR(255) UNIQUE NOT NULL,
        password VARCHAR(255) NOT NULL
    );
    ```

4. Create a `.env` file in the root directory of the project and add your database credentials:

    ```env
    DB_USER=postgres
    DB_HOST=localhost
    DB_NAME=secrets
    DB_PASS=123456
    DB_PORT=5432
    ```

5. Start the server:

    ```bash
    npm start
    ```

    The server will be running on `http://localhost:3000`.

## Usage

### Home Page

Visit `http://localhost:3000/` to view the home page.

### Registration

Go to `http://localhost:3000/register` to register a new user. Enter your email and password.

### Login

Go to `http://localhost:3000/login` to log in. Enter your registered email and password.

### Secrets

After logging in, you will be redirected to the secrets page where you can view shared secrets.

## Project Structure

secrets-app/

│

├── public/

│ ├── css/

│ └── js/
│
├── views/
│ ├── partials/
│ │ ├── header.ejs
│ │ └── footer.ejs
│ ├── home.ejs
│ ├── login.ejs
│ ├── register.ejs
│ ├── secrets.ejs
│
├── .env
├── app.js
├── package.json
└── README.md

## Code Explanation

### `app.js`

This file sets up the Express server, connects to the PostgreSQL database, and defines the routes for handling user registration and login.

### Views

The `views` directory contains EJS templates for rendering the HTML pages.

- **partials/header.ejs**: The header section included in all pages.
- **partials/footer.ejs**: The footer section included in all pages.
- **home.ejs**: The home page.
- **login.ejs**: The login page.
- **register.ejs**: The registration page.
- **secrets.ejs**: The secrets page, displayed after a successful login.

## Contact

If you have any questions or suggestions, feel free to reach out:

- [Kruthvik k s](mailto:kruthviksgowda19@gmail.com)

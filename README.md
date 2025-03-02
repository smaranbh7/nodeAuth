# Node.js Authentication System

A complete authentication system built with Node.js, Express, Passport.js, and PostgreSQL.

## Features

- User registration with password hashing
- User login with session management
- Protected routes
- Password validation
- PostgreSQL database integration
- Express session handling

## Prerequisites

- Node.js
- PostgreSQL
- npm

## Installation

1. Clone the repository:
```bash
git clone <your-repo-url>
```

2. Install dependencies:
```bash
npm install
```

3. Create a `.env` file in the root directory with the following variables:
```
DB_USER=your_db_user
DB_PASSWORD=your_db_password
DB_HOST=localhost
DB_PORT=5432
DB_DATABASE=nodeauth
SESSION_SECRET=your_session_secret
```

4. Set up the PostgreSQL database:
```sql
CREATE DATABASE nodeauth;
CREATE TABLE users (
  id SERIAL PRIMARY KEY,
  name VARCHAR(200) NOT NULL,
  email VARCHAR(200) NOT NULL,
  password VARCHAR(200) NOT NULL
);
```

5. Start the server:
```bash
npm run dev
```

The application will be running at `http://localhost:3000`

## Routes

- `GET /` - Home page
- `GET /users/login` - Login page
- `GET /users/register` - Registration page
- `GET /users/dashboard` - Protected dashboard
- `POST /users/register` - Register new user
- `POST /users/login` - Authenticate user
- `GET /users/logout` - Logout user

## Technologies Used

- Node.js
- Express.js
- Passport.js
- PostgreSQL
- EJS Templates
- bcrypt
- express-session 
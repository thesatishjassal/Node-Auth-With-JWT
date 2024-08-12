# Node.js Authentication API

## Overview

This Node.js REST API provides user authentication and CRUD operations with JWT-based security. The API includes endpoints for user signup, login, and management, utilizing MongoDB Atlas as the database.

## Features

- User authentication with JWT
- User CRUD operations (Create, Read, Update, Delete)
- Secure password hashing with `bcryptjs`
- Environment configuration with `dotenv`
- Rate limiting and CORS configuration
- HTTP security headers using `helmet`

## Prerequisites

- [Node.js](https://nodejs.org/) (v14.x or higher)
- [MongoDB Atlas](https://www.mongodb.com/cloud/atlas) account
- A text editor or IDE of your choice

## Installation

### Install Dependencies

Install the required Node.js packages:

```bash```
npm install

###  `API_ENDPOINTS.md`

This file details the API endpoints and environment configuration.


### `API_ENDPOINTS.md`

```markdown```
# API Endpoints and Environment Configuration

## API Endpoints

### Authentication Routes

- **Signup**

  - **URL:** `/api/auth`
  - **Method:** `POST`
  - **Body Parameters:**
    - `username` (String): The username of the user.
    - `email` (String): The email of the user.
    - `password` (String): The password of the user.
  - **Description:** Registers a new user and returns a JWT token.

- **Login**

  - **URL:** `/api/auth/login`
  - **Method:** `POST`
  - **Body Parameters:**
    - `email` (String): The email of the user.
    - `password` (String): The password of the user.
  - **Description:** Authenticates the user and returns a JWT token.

### User Management Routes (Protected)

- **Get All Users**

  - **URL:** `/api/users`
  - **Method:** `GET`
  - **Description:** Retrieves all users. Requires JWT authentication.

- **Get User by ID**

  - **URL:** `/api/users/:id`
  - **Method:** `GET`
  - **Description:** Retrieves a user by ID. Requires JWT authentication.

- **Update User**

  - **URL:** `/api/users/:id`
  - **Method:** `PUT`
  - **Body Parameters:**
    - `username` (String): The new username of the user.
    - `email` (String): The new email of the user.
    - `password` (String): The new password of the user (optional).
  - **Description:** Updates user information. Requires JWT authentication.

- **Delete User**

  - **URL:** `/api/users/:id`
  - **Method:** `DELETE`
  - **Description:** Deletes a user by ID. Requires JWT authentication.

## Environment Configuration

Create a `.env` file in the root directory of the project with the following content:

```env
PORT=5000
MONGO_URI=your_mongodb_atlas_connection_string
JWT_SECRET=your_jwt_secret
SESSION_SECRET=your_session_secret

PORT=5000
MONGO_URI=your_mongodb_atlas_connection_string
JWT_SECRET=your_jwt_secret
SESSION_SECRET=your_session_secret

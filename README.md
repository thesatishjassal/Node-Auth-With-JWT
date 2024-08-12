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

```bash
npm install

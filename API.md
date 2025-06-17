# Product API

A RESTful API built with Express.js to manage a collection of products. This project supports full CRUD operations and includes auto-generated Swagger documentation.

## Table of Contents

- [Features](#features)
- [Tech Stack](#tech-stack)
- [Installation](#installation)
- [Running the Server](#running-the-server)
- [API Documentation](#api-documentation)
- [API Endpoints](#api-endpoints)
  - [Get All Products](#1-get-all-products)
  - [Get Product by ID](#2-get-product-by-id)
  - [Create a Product](#3-create-a-new-product)
  - [Update a Product](#4-update-a-product)
  - [Delete a Product](#5-delete-a-product)
- [License](#license)
- [Contact](#contact)

---

## Features

- Get all products
- Retrieve a specific product by ID
- Add a new product
- Update an existing product
- Delete a product
- Interactive API docs via Swagger UI

## Tech Stack

- [Node.js](https://nodejs.org/)
- [Express.js](https://expressjs.com/)
- [Swagger UI](https://swagger.io/tools/swagger-ui/)
- [UUID](https://www.npmjs.com/package/uuid)

---

## Installation

```bash
git clone https://github.com/PLP-MERN-Stack-Development/week-2-express-js-assignment-Majmajiro.git
cd product-api
npm install

## Running the Server
npm start

API Base URL: http://localhost:3000
Swagger Docs: http://localhost:3000/api-docs

API Documentation

Swagger UI is available at /api-docs, which documents all endpoints, parameters, request bodies, and responses.

API Endpoints

1. Get All Products
Request:
GET /api/products

Response:
[
  {
    "id": "1",
    "name": "Laptop",
    "description": "High-performance laptop with 16GB RAM",
    "price": 1200,
    "category": "electronics",
    "inStock": true
  }
]

2. Get Product by ID
Request:
GET /api/products/1

Response (200 OK):
{
  "id": "1",
  "name": "Laptop",
  "description": "High-performance laptop with 16GB RAM",
  "price": 1200,
  "category": "electronics",
  "inStock": true
}

Response (404 Not Found):
{
  "error": "Product not found"
}

3. Create a New Product
Request:
POST /api/products
Content-Type: application/json

{
  "name": "Gaming Mouse",
  "description": "RGB ergonomic gaming mouse",
  "price": 59.99,
  "category": "electronics",
  "inStock": true
}

Response (201 Created):
{
  "id": "generated-uuid",
  "name": "Gaming Mouse",
  "description": "RGB ergonomic gaming mouse",
  "price": 59.99,
  "category": "electronics",
  "inStock": true
}

4. Update a Product
Request:
PUT /api/products/1
Content-Type: application/json

{
  "name": "Updated Laptop",
  "description": "Updated description",
  "price": 1100,
  "category": "electronics",
  "inStock": false
}

Response (200 OK):
{
  "id": "1",
  "name": "Updated Laptop",
  "description": "Updated description",
  "price": 1100,
  "category": "electronics",
  "inStock": false
}

Response (404 Not Found):
{
  "error": "Product not found"
}

5. Delete a Product
Request:
DELETE /api/products/1

Response (200 OK):
{
  "message": "Product deleted successfully",
  "product": {
    "id": "1",
    "name": "Laptop",
    "description": "High-performance laptop with 16GB RAM",
    "price": 1200,
    "category": "electronics",
    "inStock": true
  }
}

Response (404 Not Found):
{
  "error": "Product not found"
}




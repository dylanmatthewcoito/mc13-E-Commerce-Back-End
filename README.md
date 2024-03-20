# Module 13 Challenge: Object-Relational Mapping (ORM) E-commerce Back End

## Description

This is a backend application for an e-commerce platform built with Express.js and Sequelize. It provides a RESTful API for managing categories, products, and tags.

## Video Walkthrough Link 

https://drive.google.com/file/d/1eBmKps-ii0Y7Z7BllY5ewemzDmFtkvsr/view

## Features

- CRUD operations for categories, products, and tags
- Sequelize ORM for database management
- Express.js for building the API endpoints
- MySQL database for data persistence

## Prerequisites

- Node.js (v12 or higher)
- MySQL database

## Installation

1. Clone the repository:

```bash
git clone git@github.com:dylanmatthewcoito/mc13-E-Commerce-Back-End.git
```

2. Install the dependencies:

```bash
cd ecommerce-backend
npm install
```

3. Set up the database:

- Create a new MySQL database for the application.
- Update the database connection details in `config/connection.js`.

4. Sync the database:

```bash
node sync.js
```

5. Start the application:

```bash
npm start
```

The server will start running at `http://localhost:3001`.

## API Endpoints
![Insomnia](https://github.com/dylanmatthewcoito/mc13-E-Commerce-Back-End/assets/71201051/a48b273e-34a8-43b8-80a9-2579d99443f7)

### Categories

- GET `/api/categories`: Get all categories
- GET `/api/categories/:id`: Get a single category by ID
- POST `/api/categories`: Create a new category
- PUT `/api/categories/:id`: Update a category by ID
- DELETE `/api/categories/:id`: Delete a category by ID

### Products

- GET `/api/products`: Get all products
- GET `/api/products/:id`: Get a single product by ID
- POST `/api/products`: Create a new product
- PUT `/api/products/:id`: Update a product by ID
- DELETE `/api/products/:id`: Delete a product by ID

### Tags

- GET `/api/tags`: Get all tags
- GET `/api/tags/:id`: Get a single tag by ID
- POST `/api/tags`: Create a new tag
- PUT `/api/tags/:id`: Update a tag by ID
- DELETE `/api/tags/:id`: Delete a tag by ID

## Database Models

### Category

- `id` (Integer, Primary Key)
- `category_name` (String)

### Product

- `id` (Integer, Primary Key)
- `product_name` (String)
- `price` (Decimal)
- `stock` (Integer)
- `category_id` (Integer, Foreign Key referencing Category)

### Tag

- `id` (Integer, Primary Key)
- `tag_name` (String)

### ProductTag

- `id` (Integer, Primary Key)
- `product_id` (Integer, Foreign Key referencing Product)
- `tag_id` (Integer, Foreign Key referencing Tag)

## Contributing

Contributions are welcome! If you find any issues or have suggestions for improvements, please open an issue or submit a pull request.

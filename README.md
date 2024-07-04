# E-commerce-Back-

This project is a backend for an e-commerce website built with Express.js, Sequelize, and MySQL. It provides API routes for managing categories, products, and tags, and includes functionality for creating, updating, and deleting data.

Table of Contents
Installation
Usage
Models
Category
Product
Tag
ProductTag
API Routes
License
Installation
Clone the repository:

bash
Copy code
git clone https://github.com/your-username/ecommerce-backend.git
cd ecommerce-backend
Install dependencies:

bash
Copy code
npm install
Create a .env file in the root of your project and add your database configuration:

makefile
Copy code
DB_NAME=your_database_name
DB_USER=your_mysql_username
DB_PASSWORD=your_mysql_password
Usage
Seed the database:

bash
Copy code
npm run seed
Start the server:

bash
Copy code
npm run dev
The server will be running on http://localhost:3000. You can test the API routes using Insomnia Core or any other API testing tool.

Models
Category
Field	Type	Constraints
id	Integer	Primary key, auto-increment, not null
category_name	String	Not null
Product
Field	Type	Constraints
id	Integer	Primary key, auto-increment, not null
product_name	String	Not null
price	Decimal	Not null, validates isDecimal
stock	Integer	Not null, default 10, validates isNumeric
category_id	Integer	References Category model's id
Tag
Field	Type	Constraints
id	Integer	Primary key, auto-increment, not null
tag_name	String	
ProductTag
Field	Type	Constraints
id	Integer	Primary key, auto-increment, not null
product_id	Integer	References Product model's id
tag_id	Integer	References Tag model's id
API Routes
Categories

GET /api/categories: Get all categories
POST /api/categories: Create a new category
PUT /api/categories/:id: Update a category by ID
DELETE /api/categories/:id: Delete a category by ID
Products

GET /api/products: Get all products
POST /api/products: Create a new product
PUT /api/products/:id: Update a product by ID
DELETE /api/products/:id: Delete a product by ID
Tags

GET /api/tags: Get all tags
POST /api/tags: Create a new tag
PUT /api/tags/:id: Update a tag by ID
DELETE /api/tags/:id: Delete a tag by ID
License
This project is licensed under the MIT License. See the LICENSE file for details.
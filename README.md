# E-commerce-Back-

This project is a backend for an e-commerce website built with Express.js, Sequelize, and MySQL. It provides API routes for managing categories, products, and tags, and includes functionality for creating, updating, and deleting data.

## Table of Contents
- Installation(#installation)
- Usage(#usage)
- License(#license)

## Installation

Clone the repository:

git clone https://github.com/your-username/ecommerce-backend.git
cd ecommerce-backend

Install dependancies:

npm install

Create a .env file in the root of your project and add your database configuration:

DB_NAME=your_database_name
DB_USER=your_mysql_username
DB_PASSWORD=your_mysql_password

## Usage
Seed the database:

npm run seed

Start the server:

npm run dev

The server will be running on http://localhost:3000. You can test the API routes using Insomnia Core or any other API testing tool.

## License
This project is licensed under the MIT License. See the LICENSE file for details.
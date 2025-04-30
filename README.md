## Product Inventory Management System
This project is a CRUD (Create, Read, Update, Delete) API for managing product inventory using Node.js, Express, and MongoDB.

## Features
Add a new product

Retrieve all product entries

Update product information

Delete a product record

## Prerequisites
Make sure the following are installed on your system:

Node.js (v14 or higher)

MongoDB (local instance or cloud-based like MongoDB Atlas)

## Installation
## 1. Clone the Repository
``
git clone https://github.com/YOUR-USERNAME/YOUR-REPO-NAME.git
cd product-inventory-api
``

2. Install Dependencies
``
npm install
``
## 2. Configure MongoDB
Set up your MongoDB (local or Atlas), then update your MongoDB connection URI in the .env file:
``

MONGODB_URI=mongodb+srv://<username>:<password>@cluster0.mongodb.net/inventoryDB
PORT=3000

``

## 4. Run the Server
``

npm start
The API will run at:
http://localhost:3000
``

## API Endpoints
## 1. Create a New Product
``
Endpoint: POST /products
``

## Request Body (JSON):

{
  "name": "Wireless Mouse",
  "category": "Electronics",
  "price": 25.99,
  "stock": 100
}
## Response:


{
  "message": "Product added successfully",
  "product": {
    "_id": "661234abcd456",
    "name": "Wireless Mouse",
    "category": "Electronics",
    "price": 25.99,
    "stock": 100
  }
}
## 2. Get All Products
Endpoint: GET /products

## Response:

[
  {
    "_id": "661234abcd456",
    "name": "Wireless Mouse",
    "category": "Electronics",
    "price": 25.99,
    "stock": 100
  }
]
## 3. Update a Product
Endpoint: PUT /products/:id

## Request Body (JSON):


{
  "price": 22.99,
  "stock": 120
}
Response:


{
  "message": "Product updated successfully",
  "updatedProduct": {
    "_id": "661234abcd456",
    "price": 22.99,
    "stock": 120
  }
}
## 4. Delete a Product
Endpoint: DELETE /products/:id

Response:

{
  "message": "Product deleted successfully"
}
## Project Structure
product-inventory-api/
│── models/
│   └── product.js         # Mongoose model
│── routes/
│   └── products.js        # Express routes
│── server.js              # Entry point
│── .env                   # Environment variables
│── package.json           # Scripts and dependencies
│── README.md              # Project documentation
## Dependencies
Express – Web framework for Node.js

Mongoose – ODM for MongoDB

dotenv – Manage environment variables

Nodemon – Auto-restart server during development

## Testing the API
Postman – Use for manual testing and sending requests

cURL – Command-line test example:
``

curl -X GET http://localhost:3000/products
`` 

## License
This project is open-source and available under the MIT License.

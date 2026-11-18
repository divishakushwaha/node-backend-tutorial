# Node Backend Tutorial

A simple REST API built with Node.js, Express and MongoDB (Mongoose). It supports CRUD (Create, Read, Update, Delete) for products.

## Setup

1. Install dependencies:
   ```
   npm install
   ```
2. Create a `.env` file in the project root (see `.env.example`):
   ```
   MONGO_URI=mongodb+srv://<db_username>:<db_password>@<your-cluster>.mongodb.net/Node-API?retryWrites=true&w=majority
   PORT=3000
   ```
3. Start the server:
   ```
   npm start
   ```
   You should see `Connected to MongoDB` and `Server running on port 3000`.

## API Endpoints

Base URL: `http://localhost:3000`

| Action   | Method | URL                  | Body (JSON)                                  |
|----------|--------|----------------------|----------------------------------------------|
| Create   | POST   | `/api/products`      | `{"name":"Laptop","quantity":5,"price":50000}` |
| Read all | GET    | `/api/products`      | none                                         |
| Read one | GET    | `/api/products/:id`  | none                                         |
| Update   | PUT    | `/api/products/:id`  | fields to change                             |
| Delete   | DELETE | `/api/products/:id`  | none                                         |

## Project Structure

```
index.js                          server + MongoDB connection
models/product.model.js           Product schema
controllers/product.controller.js CRUD logic
routes/product.route.js           URL to controller mapping
```

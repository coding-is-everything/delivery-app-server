# Grocery Delivery App - Server

This is the backend server for a Grocery Delivery Application built with Node.js, Fastify, and MongoDB.

## Project Overview

This server provides the API endpoints and database connectivity for a grocery delivery application. It manages users (customers, delivery partners, and admins), products, categories, orders, and branch locations.

## Tech Stack

- **Runtime Environment**: Node.js
- **Framework**: Fastify
- **Database**: MongoDB with Mongoose ODM
- **Authentication**: JSON Web Tokens (JWT)
- **Real-time Communication**: Socket.io
- **Development**: Nodemon for hot-reloading

## Project Structure

```
├── app.js                 # Main application entry point
├── package.json           # Project dependencies and scripts
└── src/                   # Source code directory
    ├── config/            # Configuration files
    │   ├── config.js      # Application configuration
    │   └── connect.js     # Database connection
    ├── controllers/       # Request handlers
    ├── middleware/        # Custom middleware
    ├── models/            # Database models
    │   ├── branch.js      # Branch location model
    │   ├── category.js    # Product category model
    │   ├── counter.js     # Counter model for IDs
    │   ├── orders.js      # Order management model
    │   ├── products.js    # Product model
    │   └── user.js        # User models (Customer, Admin, Delivery Partner)
    └── routes/            # API routes
```

## Models

### User Model

The application has three types of users:

1. **Customer**: End users who place orders
2. **Delivery Partner**: Users who deliver orders to customers
3. **Admin**: Users who manage the application

### Product Model

Stores information about products including:
- Name
- Image
- Price
- Discount Price
- Quantity
- Category

### Order Model

Manages order information including:
- Order ID
- Customer
- Delivery Partner
- Branch
- Items
- Delivery Location
- Pickup Location
- Delivery Person Location

## Setup and Installation

### Prerequisites

- Node.js (v14 or higher)
- MongoDB

### Installation

1. Clone the repository
2. Install dependencies:
   ```
   npm install
   ```
3. Create a `.env` file in the root directory with the following variables:
   ```
   PORT=3000
   MONGO_URI=your_mongodb_connection_string
   COOKIE_PASSWORD=your_secret_cookie_password
   ```

### Running the Application

```
npm start
```

The server will start on http://localhost:3000 (or the port specified in your .env file).

## API Endpoints

The API endpoints will be implemented in the routes directory. The current structure suggests the following potential endpoints:

- User authentication and management
- Product listing and management
- Order creation and tracking
- Category management
- Branch location management

## Development

The application uses nodemon for hot-reloading during development. Any changes to the files will automatically restart the server.

## License

ISC
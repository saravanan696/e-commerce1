# Internship Project: Basic Online Store with Product Management and Order Tracking

## 1. Project Title

**Online Store Management System**

---

# 2. Project Overview

The Online Store Management System is a full-stack web application that allows customers to browse products, add items to a cart, place orders, and track their order status. Administrators can manage products, monitor orders, and update order statuses through an admin dashboard.

This project demonstrates key full-stack development concepts including frontend development, backend APIs, authentication, database management, and role-based access control.

---

# 3. Project Objectives

### Customer Features

* View product catalog
* Search and filter products
* Add products to cart
* Checkout and place orders
* Track order status
* Manage user profile

### Admin Features

* Add new products
* Update product details
* Delete products
* Manage inventory
* View customer orders
* Update order status

---

# 4. Technology Stack

| Layer           | Technology                      |
| --------------- | ------------------------------- |
| Frontend        | HTML, CSS, JavaScript, React.js |
| Backend         | Node.js, Express.js             |
| Database        | MySQL / PostgreSQL / MongoDB    |
| Authentication  | JWT (JSON Web Token)            |
| Version Control | Git & GitHub                    |
| API Testing     | Postman                         |

---

# 5. System Architecture

```text
User
 │
 ▼
Frontend (React)
 │
 ▼
Backend API (Node.js + Express)
 │
 ▼
Database
(MySQL/PostgreSQL/MongoDB)
```

---

# 6. Modules of the Project

## Module 1: User Authentication

### Features

* User Registration
* User Login
* Logout
* Password Encryption
* JWT Authentication

### Database Table

Users

| Field    | Type       |
| -------- | ---------- |
| id       | Integer    |
| name     | String     |
| email    | String     |
| password | String     |
| role     | User/Admin |

---

## Module 2: Product Management

### Features

* Add Product
* Edit Product
* Delete Product
* View Product
* Search Product

### Database Table

Products

| Field        | Type    |
| ------------ | ------- |
| id           | Integer |
| product_name | String  |
| description  | Text    |
| price        | Decimal |
| stock        | Integer |
| image_url    | String  |

---

## Module 3: Shopping Cart

### Features

* Add Item to Cart
* Remove Item
* Update Quantity
* View Total Price

### Cart Workflow

```text
Product
 ↓
Add to Cart
 ↓
Update Quantity
 ↓
Calculate Total
 ↓
Checkout
```

---

## Module 4: Order Management

### Features

* Place Order
* View Orders
* Cancel Order
* Track Order Status

### Order Status

```text
Pending
 ↓
Confirmed
 ↓
Packed
 ↓
Shipped
 ↓
Delivered
```

### Database Table

Orders

| Field        | Type    |
| ------------ | ------- |
| order_id     | Integer |
| user_id      | Integer |
| total_amount | Decimal |
| order_date   | Date    |
| status       | String  |

---

## Module 5: Admin Dashboard

### Features

* Product Management
* Order Management
* User Monitoring
* Sales Reports

### Dashboard Functions

```text
Admin Dashboard
│
├── Manage Products
├── Manage Orders
├── Manage Users
└── Generate Reports
```

---

# 7. Database Design

## Users Table

```sql
CREATE TABLE users (
 id INT PRIMARY KEY AUTO_INCREMENT,
 name VARCHAR(100),
 email VARCHAR(100),
 password VARCHAR(255),
 role VARCHAR(20)
);
```

---

## Products Table

```sql
CREATE TABLE products (
 id INT PRIMARY KEY AUTO_INCREMENT,
 product_name VARCHAR(100),
 description TEXT,
 price DECIMAL(10,2),
 stock INT
);
```

---

## Orders Table

```sql
CREATE TABLE orders (
 order_id INT PRIMARY KEY AUTO_INCREMENT,
 user_id INT,
 total_amount DECIMAL(10,2),
 status VARCHAR(50)
);
```

---

# 8. REST API Endpoints

## Authentication APIs

| Method | Endpoint  |
| ------ | --------- |
| POST   | /register |
| POST   | /login    |

---

## Product APIs

| Method | Endpoint      |
| ------ | ------------- |
| GET    | /products     |
| GET    | /products/:id |
| POST   | /products     |
| PUT    | /products/:id |
| DELETE | /products/:id |

---

## Order APIs

| Method | Endpoint    |
| ------ | ----------- |
| GET    | /orders     |
| POST   | /orders     |
| PUT    | /orders/:id |
| DELETE | /orders/:id |

---

# 9. Step-by-Step Development Process

## Step 1: Create Project Structure

```text
online-store/
│
├── frontend/
├── backend/
├── database/
└── docs/
```

---

## Step 2: Setup Backend

Install Packages

```bash
npm init -y

npm install express mongoose cors dotenv bcryptjs jsonwebtoken
```

Create:

```text
server.js
routes/
controllers/
models/
middleware/
```

---

## Step 3: Setup Database

Choose one:

* MySQL
* PostgreSQL
* MongoDB

Create tables/collections.

---

## Step 4: Build Authentication System

Implement:

* Registration
* Login
* Password Hashing
* JWT Token Generation

---

## Step 5: Create Product APIs

Functions:

```text
Create Product
Read Product
Update Product
Delete Product
```

Test using Postman.

---

## Step 6: Build Frontend UI

Pages:

```text
Home
Products
Product Details
Cart
Checkout
Login
Register
Admin Dashboard
```

---

## Step 7: Implement Shopping Cart

Store cart items:

```javascript
Local Storage
or
Database
```

Features:

* Add Item
* Remove Item
* Update Quantity

---

## Step 8: Build Order System

Workflow:

```text
Cart
 ↓
Checkout
 ↓
Place Order
 ↓
Save in Database
 ↓
Track Status
```

---

## Step 9: Admin Dashboard

Admin can:

* Add Products
* Edit Products
* Delete Products
* Update Order Status

---

## Step 10: Testing

Test:

### Functional Testing

* Login
* Registration
* Product CRUD

### API Testing

* Postman

### Database Testing

* Verify Data Storage

---

# 10. Project Workflow

```text
User Registration
        ↓
User Login
        ↓
Browse Products
        ↓
Add to Cart
        ↓
Checkout
        ↓
Place Order
        ↓
Order Stored in Database
        ↓
Track Order Status
```

---

# 11. Future Enhancements

* Online Payment Integration
* Email Notifications
* Product Reviews & Ratings
* Wishlist
* Coupon System
* AI Product Recommendations
* Sales Analytics Dashboard

---

# 12. Learning Outcomes

After completing this internship project, you will learn:

* Full Stack Web Development
* REST API Development
* Database Integration
* Authentication & Authorization
* CRUD Operations
* Shopping Cart Logic
* Order Management System
* GitHub Version Control
* Deployment of Web Applications

---


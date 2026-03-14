# 🚀 CoreInventory – Smart Inventory Management System

CoreInventory is a modern **Inventory Management System** built using **Next.js and PostgreSQL**.
It helps businesses track products, manage stock movements, and monitor inventory operations efficiently.

This project was developed as part of a **hackathon challenge** to build a scalable, full-stack inventory management solution.

---

# 🧠 Problem Statement

Many small businesses and warehouses struggle with:

* Manual stock tracking
* Lack of real-time inventory visibility
* Difficulty tracking incoming and outgoing stock
* Errors in stock updates

CoreInventory solves these issues by providing a **centralized digital inventory management system** with automated stock updates and analytics.

---

# 💡 Solution

CoreInventory provides a **web-based inventory dashboard** that allows users to:

* Manage products
* Track incoming stock (receipts)
* Track outgoing stock (deliveries)
* Monitor inventory levels in real time
* Analyze stock status

The system automatically **updates product quantities** whenever stock is received or delivered.

---

# ✨ Key Features

## 📦 Product Management

* Add new products
* Edit product details
* Delete products
* View complete product catalog

## 📥 Stock Receipts

* Record incoming inventory
* Automatically increase product stock

## 📤 Deliveries

* Track outgoing shipments
* Automatically decrease stock

## 📊 Inventory Dashboard

* Total products overview
* Stock analytics
* Real-time inventory updates

## 🔍 Smart Search & Filters

* Search by product name or SKU
* Filter by category
* Filter by stock status

## 🔐 Authentication System

* Secure login system
* Email/password authentication
* Protected dashboard routes

---

# 🛠 Tech Stack

## Frontend

* Next.js
* React
* JavaScript
* Modern UI components

## Backend

* Next.js API Routes
* Node.js

## Database

* PostgreSQL

## Authentication

* Email + Password login

---

# 🏗 System Architecture

User Interface
↓
Next.js Frontend
↓
Next.js API Routes
↓
PostgreSQL Database

The system follows a **full-stack architecture with API-driven data flow**.

---

# 📂 Project Structure

```
inventory-management-system
│
├── app/
│   ├── api/
│   │   ├── products/
│   │   ├── receipts/
│   │   ├── deliveries/
│   │   ├── dashboard/
│   │   └── auth/
│   │
│   ├── products/
│   ├── receipts/
│   ├── deliveries/
│   ├── dashboard/
│   └── login/
│
├── components/
│   ├── Navbar.js
│   ├── ProductCard.js
│   └── DashboardStats.js
│
├── lib/
│   └── db.js
│
├── public/
└── README.md
```

---

# ⚙️ Installation

Clone the repository:

```
git clone https://github.com/SakshiHanwat/inventory-management-system.git
cd inventory-management-system
```

Install dependencies:

```
npm install
```

---

# 🔑 Environment Variables

Create a `.env` file in the root directory.

```
DATABASE_URL=postgresql://username:password@localhost:5432/inventory_db
```

---

# 🗄 Database Setup

Run the following SQL commands in PostgreSQL:

```
CREATE TABLE products (
  id SERIAL PRIMARY KEY,
  name TEXT,
  sku TEXT,
  category TEXT,
  unit TEXT,
  stock INT
);

CREATE TABLE receipts (
  id SERIAL PRIMARY KEY,
  product_id INT,
  quantity INT,
  received_at TIMESTAMP DEFAULT CURRENT_TIMESTAMP
);

CREATE TABLE deliveries (
  id SERIAL PRIMARY KEY,
  product_id INT,
  quantity INT,
  delivered_at TIMESTAMP DEFAULT CURRENT_TIMESTAMP
);

CREATE TABLE users (
  id SERIAL PRIMARY KEY,
  email TEXT UNIQUE,
  password TEXT
);
```

---

# ▶️ Run the Project

Start the development server:

```
npm run dev
```

Open the application:

```
http://localhost:3000
```

---

# 📷 Application Screens

### Dashboard

Overview of inventory analytics and stock insights.

### Products Page

Manage all products with filters and search.

### Receipts

Record incoming stock and automatically update inventory.

### Deliveries

Track outgoing stock and maintain accurate inventory levels.

---

# 🎯 Future Improvements

* Barcode scanning for product tracking
* Low-stock alerts
* Multi-warehouse inventory management
* Real-time notifications
* Advanced inventory analytics

---

# 🤝 Contributors

This project was developed during a Hackathon by the following team members:

- **Sakshi Hanwat** – Team Leader  
- **Palak Khare** – Developer  
- **Monalika Khanna** – Developer  

GitHub Repository:  
https://github.com/SakshiHanwat/inventory-management-system

---

# 📜 License

This project is open-source and available under the **MIT License**.

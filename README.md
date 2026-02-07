# 🛒 The Gadget Hub - Full Stack E-Commerce Store

**The Gadget Hub** is a robust, modern MERN stack e-commerce application designed for electronics enthusiasts. It features a complete shopping experience, secure user authentication, an interactive dashboard, 
and a dynamic light/dark theme system.

---

## 📑 Table of Contents

* [Tech Stack](https://www.google.com/search?q=%23-tech-stack)
* [Database Architecture (ADBMS)](https://www.google.com/search?q=%23-database-architecture-adbms)
* [Key Features](https://www.google.com/search?q=%23-key-features)
* [Project Structure](https://www.google.com/search?q=%23-project-structure)
* [Installation & Setup](https://www.google.com/search?q=%23-installation--setup)
* [Environment Variables](https://www.google.com/search?q=%23-environment-variables)

---

## 💻 Tech Stack

| Layer | Technology |
| --- | --- |
| **Frontend** | React.js, Context API, CSS Modules, React-Slick |
| **Backend** | Node.js, Express.js |
| **Database** | MongoDB (NoSQL) |
| **Authentication** | JSON Web Tokens (JWT), Bcrypt.js |
| **Notifications** | React Hot Toast |

---

## 🗄️ Database Architecture (ADBMS)

This project utilizes **MongoDB**, a document-oriented NoSQL database. The schema design focuses on high availability and flexible data structures.

### **Core Collections:**

1. **Users:** Stores authenticated users. Passwords are encrypted using **Bcrypt.js** (salting and hashing).
2. **Products:** Contains electronic inventory items. Includes fields for price, stock, and category.
3. **Orders:** Manages transactions. It demonstrates the power of NoSQL by **embedding** line items as an array of objects directly within the order document, reducing the need for complex joins.

---

## ✨ Key Features

### 👤 User Features

* **Authentication:** Secure Login/Register system using JWT.
* **Advanced Search:** Filter products by keywords or specific categories.
* **Shopping Cart:** Persistent cart with "bump" animation feedback.
* **Wishlist:** Save favorite products for later.
* **Responsive Theme:** Seamless transition between **Light** and **Dark** modes using React Context and CSS Variables.
* **Checkout Process:** 4-step secure checkout (Cart ➡️ Shipping ➡️ Payment ➡️ Review).

### 🛠️ Admin Features

* **Product Management:** Full **CRUD** (Create, Read, Update, Delete) capabilities.
* **Inventory Control:** Update stock levels and prices in real-time.
* **Order Tracking:** View all customer orders and their payment status.

---

## 📂 Project Structure

```text
Adbms/
├── client/                # React Frontend
│   ├── public/            # Static assets (logos, images)
│   └── src/
│       ├── components/    # Reusable UI components
│       ├── context/       # State management (Auth, Cart, Theme)
│       ├── pages/         # Page components
│       └── styles/        # CSS Modules
├── server/                # Node.js & Express Backend
│   ├── controllers/       # Business logic for routes
│   ├── middleware/        # Auth & Admin verification
│   ├── models/            # MongoDB Schemas
│   ├── routes/            # API Endpoints
│   └── utils/             # JWT helper functions
└── README.md

```

---

## 🚀 Installation & Setup

### **Prerequisites**

* Node.js installed
* MongoDB Atlas account or Local MongoDB Compass

### **1. Clone the Repository**

```bash
git clone https://github.com/Viru45/Adbms.git
cd Adbms

```

### **2. Backend Setup**

```bash
cd server
npm install
# Create a .env file (see Environment Variables section)
npm start

```

### **3. Frontend Setup**

```bash
cd client
npm install
npm start

```

---

## 🔑 Environment Variables

Create a `.env` file in the **server** directory and add the following:

```env
NODE_ENV = development
PORT = 5000
MONGO_URI = your_mongodb_connection_string
JWT_SECRET = your_secret_key_here

```

---

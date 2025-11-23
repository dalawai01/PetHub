


# 🐾 **PetHub – Pet Food & Grooming Hub**

---

## ⭐ **Overview**

**PetHub** is a Java-based online shopping platform where pet owners can browse and purchase:

* 🐶 Pet food
* 🐱 Grooming products
* 🧴 Hygiene essentials
* 🧸 Pet toys
* And other pet-care items

The platform is built using **Java + JSP + Servlets + JDBC** following the **MVC architecture** and runs on **Apache Tomcat**.

---

## 🚀 **Features**

### 🛒 User Features

* Browse products by category (Food, Grooming, Toys, etc.)
* View product details
* Add items to cart
* Place an order
* Simple and clean JSP-driven UI

### 🛠️ Admin Features

* Add new products
* Edit product information
* Delete products
* Manage inventory
* View customer orders

### ⚙️ Technical Features

* Java Servlets backend
* JSP/HTML-based views
* MySQL relational database
* Structured MVC architecture

---

## 🧰 **Tech Stack**

| Layer            | Technology     |
| ---------------- | -------------- |
| **Frontend**     | HTML, CSS, JSP |
| **Backend**      | Java, Servlets |
| **Database**     | MySQL, JDBC    |
| **Architecture** | MVC            |
| **Server**       | Apache Tomcat  |

---

## 📁 **Project Structure**

```
PetHub/
├── src/main/
│   ├── java/                 # Servlets, Models, DAO
│   ├── webapp/               # JSP pages, CSS, images
├── build/classes/            # Compiled .class files
├── .classpath
├── .project
└── README.md
```

---

## 🗄️ **Database Schema (Suggested)**

### **Products Table**

```sql
CREATE TABLE products (
  id INT AUTO_INCREMENT PRIMARY KEY,
  name VARCHAR(255),
  category VARCHAR(100),
  price DECIMAL(10,2),
  description TEXT,
  image_url VARCHAR(500)
);
```

### **Cart Table**

```sql
CREATE TABLE cart (
  id INT AUTO_INCREMENT PRIMARY KEY,
  user_id INT,
  product_id INT,
  quantity INT,
  FOREIGN KEY (product_id) REFERENCES products(id)
);
```

### **Orders Table**

```sql
CREATE TABLE orders (
  id INT AUTO_INCREMENT PRIMARY KEY,
  user_id INT,
  total_price DECIMAL(10,2),
  created_at TIMESTAMP DEFAULT CURRENT_TIMESTAMP
);
```

---

## 🛠️ **Setup Instructions**

### 1️⃣ Clone the Repository

```bash
git clone https://github.com/dalawai01/PetHub.git
```

### 2️⃣ Import into IDE

* Eclipse → *Import Existing Project*
* IntelliJ → *Open Project*

### 3️⃣ Configure MySQL

Create database:

```sql
CREATE DATABASE pethub;
```

Update JDBC configuration inside DAO classes.

### 4️⃣ Run on Tomcat

Add project → Start Tomcat → Visit:

```
http://localhost:8080/PetHub/
```

---

## 🎯 **Future Enhancements**

* Add **Spring Boot** version
* Add **online payment integration**
* Add **user login/registration**
* Add **order history tracking**
* Add **search & filtering**
* Enhance **UI with modern styling**

---

## 🙌 **Contributing**

1. Fork this repo
2. Create a branch
3. Commit your changes
4. Submit a PR

---

## 📮 **Contact**

**Developer:** Basu Dalawai
GitHub: [@dalawai01](https://github.com/dalawai01)

---




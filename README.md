
# 🐾 **PetHub – Pet Adoption Platform**


## ⭐ **Overview**

**PetHub** is a full-stack **Java Web Application** built using **JSP, Servlets, JDBC, and MVC architecture**.
It provides a centralized platform where users can **browse pets**, view details, and submit **adoption requests**.
Admins can manage listings, while the system maintains smooth backend operations through a clean MVC structure.

---

## 🚀 **Features**

### 👤 User Features

* Browse available pets
* View detailed information
* Apply for pet adoption
* User-friendly UI powered by JSP

### 🛠️ Admin Features

* Add new pets
* Update existing pet details
* Delete unwanted pet entries
* Track adoption requests

### ⚙️ Technical Features

* MVC architecture (Servlets + JSP)
* JDBC-based database connectivity
* MySQL relational schema
* Works on Apache Tomcat

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
│   ├── java/                # Java source code (Servlets, Models, DAO)
│   ├── webapp/              # JSP pages, static assets
├── build/classes/           # Compiled .class files (should be gitignored)
├── .classpath
├── .project
└── README.md
```

---

## 🗄️ **Database Schema (Suggested)**

```sql
CREATE TABLE pets (
  id INT AUTO_INCREMENT PRIMARY KEY,
  name VARCHAR(255),
  type VARCHAR(100),
  age INT,
  description TEXT,
  image_url VARCHAR(512),
  status VARCHAR(50)
);

CREATE TABLE adoption_requests (
  id INT AUTO_INCREMENT PRIMARY KEY,
  pet_id INT,
  name VARCHAR(255),
  email VARCHAR(255),
  phone VARCHAR(50),
  message TEXT,
  status VARCHAR(50),
  created_at TIMESTAMP DEFAULT CURRENT_TIMESTAMP,
  FOREIGN KEY (pet_id) REFERENCES pets(id)
);
```

---

## 🛠️ **Setup & Run Locally**

### 1️⃣ Clone the repository

```bash
git clone https://github.com/dalawai01/PetHub.git
```

### 2️⃣ Import into IDE

* Open Eclipse → *Import Existing Project*
* Or open in IntelliJ as a simple Java web project

### 3️⃣ Configure MySQL

* Create DB:

```sql
CREATE DATABASE pethub;
```

* Update JDBC URL, username, and password inside DAO classes.

### 4️⃣ Deploy to Tomcat

* Add project to Tomcat Server in IDE
* Start server
* Visit:

```
http://localhost:8080/PetHub/
```

---

## 🎯 **Roadmap / Future Enhancements**

* Add Spring Boot version
* User authentication (JWT or sessions)
* Image upload feature
* Advanced search filters
* Admin dashboard UI redesign

---

## 🙌 **Contributing**

1. Fork this repository
2. Create a feature branch (`feature/new-update`)
3. Commit changes
4. Push branch
5. Open PR 🚀

---

## 📮 **Contact**

Developed & Maintained by **Basu Dalawai**
GitHub: [@dalawai01](https://github.com/dalawai01)

---


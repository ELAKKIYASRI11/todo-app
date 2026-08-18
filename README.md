# Todo List App (Spring Boot + MySQL + HTML/CSS/JS)

## 🚀 Live Demo

👉 [Open Todo List App](https://todo-app-production-cc3e.up.railway.app/)

## 📌 About the Project

A simple Todo List web application built using **Spring Boot, MySQL, HTML, CSS, and JavaScript**.

The application allows users to create, view, update, and delete todo items through a web interface and REST APIs.

## 🛠️ Technologies Used

* Java
* Spring Boot
* Spring Data JPA
* MySQL
* HTML
* CSS
* JavaScript
* Maven
* Railway

## 🚀 Features

* Add new todos
* View all todos
* Update todo status
* Delete todos
* REST API support
* MySQL database integration
* Simple and responsive frontend
* Deployed using Railway

## 🌐 Live Application

You can access the deployed application here:

👉 https://todo-app-production-cc3e.up.railway.app/

## 💻 Before Running Locally

### 1. Create the Database

Create a database in **MySQL Workbench** or using the MySQL CLI:

```sql
CREATE DATABASE tododb;
```

### 2. Configure MySQL

Open:

```text
src/main/resources/application.properties
```

Set your MySQL username and password.

Example:

```properties
spring.datasource.url=jdbc:mysql://localhost:3306/tododb
spring.datasource.username=root
spring.datasource.password=your_mysql_password
```

**Do not upload your real MySQL password to GitHub.**

For deployment, use environment variables in Railway instead of storing your database password directly in the source code.

## ▶️ Run the Project Locally

1. Clone the repository.

2. Open the project in **IntelliJ IDEA**.

3. Import it as a **Maven project**.

4. Make sure MySQL is running.

5. Create the `tododb` database.

6. Configure your MySQL username and password in `application.properties`.

7. Run:

```text
TodoAppApplication.java
```

8. Open the application in your browser:

```text
http://localhost:8080
```

The Todo List UI will be displayed.

The `todos` table will be created automatically because of:

```properties
spring.jpa.hibernate.ddl-auto=update
```

## 🔗 REST API Endpoints

### Get All Todos

```http
GET http://localhost:8080/api/todos
```

### Create a Todo

```http
POST http://localhost:8080/api/todos
```

Request body:

```json
{
  "title": "Buy milk",
  "completed": false
}
```

### Update a Todo

```http
PUT http://localhost:8080/api/todos/1
```

Request body:

```json
{
  "title": "Buy milk",
  "completed": true
}
```

### Delete a Todo

```http
DELETE http://localhost:8080/api/todos/1
```

## 🧪 Testing the API

The REST APIs can be tested using **Postman**.

You can test:

* `GET` — Retrieve todos
* `POST` — Create a todo
* `PUT` — Update a todo
* `DELETE` — Delete a todo

## ☁️ Deployment

The application is deployed using **Railway**.

### Production URL

👉 [Open Deployed Application](https://todo-app-production-cc3e.up.railway.app/)

The deployed application uses a Railway MySQL database for data persistence.

## 🔐 Security

Security authentication is not implemented yet.

The security starter is intentionally left out while developing the core Todo List functionality.

Authentication and authorization can be added later using:

* Spring Security
* Login/Signup
* Password encryption
* Role-based access control

## 📁 Project Structure

```text
Todo-App/
│
├── src/
│   ├── main/
│   │   ├── java/
│   │   │   └── ...
│   │   │
│   │   └── resources/
│   │       ├── static/
│   │       │   ├── index.html
│   │       │   ├── style.css
│   │       │   └── script.js
│   │       │
│   │       └── application.properties
│   │
├── pom.xml
└── README.md
```

## 📝 Notes

* Make sure MySQL is running when running the application locally.
* Do not commit passwords or other sensitive credentials to GitHub.
* For Railway deployment, configure database credentials using Railway environment variables.
* The database table is automatically created/updated using JPA and Hibernate.

## 👩‍💻 Author

**Elakkiyasri S**

GitHub: [View My GitHub Profile](https://github.com/)

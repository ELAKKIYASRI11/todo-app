# Todo List App (Spring Boot + MySQL + HTML/CSS/JS)

## 🚀 Live Demo

https://todo-app-production-cc3e.up.railway.app/

## Before running

1. Create the database in MySQL Workbench (or CLI):

   ```sql
   CREATE DATABASE tododb;
   ```

2. Open `src/main/resources/application.properties` and set your real MySQL
   username and password (replace `your_mysql_password`).

## Run it

* Import the project into IntelliJ as a Maven project.
* Run `TodoAppApplication.java`.
* Open `http://localhost:8080` in your browser — you'll see the todo list UI.
* The table `todos` is created automatically (thanks to `ddl-auto=update`).

## Test the API directly (Postman)

* `GET    http://localhost:8080/api/todos`
* `POST   http://localhost:8080/api/todos`      body: `{"title": "Buy milk", "completed": false}`
* `PUT    http://localhost:8080/api/todos/1`     body: `{"title": "Buy milk", "completed": true}`
* `DELETE http://localhost:8080/api/todos/1`

## Notes

* Security starter is intentionally left out for now, so there's no login
  wall while you're testing. Add `spring-boot-starter-security` back in
  once the core todo list works and you're ready to build login/signup.
* To deploy, swap the three `spring.datasource.*` lines in
  `application.properties` for your Railway MySQL connection details.

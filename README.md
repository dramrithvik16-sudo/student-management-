# Student Management System — Full-Stack Internship Project

Full-stack Student Management System built with React + Vite, Java 17, Spring Boot, Spring Data JPA, and MySQL.

## Features
- Create, view, edit, delete and search student records
- Form validation and duplicate-email protection
- REST API backed by MySQL

## Run locally in VS Code
Requirements: JDK 17+, Maven 3.9+, Node.js 20+ and MySQL 8+.

1. Create the database: `CREATE DATABASE student_management;`
2. Configure database credentials using `SPRING_DATASOURCE_URL`, `SPRING_DATASOURCE_USERNAME`, and `SPRING_DATASOURCE_PASSWORD` or edit `backend/src/main/resources/application.properties`.
3. Backend: `cd backend && mvn spring-boot:run` (API: http://localhost:8080/api/students).
4. Frontend in another terminal: `cd frontend && npm install && npm run dev` (normally http://localhost:5173).

## Deployment
The project is configured with environment-variable support. See `render.yaml` for an initial Render Blueprint definition. The backend requires a reachable MySQL database. Set `VITE_API_BASE_URL` to the deployed backend URL ending in `/api`; set backend datasource variables in the hosting provider. Add the deployed frontend domain to `@CrossOrigin` in `StudentController.java` before production use.

A live service URL is not created merely by uploading source code; it becomes available after hosting and database setup succeed. Do not commit real database passwords.

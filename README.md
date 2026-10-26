# 🏢 Employee Management System

> A modern, full-stack CRUD application for managing employee records — built with **Spring Boot**, **React**, and **MySQL**.

![Java](https://img.shields.io/badge/Java-17-orange?style=flat-square&logo=openjdk)
![Spring Boot](https://img.shields.io/badge/Spring%20Boot-3-6DB33F?style=flat-square&logo=springboot)
![React](https://img.shields.io/badge/React-18-61DAFB?style=flat-square&logo=react)
![MySQL](https://img.shields.io/badge/MySQL-8-4479A1?style=flat-square&logo=mysql&logoColor=white)

---

## ✨ Features

- **Full CRUD Operations** — Create, read, update, and delete employee records
- **Real-time Search** — Search employees by name instantly
- **Department Filtering** — Filter employees by department
- **Server-side Validation** — Required fields, email format, positive salary with clean error messages
- **Global Exception Handling** — Custom 404s instead of raw stack traces
- **RESTful API** — Standard HTTP verb conventions
- **Clean & Minimal UI** — Modern design with smooth animations and premium feel

## 🛠️ Tech Stack

| Layer | Technologies |
|-------|-------------|
| **Backend** | Java 17, Spring Boot 3, Spring Data JPA, Hibernate, MySQL, Maven, Lombok, Bean Validation |
| **Frontend** | React 18, Axios, CSS3 (Custom Properties, Animations) |
| **Database** | MySQL 8 |
| **Deployment** | Render (Backend), Vercel (Frontend) |

## 📁 Project Structure

```
employee-management-system/
├── backend/                          # Spring Boot REST API
│   ├── src/main/java/com/ems/employeemanagement/
│   │   ├── controller/               # REST endpoints
│   │   ├── service/                  # Business logic
│   │   ├── repository/               # Data access (Spring Data JPA)
│   │   ├── entity/                   # JPA entities
│   │   └── exception/               # Custom exceptions + global handler
│   ├── src/main/resources/
│   │   └── application.properties
│   └── pom.xml
├── frontend/                         # React app
│   ├── src/
│   │   ├── components/               # EmployeeForm, EmployeeList
│   │   ├── services/                 # Axios API calls
│   │   ├── App.js                    # Main application component
│   │   └── App.css                   # Complete design system
│   └── package.json
└── README.md
```

## 🚀 Getting Started

### Prerequisites

- Java 17+
- Maven
- Node.js 18+
- MySQL (or use H2 in-memory for quick testing)

### 1. Backend (Spring Boot)

```bash
cd backend

# Update src/main/resources/application.properties with your MySQL credentials
# Then run:
mvn spring-boot:run
```

The API will start at `http://localhost:8080`

> 💡 **No MySQL?** Run with H2 in-memory database:
> ```bash
> mvn spring-boot:run -Dspring-boot.run.profiles=h2
> ```

### 2. Frontend (React)

```bash
cd frontend
npm install
npm start
```

The app will open at `http://localhost:3000` and connect to the backend at `http://localhost:8080`.

## 📡 API Endpoints

| Method | Endpoint | Description |
|--------|----------|-------------|
| `GET` | `/api/employees` | Get all employees |
| `GET` | `/api/employees/{id}` | Get employee by ID |
| `POST` | `/api/employees` | Create a new employee |
| `PUT` | `/api/employees/{id}` | Update an employee |
| `DELETE` | `/api/employees/{id}` | Delete an employee |
| `GET` | `/api/employees/department/{dept}` | Filter by department |
| `GET` | `/api/employees/search?name=xyz` | Search by name |

## 🧪 Running Tests

```bash
cd backend
mvn test
```

## 🔮 Future Improvements

- [ ] Authentication & Authorization (Spring Security + JWT)
- [ ] Pagination and sorting on the employee list
- [ ] Department management module
- [ ] Docker containerization
- [ ] Employee profile picture uploads
- [ ] Dark mode toggle

## 🤝 Contributing

Contributions, issues, and feature requests are welcome! Feel free to open an issue or submit a pull request.

## 📝 License

This project is open source and available under the [MIT License](LICENSE).

---

**Built with ❤️ by [mohan-sai143](https://github.com/mohan-sai143)**
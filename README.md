# Student Management System

A full-stack web application for managing student records, built with **Spring Boot** and **Thymeleaf**. This project provides a complete CRUD (Create, Read, Update, Delete) interface for student data management with a modern, responsive user interface.

## 🚀 Features

- **View All Students**: Display a list of all registered students in a clean, organized table
- **Add New Students**: Create new student records with first name, last name, and email
- **Edit Student Information**: Update existing student details
- **Delete Students**: Remove student records from the database
- **Responsive Design**: Custom CSS styling for an enhanced user experience
- **Data Persistence**: MySQL database integration for reliable data storage

## 🛠️ Technologies Used

### Backend
- **Java 17**
- **Spring Boot 4.0.1**
  - Spring Boot Web MVC
  - Spring Data JPA
  - Spring Boot Actuator
  - Spring Boot DevTools
- **Maven** - Dependency management and build tool

### Frontend
- **Thymeleaf** - Server-side templating engine
- **HTML5**
- **CSS3** - Custom styling for each page

### Database
- **MySQL** - Relational database
- **Hibernate/JPA** - Object-relational mapping

### Server
- **Apache Tomcat** - Embedded servlet container

## 📋 Prerequisites

Before running this application, ensure you have the following installed:

- **Java Development Kit (JDK) 17** or higher
- **Maven 3.6+**
- **MySQL Server 8.0+**
- **Git** (optional, for cloning the repository)

## ⚙️ Configuration

### Database Setup

1. Create a MySQL database:
```sql
CREATE DATABASE students_db;
```

2. Update the `src/main/resources/application.properties` file with your MySQL credentials:
```properties
spring.datasource.url=jdbc:mysql://localhost:3306/students_db
spring.datasource.username=your_username
spring.datasource.password=your_password
spring.jpa.hibernate.ddl-auto=update
spring.jpa.show-sql=true
```

## 🚦 Getting Started

### Installation

1. **Clone the repository**
```bash
git clone https://github.com/yourusername/student-management-system.git
cd student-management-system
```

2. **Build the project**
```bash
./mvnw clean install
```
*On Windows, use `mvnw.cmd` instead*

3. **Run the application**
```bash
./mvnw spring-boot:run
```

4. **Access the application**

Open your web browser and navigate to:
```
http://localhost:8080/students
```

## 📁 Project Structure

```
demo/
├── src/
│   ├── main/
│   │   ├── java/com/example/demo/
│   │   │   ├── controller/
│   │   │   │   └── StudentController.java      # Handles HTTP requests
│   │   │   ├── entity/
│   │   │   │   └── Student.java                # JPA entity model
│   │   │   ├── repository/
│   │   │   │   └── StudentRepository.java      # Data access layer
│   │   │   ├── service/
│   │   │   │   ├── StudentService.java         # Service interface
│   │   │   │   └── impl/
│   │   │   │       └── StudentServiceImpl.java # Service implementation
│   │   │   ├── DemoApplication.java            # Main application entry point
│   │   │   └── ServletInitializer.java         # WAR deployment configuration
│   │   └── resources/
│   │       ├── static/css/
│   │       │   ├── students.css                # Styles for student list
│   │       │   ├── create_student.css          # Styles for create form
│   │       │   └── update_student.css          # Styles for update form
│   │       ├── templates/
│   │       │   ├── students.html               # Student list view
│   │       │   ├── create_student.html         # Create student form
│   │       │   └── update_student.html         # Update student form
│   │       └── application.properties          # Application configuration
├── pom.xml                                      # Maven dependencies
└── README.md
```

## 🎯 API Endpoints

| Method | Endpoint | Description |
|--------|----------|-------------|
| GET | `/students` | Display all students |
| GET | `/students/new` | Show create student form |
| POST | `/students` | Save a new student |
| GET | `/students/edit/{id}` | Show edit student form |
| POST | `/students/{id}` | Update existing student |
| GET | `/students/{id}` | Delete a student |

## 💾 Database Schema

### Students Table
| Column | Type | Constraints |
|--------|------|-------------|
| id | BIGINT | PRIMARY KEY, AUTO_INCREMENT |
| first_name | VARCHAR | NOT NULL |
| last_name | VARCHAR | NOT NULL |
| email | VARCHAR | NOT NULL |

## 🎨 User Interface

The application features three main pages:

1. **Student List Page** (`students.html`) - Displays all students in a table with Edit and Delete options
2. **Create Student Page** (`create_student.html`) - Form to add new students
3. **Update Student Page** (`update_student.html`) - Form to edit existing student information

Each page has its own custom CSS file for a polished, professional appearance.

## 🔧 Development

### Running in Development Mode

The project includes **Spring Boot DevTools** for automatic restart and live reload during development:

```bash
./mvnw spring-boot:run
```

### Building for Production

To create a WAR file for deployment:

```bash
./mvnw clean package
```

The WAR file will be generated in the `target/` directory.

## 📝 License

This project is open source and available under the [MIT License](LICENSE).

## 👨‍💻 Author

**Younes**

## 🤝 Contributing

Contributions, issues, and feature requests are welcome! Feel free to check the [issues page](https://github.com/yourusername/student-management-system/issues).

## 📧 Contact

If you have any questions or suggestions, feel free to reach out!

---

⭐ **If you find this project useful, please consider giving it a star!** ⭐

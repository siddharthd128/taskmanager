1. # Task Management API

  A RESTful API for managing tasks with basic CRUD operations.

  ## Features
  - Create, retrieve, update, and delete tasks.
  - Manage task statuses: Pending, In Progress, and Completed.
  - Input validation to ensure proper data handling.
  - Comprehensive error handling for invalid requests.

  ## Prerequisites
  - Java Development Kit (JDK 17 or later)
  - Gradle or Maven
  - Spring Boot framework
  - Postman (optional, for testing)
  - H2 Database (default) or other relational database
  
  ## Setup Instructions
  1. Clone the repository:
     ```bash
     git clone https://github.com/siddharthd128/taskmanager.git
     cd taskmanager
2. Build and run the project:
   mvn spring-boot:run
3. Access the API:
  API Base URL: http://localhost:8080
4. H2 Database Console:

URL: http://localhost:8080/h2-console
    JDBC URL: jdbc:h2:mem:taskdb
    Username: siddharthd128
    Password: **********

5. API Endpoints
  Task Endpoints
    1. Create a Task
        POST /tasks
        Request Body:
          json
          {
              "title": "Task Title",
              "description": "Task Description",
              "status": "PENDING"
          }
        Response: Task details with ID.
    2. Retrieve All Tasks
        GET /tasks
        Response: List of all tasks.
    3. Retrieve a Task by ID
        GET /tasks/{id}
        Response: Task details.
    4. Update a Task
        PUT /tasks/{id}
        Request Body:
          json
          {
              "title": "Updated Title",
              "description": "Updated Description",
              "status": "IN_PROGRESS"
          }
        Response: Updated task details.
    5. Delete a Task
        DELETE /tasks/{id}
        Response: 204 No Content (on success).
6. Error Handling
    400 Bad Request: Invalid input data.
    404 Not Found: Resource not found.
    500 Internal Server Error: Generic server error.
7. Project Structure
    scss
    taskmanager/
    ├── src/main/java/com/example/taskmanager
    │   ├── controller/      // Controllers handling API endpoints
    │   ├── exception/       // Custom exceptions and global error handlers
    │   ├── model/           // Data models (e.g., Task, TaskStatus)
    │   ├── repository/      // JPA repositories
    │   ├── service/         // Business logic
    │   └── TaskManagerApplication.java  // Main class
    ├── src/main/resources
    │   ├── application.properties  // Configuration
    │   └── static/                 // Static resources (if any)
    ├── .gitignore
    ├── build.gradle or pom.xml     // Build file
    └── README.md
8. License
    This project is licensed under the MIT License - see the LICENSE file for details.
    yaml
      ### **Publish the Repository**
      Once you’ve added the `README.md` file:
      1. Commit the changes:
         ```bash
         git add README.md
         git commit -m "Added README with setup instructions and API details"
         git push origin main

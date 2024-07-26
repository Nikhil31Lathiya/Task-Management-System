# Task Management System 📋

Welcome to the Task Management System! This Java-based application allows you to efficiently manage tasks with a MySQL database backend. You can add, view, update, and delete tasks, making it a handy tool for organizing and tracking tasks.

## Features 🌟

- **Add Task** ➕: Add new tasks with details like name, description, priority, due date, assigned person, and status.
- **View All Tasks** 👁️: Display all tasks stored in the system.
- **View Task by ID** 🔍: Retrieve and view task details by providing the task ID.
- **Update Task** ✏️: Modify existing task details.
- **Update Task Progress** 📈: Update the progress percentage of a task.
- **Delete Task** 🗑️: Remove tasks from the system by ID.

## Prerequisites 🔧

1. **Java**: Make sure you have Java Development Kit (JDK) installed.
2. **MySQL**: You need a MySQL database set up with the appropriate schema.
3. **JDBC Driver**: Ensure you have the MySQL JDBC driver (`mysql-connector-java`) in your classpath.

## Setup ⚙️

1. **Clone the Repository**:
    ```bash
    git clone https://github.com/yourusername/task-management-system.git
    ```

2. **Configure Database**:
   - Create a MySQL database named `task_management_system`.
   - Create a table named `tasks` using the following schema:
     ```sql
     CREATE TABLE tasks (
         id INT AUTO_INCREMENT PRIMARY KEY,
         name VARCHAR(255) NOT NULL,
         description TEXT,
         priority INT,
         due_date DATE,
         assigned_to VARCHAR(255),
         status VARCHAR(50),
         progress INT DEFAULT 0
     );
     ```

3. **Update Database Connection**:
   - Open `Task_Management_System.java`.
   - Modify the `URL`, `USER`, and `PASSWORD` constants with your MySQL database credentials.

4. **Build the JAR File**:
   - Navigate to the project directory where `Task_Management_System.java` is located.
   - Compile the Java file:
     ```bash
     javac Task_Management_System.java
     ```
   - Package the compiled classes into a JAR file:
     ```bash
     jar cvf task_management_system.jar Task_Management_System.class
     ```

5. **Add MySQL JDBC Driver to Classpath**:
   - Download the MySQL JDBC driver (`mysql-connector-java.jar`) from the [official MySQL website](https://dev.mysql.com/downloads/connector/j/).
   - Ensure the JDBC driver JAR is in the same directory as your JAR file or provide the path to it.

## Running the Application ▶️

To run the application, use the following command, replacing `path/to/mysql-connector-java.jar` with the actual path to your MySQL JDBC driver JAR file:

```bash
java -cp "task_management_system.jar:path/to/mysql-connector-java.jar" Task_Management_System

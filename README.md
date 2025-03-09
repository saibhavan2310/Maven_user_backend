# User Backend Microservices

This repository contains three Maven-based microservices:
1. **Eureka Server** (Service Discovery)
2. **User Service** (Handles user data and operations)
3. **Notification Service** (Provides console and frontend notifications on user actions)

## Prerequisites
Before you begin, ensure you have the following installed:
- **Java JDK 11+**
- **Eclipse IDE** (or any IDE supporting Maven projects)
- **Maven** (Ensure Maven is installed and configured in your system PATH)
- **Spring Boot** (Comes with the project dependencies)

## Setup Instructions

### Step 1: Clone the Repository
```sh
 git clone <your-repo-link>
 cd <repo-folder>
```

### Step 2: Import Projects into Eclipse
1. Open **Eclipse IDE**
2. Go to **File** > **Import**
3. Select **Existing Maven Projects**
4. Browse to the cloned repository folder
5. Select all three projects (**Eureka Server**, **User Service**, **Notification Service**)
6. Click **Finish**

### Step 3: Start the Services in Order
#### 1. Start the Eureka Server
- Navigate to the **Eureka Server** project
- Run the application using:
  ```sh
  mvn spring-boot:run
  ```
- Eureka should start on `http://localhost:8761/`

#### 2. Start the User Service
- Navigate to the **User Service** project
- Run the application using:
  ```sh
  mvn spring-boot:run
  ```
- The User Service contains user-related tables and REST APIs

#### 3. Start the Notification Service
- Navigate to the **Notification Service** project
- Run the application using:
  ```sh
  mvn spring-boot:run
  ```
- This service logs messages to the console whenever a new user is added or deleted.
- It also provides real-time notifications on the frontend.

### Features Overview
- **User Service**:
  - Handles user table operations (CRUD)
  - Provides REST API endpoints for user management
  
- **Notification Service**:
  - Monitors user addition and deletion
  - Logs updates to the console
  - Sends notifications to the frontend


## Additional Notes
- Ensure all services are running correctly before testing the User and Notification services.
- Modify `application.properties` in each service to match your database configuration if needed.
- Eureka Server should always be started first to ensure service discovery.

---

### Need Help?
If you encounter any issues, feel free to raise an issue in the repository or contact the project maintainer.

Happy Coding! 🚀


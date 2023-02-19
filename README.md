# Monthly Expenses Repo
The Monthly Expenses Service is a Spring Boot application that provides a RESTful API for managing personal expenses on a monthly basis. The service is built using the following technologies:

- Spring Boot: to simplify the creation of a Spring application
- Spring Data JPA: to simplify access to relational databases using the data object pattern
- Spring Security: to provide a wide range of security features for web applications and RESTful services
- Thymeleaf: to create HTML templates used in the application
- Spring Task: to schedule tasks such as monthly alert notifications
- Spring Mail: to send email notifications to users
- Spring Boot Admin: to monitor and supervise the application's status
- Spring Boot Validation: to validate the input parameters in RESTful endpoints
- Spring Boot Web: to create RESTful endpoints that allow interaction with the application
- Spring Boot DevTools: to improve development experience

### Requirements
- Java 11 or higher
- MySQL database
- Redis cache server
- SMTP server for sending email notifications

### Getting Started
1.  Clone the repository
2.  Set up the MySQL database and Redis cache server
3.  Configure the SMTP server for sending email notifications
4.  Run the following command to start the application:

```bash
./mvnw spring-boot:run
```

Alternatively, you can build the application first and then run the generated jar file:

```bash
./mvnw clean package
java -jar target/monthly-expenses-0.0.1-SNAPSHOT.jar
```
5.  Access the application at http://localhost:8080

### RESTful Endpoints
The following RESTful endpoints are available:

- GET /expenses: Returns a list of all expenses
- GET /expenses/{id}: Returns the expense with the specified ID
- POST /expenses: Creates a new expense
- PUT /expenses/{id}: Updates the expense with the specified ID
- DELETE /expenses/{id}: Deletes the expense with the specified ID
- GET /expenses/search/findByMonthAndYear?month={month}&year={year}: Returns a list of expenses for the specified month and year
- POST /signup: Creates a new user account
- GET /activate?token={token}: Activates a user account
- POST /login: Authenticates a user and returns an access token
- POST /logout: Logs out the current user
- POST /sendAlert: Sends an alert to the user with the monthly expense summary

### Monitoring and Management
The following management endpoints are available:

- /actuator/health: Returns the health of the application
- /actuator/info: Returns information about the application
- /actuator/metrics: Returns metrics about the application
- /actuator/loggers: Returns or modifies the loggers used by the application
- /actuator/httptrace: Returns the HTTP requests and responses made by the application

To access these endpoints, you need to be authenticated with a user account that has the ACTUATOR role. The admin user account created during the application startup has this role.

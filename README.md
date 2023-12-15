# Spring MVC CRUD Web Application

This is a Spring MVC web application built using Java Springboot, SpringMVC, Thymeleaf and MYSQL database. It is designed for managing employee details through Create, Read, Update, and Delete (CRUD) operations.

## Features
- Add an Employee
- Delete an Employee
- Update an Employee

## Technologies Used
- Frontend:
  - Thymeleaf (Java Server-side template Engine to preview backend)
- Backend:
  - Java Springboot, SpringMVC
- Database:
  - MySQL

## Endpoints (Base path http://localhost:{PORT}/employees)
- `/list`: It contains a table represeting firstName, lastName and email of all the employees with update and delete button on the action column of each employees.
- `/showFormAdd`: This is accessed when add employee button is clicked which contains all the fields and a save button which saves the data to database amd redirect to `/list`.
- `/showFormForUpdate?employeeId=*`: It opens when update button is clicked and contains all the fields pre-populated.
- `/delete`: This endpoint basically deletes the employee.

## Project Structure
![p3](https://github.com/kravi770/Spring_MVC_CRUD/assets/99242457/3db75e21-fe90-4ac6-8e10-0cbf383d3309)

The project is structured as follows:

- `src/main/java/com/luv2code/springboot/thymeleafdemo/`: Contains all backend code.
  - `controller/EmployeeController.java`: Contains all the base mappings, getmappings, postmappings to create endpoints and other business logic related to these endpoints
  - `dao/`: It extends predefined JPA Respository to get all methods such as getAll(), update(), delete(), etc... that will be used to interact to database.
  - `entity/`: It contains the Java Class for the Employee and defines all the related fields.
  - `service/EmployeeServiceImpl.java`: This class provides a service layer to interact with different DAOs to further interact with database indirectly.
  - `ThymeleafdemoApplication.java`: This is the root file used to run Java Springboot application.
  



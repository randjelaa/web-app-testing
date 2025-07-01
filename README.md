# Student Management System Testing

## Overview

This repository contains automated tests and a bug report for a Student Management System consisting of:

* A **Spring Boot server** providing mock student data via RESTful CRUD endpoints.
* An **Angular client** application for managing student records.

The goal is to validate the correctness of CRUD operations on both client and server, identify bugs, and ensure data integrity through comprehensive testing.

---

## Features

* **Selenium WebDriver UI tests** covering the Angular client’s student data forms, tables, dialogs, and associated actions.
* **Postman API tests** verifying the REST endpoints’ data responses and HTTP status codes, including error handling (e.g., 404 Not Found).
* Detailed **bug report** documenting discovered issues in both server and client applications.

---

## Technologies Used

* Java 11+
* Selenium WebDriver with JUnit 5
* Postman for API testing
* Spring Boot (server, mock data)
* Angular (client application)

---

## Getting Started

### Running the Server

The server runs without a database and serves mock data.

```bash
java -jar aplikacija.jar
```

### Deploying the Client

Unpack the Angular client build into the ROOT folder of your web server (as per Exercise 7 setup) and start the web server. Clear any previous content in the ROOT folder before deploying.

### Running Tests

* **Selenium Tests:** Execute JUnit tests from the `selenium-tests` project.
* **Postman Tests:** Import and run the Postman collection included in the `postman-tests` folder.

---

## Bug Report Summary

The project includes a detailed report listing bugs found in both server and client applications, assisting in quality assurance and future improvements.

---

## Student Attributes

```java
private Long studentId;
private String studentName;
private String studentEmail;
private String studentBranch;
```

---

## Notes

* Tests assume a fresh server state (no students) at start; restart the server to reset data.
* Browser developer tools (e.g., Chrome DevTools) with disabled cache are recommended during UI testing.
* Tests focus strictly on core CRUD functionality; UI elements like menus and search are excluded.



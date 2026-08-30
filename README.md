# E-Commerce Test Automation 

A complete **end-to-end test automation framework** for an e-commerce application using **Java, Selenium, TestNG, Rest Assured, Maven, Git, and Jenkins**.


---

## 📌 Project Overview

This project automates an e-commerce application across multiple layers:

```text
                         E-Commerce Application
                                  │
                   ┌──────────────┴──────────────┐
                   ↓                             ↓
             UI Automation                  API Automation
               Selenium                    Rest Assured
                   │                             │
                   ↓                             ↓
                TestNG                        TestNG
                   │                             │
                   └──────────────┬──────────────┘
                                  ↓
                         Automation Framework
                                  │
                    ┌─────────────┼─────────────┐
                    ↓             ↓             ↓
                  POM         Utilities      Test Data
                    │             │             │
                    └─────────────┼─────────────┘
                                  ↓
                                Maven
                                  ↓
                                 Git
                                  ↓
                               Jenkins
                                  ↓
                               Reports
```

---

## 🎯 Project Objectives

The main objectives are:

* Automate critical e-commerce workflows.
* Automate UI scenarios using Selenium WebDriver.
* Automate REST APIs using Rest Assured.
* Use TestNG for test execution and assertions. 
* Generate test execution reports.
* Integrate the framework with Git and Jenkins.
* Execute UI and API tests through CI/CD.
---

# 🛠️ Technology Stack

| Technology              | Purpose                            |
| ----------------------- | ---------------------------------- |
| Java                    | Programming language               |
| Selenium WebDriver      | UI automation                      |
| TestNG                  | Test execution and assertions      |
| Rest Assured            | REST API automation                |
| Maven                   | Build and dependency management    |
| Git                     | Version control                    |
| GitHub                  | Source code repository             |
| Jenkins                 | CI/CD                              |
| SQL                     | Database validation                |

---

# 📋 Prerequisites

Before working on this project, you should have basic knowledge of:

### Java

* OOP
* Classes and objects
* Inheritance
* Interfaces
* Exception handling
* Collections
* Strings
* Arrays
* File handling
* Java 8+ features

### Selenium

* WebDriver
* Locators
* XPath
* CSS Selectors
* WebElement
* Explicit waits
* Actions
* Frames
* Alerts
* Windows/Tabs
* JavaScriptExecutor

### TestNG

* `@Test`
* `@BeforeMethod`
* `@AfterMethod`
* `@BeforeClass`
* `@AfterClass`
* Assertions
* Groups
* DataProvider
* Parameters
* Dependencies
* `testng.xml`
* Parallel execution

### API Testing

* HTTP/HTTPS
* REST
* GET/POST/PUT/PATCH/DELETE
* Headers
* Query parameters
* Path parameters
* Request body
* JSON
* Authentication
* HTTP status codes

### Tools

* IntelliJ IDEA / Eclipse
* JDK
* Maven
* Git
* GitHub
* Postman
* Jenkins

---

# 🛒 E-Commerce Modules

The project will cover the following modules.

## 1. User Registration

### UI

* Open registration page
* Enter valid user details
* Register user
* Verify successful registration

### API

```text
POST /users
```

### Test scenarios

* Valid registration
* Duplicate email
* Invalid email
* Missing fields
* Empty fields
* Invalid password
* Boundary values

---

# 2. Login

### UI

```text
Open Login
     ↓
Enter Username
     ↓
Enter Password
     ↓
Click Login
     ↓
Verify Dashboard
```

### API

```text
POST /login
```

### Test scenarios

* Valid credentials
* Invalid username
* Invalid password
* Empty username
* Empty password
* Locked user
* Invalid token
* Expired token

---

# 3. Product Search

### UI

```text
Search Product
      ↓
Verify Results
      ↓
Select Product
```

### API

```text
GET /products
GET /products?search=laptop
```

### Validations

* Search result count
* Product name
* Product ID
* Price
* Availability
* Category

---

# 4. Product Details

### UI

Verify:

* Product name
* Product image
* Price
* Description
* Category
* Stock
* Rating

### API

```text
GET /products/{id}
```

Verify that API and UI display consistent product information.

---

# 5. Shopping Cart

### UI

```text
Product
   ↓
Add to Cart
   ↓
Open Cart
   ↓
Update Quantity
   ↓
Remove Product
```

### API

```text
POST   /cart
GET    /cart
PUT    /cart/{id}
DELETE /cart/{id}
```

### Test scenarios

* Add product
* Add multiple products
* Update quantity
* Remove product
* Empty cart
* Verify total price
* Verify cart count

---

# 6. Wishlist

### UI

* Add product to wishlist
* Remove product
* View wishlist
* Move product to cart

### API

```text
POST   /wishlist
GET    /wishlist
DELETE /wishlist/{id}
```

---

# 7. Address Management

Test:

* Add address
* Edit address
* Delete address
* Select default address
* Invalid address data

Example API:

```text
POST   /addresses
GET    /addresses
PUT    /addresses/{id}
DELETE /addresses/{id}
```

---

# 8. Checkout

### UI

```text
Cart
 ↓
Address
 ↓
Shipping
 ↓
Payment
 ↓
Place Order
 ↓
Order Confirmation
```

### API

```text
POST /orders
GET  /orders/{id}
```

Validate:

* Order ID
* Products
* Quantity
* Price
* Tax
* Shipping
* Discount
* Final total
* Order status

---

# 9. Orders

### UI

```text
My Orders
    ↓
Order Details
```

### API

```text
GET /orders
GET /orders/{id}
```

Validate that UI and API return consistent order information.

---

# 🔄 UI + API Integration Testing

One of the main goals of this project is to demonstrate **API + UI integration**.

Instead of performing all setup through the UI:

```text
Open Browser
    ↓
Register User
    ↓
Login
    ↓
Create Product
    ↓
Add Product
    ↓
Checkout
```

Use APIs for test data/setup where appropriate:

```text
API
 ↓
Create User
 ↓
Generate Token
 ↓
Create Cart
 ↓
Create Test Data
 ↓
Selenium
 ↓
Open UI
 ↓
Validate Data
 ↓
API
 ↓
Validate Backend Data
```

Example:

```text
API:
Quantity = 2

        ↓

UI:
Quantity = 2

        ↓

Database:
Quantity = 2
```

This provides stronger end-to-end validation.

---

# 🏗️ Framework Architecture

```text
                    Test Automation Framework
                              │
              ┌───────────────┴───────────────┐
              ↓                               ↓
        UI Automation                    API Automation
          Selenium                       Rest Assured
              │                               │
              ↓                               ↓
         Page Objects                    API Clients
              │                               │
              └───────────────┬───────────────┘
                              ↓
                            TestNG
                              │
                              ↓
                           Assertions
                              │
                              ↓
                        Test Data / Config
                              │
                              ↓
                            Maven
                              │
                              ↓
                             Git
                              │
                              ↓
                           Jenkins
                              │
                              ↓
                           Reports
```

---

# 📁 Project Structure

```text
ecommerce-test-automation/
│
├── pom.xml
├── testng.xml
├── README.md
├── .gitignore
│
├── src/
│   │
│   ├── main/
│   │   └── java/
│   │       │
│   │       ├── pages/
│   │       │   ├── LoginPage.java
│   │       │   ├── HomePage.java
│   │       │   ├── ProductPage.java
│   │       │   ├── CartPage.java
│   │       │   ├── CheckoutPage.java
│   │       │   └── OrderPage.java
│   │       │
│   │       ├── api/
│   │       │   ├── ApiClient.java
│   │       │   ├── UserApi.java
│   │       │   ├── ProductApi.java
│   │       │   ├── CartApi.java
│   │       │   └── OrderApi.java
│   │       │
│   │       ├── models/
│   │       │   ├── User.java
│   │       │   ├── Product.java
│   │       │   ├── Cart.java
│   │       │   └── Order.java
│   │       │
│   │       ├── utils/
│   │       │   ├── ConfigReader.java
│   │       │   ├── DriverFactory.java
│   │       │   ├── WaitUtils.java
│   │       │   ├── ScreenshotUtils.java
│   │       │   ├── JsonUtils.java
│   │       │   └── TestDataUtils.java
│   │       │
│   │       ├── config/
│   │       │   ├── qa.properties
│   │       │   └── staging.properties
│   │       │
│   │       └── constants/
│   │           └── FrameworkConstants.java
│   │
│   └── test/
│       └── java/
│           │
│           ├── ui/
│           │   ├── LoginTest.java
│           │   ├── ProductTest.java
│           │   ├── CartTest.java
│           │   ├── CheckoutTest.java
│           │   └── OrderTest.java
│           │
│           ├── api/
│           │   ├── LoginApiTest.java
│           │   ├── ProductApiTest.java
│           │   ├── CartApiTest.java
│           │   └── OrderApiTest.java
│           │
│           └── integration/
│               ├── ProductIntegrationTest.java
│               ├── CartIntegrationTest.java
│               └── OrderIntegrationTest.java
│
└── test-data/
    ├── users.json
    ├── products.json
    └── orders.json
```

---

# ⚙️ Maven Configuration

Maven manages project dependencies and test execution.

Important dependencies include:

```text
Selenium
TestNG
Rest Assured
Jackson
Logging
Reporting
```

The test suite can be executed using:

```bash
mvn clean test
```

---

# 🧪 TestNG

TestNG is responsible for:

* Test execution
* Assertions
* Test grouping
* Data-driven testing
* Dependencies
* Parallel execution
* Setup/teardown

Example:

```java
@Test(groups = "smoke")
public void loginTest() {
    // test
}
```

---

# 🔌 API Automation

Rest Assured is used for REST API automation.

Example GET:

```java
given()
.when()
    .get("/products")
.then()
    .statusCode(200);
```

Example POST:

```java
given()
    .contentType("application/json")
    .body(requestBody)
.when()
    .post("/users")
.then()
    .statusCode(201);
```

API validations include:

* Status code
* Response body
* Headers
* Schema
* Response time
* Authentication
* Error handling
* Data consistency

---

# 🔐 Authentication

The framework will support authentication workflows such as:

```text
Login API
    ↓
Generate Token
    ↓
Token Manager
    ↓
Store Token
    ↓
Use Token
    ↓
Protected APIs
```

Example:

```java
given()
    .header("Authorization", "Bearer " + token)
.when()
    .get("/orders")
.then()
    .statusCode(200);
```

---

# 🗄️ Database Validation

Where database access is available, validate backend data using SQL.

Example:

```sql
SELECT *
FROM orders
WHERE order_id = 101;
```

Validation flow:

```text
UI
 ↓
API
 ↓
Database
```

This helps verify complete data flow across the application.

---

# 📊 Test Strategy

Each major feature should contain:

### Functional Tests

```text
Positive scenarios
Negative scenarios
Boundary scenarios
```

### UI Tests

```text
Navigation
UI validation
User interactions
Error messages
```

### API Tests

```text
Request validation
Response validation
Authentication
Authorization
Negative testing
```

### Integration Tests

```text
API → UI
API → Database
UI → API → Database
```

---

# 🧩 Test Categories

Tests will be organized into groups:

```text
smoke
regression
functional
api
ui
integration
```

Example:

```java
@Test(groups = {"smoke", "ui"})
public void loginTest() {
}
```

Run only smoke tests through TestNG configuration.

---

# 📸 Screenshots

For failed UI tests, the framework should automatically capture screenshots.

Example:

```text
test failure
     ↓
Screenshot
     ↓
Reports
```

Screenshots should be attached or linked from the generated report where supported.

---

# 📝 Logging

Logging will capture important execution information:

```text
Test started
Browser launched
Application opened
Login performed
API request sent
API response received
Product added
Order created
Assertion passed/failed
Test completed
```

Logging helps diagnose failures during local and CI execution.

---

# 📈 Reporting

The framework should generate reports containing:

* Total tests
* Passed tests
* Failed tests
* Skipped tests
* Execution duration
* Failure details
* Screenshots
* API request/response information where appropriate

Possible reporting tools:

```text
Allure
Extent Reports
TestNG Reports
```

---

# 🌐 Environment Configuration

The framework should support multiple environments:

```text
QA
Staging
Production
```

Example:

```properties
browser=chrome
baseUrl=https://qa.example.com
apiBaseUrl=https://api.qa.example.com
```

The environment should be configurable without changing test code.

---

# 🔄 CI/CD Pipeline

The project will eventually integrate with Jenkins.

```text
Developer
    ↓
Git Push
    ↓
GitHub
    ↓
Jenkins
    ↓
Checkout Code
    ↓
Maven Build
    ↓
TestNG
    ↓
API Tests
    ↓
UI Tests
    ↓
Reports
    ↓
PASS / FAIL
```


## 👨‍💻 Author

**Junaid**

This project is intended as a practical SDET portfolio project demonstrating **UI automation, API automation, framework design, integration testing, and CI/CD practices**.

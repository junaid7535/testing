# E-Commerce API Testing & Automation

## 📌 Project Overview

This repository contains the testing documentation and automation work for an E-commerce application developed as part of my participation in Flipkart GRID 7.0.

The project focuses primarily on **API Testing**, along with **Manual Testing** and selected **UI Automation** scenarios for critical user journeys.

The objective of this project is to demonstrate practical software testing skills by testing important E-commerce functionalities such as authentication, product management, shopping cart, checkout, and order processing.

---

## 🎯 Testing Objectives

The main objectives of this project are:

* Validate core E-commerce application functionality.
* Perform API testing for important application modules.
* Create and execute manual test cases.
* Identify and document defects.
* Validate API request and response data.
* Perform positive and negative testing.
* Validate HTTP status codes and error responses.
* Automate selected critical UI scenarios.
* Generate and maintain testing reports.

---

## 🛒 Application Modules Tested

The following modules are covered in this project:

### 🔐 Authentication

* User Registration
* User Login
* Invalid Login
* Password Validation
* Logout

### 📦 Product

* Product Search
* Product Details
* Product Availability
* Product Validation

### 🛒 Shopping Cart

* Add Product to Cart
* Remove Product from Cart
* Update Product Quantity
* Validate Cart Total

### 💳 Checkout

* Address Validation
* Order Summary
* Checkout Validation

### 📋 Orders

* Order Placement
* Order Confirmation
* Order Details

---

# 🧪 Testing Types

The following testing activities are included:

* Functional Testing
* Manual Testing
* API Testing
* API Validation
* Positive Testing
* Negative Testing
* Boundary Value Testing
* Smoke Testing
* Regression Testing
* UI Testing
* UI Automation

---

# 🔌 API Testing

API testing is the primary focus of this project.

The following API validations are performed:

* HTTP Status Code Validation
* Response Body Validation
* Request Parameter Validation
* Response Header Validation
* Authentication Validation
* Invalid Request Validation
* Missing Field Validation
* Error Message Validation
* Response Time Validation

Example API modules:

```text
Authentication API
Product API
Cart API
Order API
```

---

# 🧰 Tools & Technologies

| Category             | Tools              |
| -------------------- | ------------------ |
| API Testing          | Postman            |
| API Automation       | Postman / Newman   |
| UI Automation        | Selenium           |
| Programming Language | Java               |
| Build Tool           | Maven              |
| Version Control      | Git                |
| Repository Hosting   | GitHub             |
| Test Management      | Excel              |
| IDE                  | Visual Studio Code |

---

# 📁 Project Structure

```text
Ecommerce-API-Testing-Automation/
│
├── README.md
│
├── Documentation/
│   ├── Project_Overview.md
│   └── Test_Plan.md
│
├── Test_Cases/
│   ├── Authentication.xlsx
│   ├── Product.xlsx
│   ├── Cart.xlsx
│   ├── Checkout.xlsx
│   └── Orders.xlsx
│
├── Bug_Reports/
│   └── Bug_Report.xlsx
│
├── API_Testing/
│   ├── Postman_Collection.json
│   └── API_Test_Cases.xlsx
│
├── Automation/
│   └── Selenium_Framework/
│
├── Screenshots/
│
└── Reports/
    └── Test_Summary_Report.md
```

---

# 📋 Test Case Coverage

Test cases are created for the following areas:

| Module         | Coverage                         |
| -------------- | -------------------------------- |
| Authentication | Login and validation scenarios   |
| Product        | Search and product details       |
| Cart           | Add, remove and update products  |
| Checkout       | Checkout validation              |
| Orders         | Order placement and confirmation |
| API            | Request and response validation  |

---

# 🐞 Bug Reporting

Defects identified during testing are documented with the following information:

* Bug ID
* Module
* Bug Summary
* Preconditions
* Steps to Reproduce
* Expected Result
* Actual Result
* Severity
* Priority
* Bug Status
* Screenshot

---

# 🤖 Automation Coverage

Selected critical user journeys are automated using Selenium.

Examples include:

```text
User Login
     ↓
Product Search
     ↓
Product Selection
     ↓
Add Product to Cart
```

Automation is focused on important user workflows rather than attempting to automate every test scenario.

---

# 🚀 How to Use This Repository

### Clone the repository

```bash
git clone <your-github-repository-url>
```

### Navigate to the project

```bash
cd Ecommerce-API-Testing-Automation
```

### API Testing

1. Open Postman.
2. Import the Postman collection.
3. Configure the required environment variables.
4. Execute the API requests.
5. Validate request and response data.

### UI Automation

1. Navigate to the automation framework.

```bash
cd Automation/Selenium_Framework
```

2. Configure the required dependencies.
3. Update application configuration if required.
4. Run the automation tests.

---

# 📊 Test Reporting

The project includes testing reports containing:

* Total Test Cases
* Passed Test Cases
* Failed Test Cases
* Blocked Test Cases
* Bugs Identified
* Severity Distribution
* Test Execution Summary

Reports are available in the `Reports` directory.

---

# 🎓 Key Learnings

Through this project, I gained practical experience in:

* Understanding E-commerce business workflows.
* Creating test scenarios and test cases.
* Performing API testing.
* Validating REST API responses.
* Testing positive and negative scenarios.
* Defect identification and reporting.
* UI testing.
* Test automation fundamentals.
* Using Git and GitHub for project management.

---

# 🏆 Flipkart GRID 7.0

This project is based on practical experience gained while participating in **Flipkart GRID 7.0**, where I worked on an E-commerce application.

The testing work in this repository represents my own testing practice and documentation created for the application.

> Note: This repository is a personal QA/testing portfolio project and does not imply official endorsement or affiliation with Flipkart beyond participation in Flipkart GRID 7.0.

---

# 👨‍💻 Author

**Your Name**

QA Engineer | Software Tester

Skills:

* Manual Testing
* API Testing
* Postman
* REST API Testing
* Selenium
* Java
* SQL
* Git & GitHub

---

## ⭐ If You Like This Project

Feel free to explore the repository and review the testing documentation, API testing artifacts, and automation work.


# ECommerce Postman Framework

## Project Overview

This project is an end-to-end API automation framework built using Postman for a demo ECommerce application.

The framework validates complete business workflows including authentication, product management, order creation, and cleanup operations.
It also includes negative scenario validations, schema validation, data-driven execution, and Newman HTML reporting.

---

## Tech Stack

- Postman
- Newman
- JavaScript
- CSV Data-Driven Testing
- Newman HTML Extra Reporter

---

## Features

- End-to-end API workflow automation
- Dynamic token and ID chaining
- Environment and collection variables
- Data-driven testing using CSV
- JSON schema validation
- Positive and negative scenario coverage
- Newman HTML reporting
- Organized project structure
- Reusable validation approach

---

## Workflow Covered

The following E2E workflow is automated:

1. User Login
2. Get All Products
3. Create Product
4. Create Order
5. View Order Details
6. Delete Order
7. Delete Product

### Negative Scenarios Covered

- Invalid login
- Create product without token
- Create order with invalid product ID
- Create product without payload
- View deleted order details

---

## Project Structure

```text
PostmanProject/
│
├── collections/
│   └── ECom_E2E_flow.postman_collection.json
│
├── environments/
│   └── QA.postman_environment.json
│
├── test-data/
│   ├── ProductData.csv
│   └── SampleImage.jpg
│       
├── reports/
│   └── newman-report.html
│
├── screenshots/
│
└── README.md
````

---

## Prerequisites

Ensure the following tools are installed:

* Postman
* Node.js
* Newman

### Install Newman

```bash
npm install -g newman
```

### Install Newman HTML Extra Reporter

```bash
npm install -g newman-reporter-htmlextra
```

---

## How To Run The Collection

### Run Using Newman

```bash
newman run collections/ECom_E2E_flow.postman_collection.json ^
-d test-data/ProductData.csv ^
-e environments/QA.postman_environment.json ^
-r cli,htmlextra ^
--reporter-htmlextra-export reports/newman-report.html
```

---

## Important Note

Before executing the Positive Scenarios collection, manually attach the sample image available inside the `test-data/images/` folder 
in the `productImage` form-data field of the `Create Product` request.

---

## Reporting

The framework generates detailed Newman HTML reports after execution.

Generated report location:

```text
reports/newman-report.html
```

---

## Screenshots

### Postman Collection Execution
<img width="1578" height="958" alt="PostmanCollectionRunnerResult" src="https://github.com/user-attachments/assets/ac0b1cc0-1562-409a-9599-3d418784be35" />

---

### Newman HTML Report
<img width="925" height="893" alt="NewmanReportScreenshot" src="https://github.com/user-attachments/assets/cd2a9d01-49f2-40cf-947e-af59a1c5b086" />

---

## Author

Deepasree S

QA Automation Engineer




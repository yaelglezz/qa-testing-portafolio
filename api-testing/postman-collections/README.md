# Postman Collections – Urban Grocers API

This folder contains a Postman collection used to test the **Urban Grocers API**, focusing on adding products to shopping kits.

---

## 🎯 Key QA Focus
Validate backend behavior when adding products to kits, ensuring correct data handling, proper error responses, and enforcement of business rules.

---

## 🔍 Scope
The collection covers **manual API testing** executed in Postman, including:

- Positive scenarios for adding existing products to existing kits
- Negative scenarios validating backend error handling
- Boundary Value Analysis and Equivalence Class Partitioning
- Validation of HTTP status codes and JSON responses

---

## 🧪 Validated Scenarios
- Adding products with valid kit and product IDs (`200 OK`)
- Adding products with non-existing product IDs (`400 Bad Request`)
- Adding products to non-existing kits (`404 Not Found`)
- Invalid request body structure (`400 Bad Request`)
- Exceeding the limit of **30 unique products per kit** (`400 Bad Request`)

All API responses were validated in **JSON format**.

---

## 🗂 Collection Structure
The collection is organized to reflect real QA workflows:

- **Positive Scenarios** – Valid requests that should be processed successfully
- **Negative Scenarios** – Invalid inputs to validate backend error handling

Each request is named using the convention:
**Action + Resource – Condition being validated**

---

## 🔗 Test Case Traceability
All scenarios executed in this collection were designed based on documented **API test cases**, including:

- Positive and negative cases
- Equivalence classes
- Boundary values

Related test case documentation can be found in: *api-testing/test-cases/*

---

## 🐞 Bug Reporting
Any scenario that produced:
- An unexpected success response
- An incorrect HTTP status code
- An incorrect error message

was reported and tracked in **Jira**, ensuring proper defect documentation and follow-up.

---

## 🚀 How to Use This Collection
1. Download the `.postman_collection.json` file
2. Import it into Postman
3. Configure required variables if applicable (e.g. `baseUrl`, `:id`)
4. Execute requests from the **Positive** and **Negative** scenario folders
5. Validate responses against expected results

---

## 🛠 Tools
- **Postman** – Manual API testing and request execution  
- **JSON-based REST API**  
- **Jira** – Bug reporting and tracking  
- **GitHub** – Version control and test documentation

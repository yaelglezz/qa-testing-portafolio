
# API Testing – Urban Grocers

## 📌 Project Overview

This section contains API testing artifacts created for the **Urban Grocers** project, an online grocery platform where users can create custom shopping kits or purchase predefined ones.

The main objective of this project was to **design, execute, and validate API test cases** for the functionality of **adding products to a kit**, covering both **positive and negative scenarios**, and ensuring correct backend behavior according to business rules and technical specifications.

All API responses were returned and validated in **JSON format**

---

## 🔍 Scope of Testing

The API testing focused on validating:

- Adding existing products to an existing kit
- Handling invalid or non-existent product IDs
- Handling invalid or non-existent kit IDs
- Request body structure and data validation
- Business constraints and limits enforced by the backend

---

## 📄 Test Design Techniques Applied

- Positive and Negative Test Cases
- Equivalence Classes
- Boundary Value Analysis

The following elements were explicitly validated:

- Kit ID (valid, invalid, non-existent)
- Product ID (valid, invalid, negative, non-existent)
- `quantity` field in the request body
- Structure and data type of `productsList`
- Length and structure of the `productsList` array
- Maximum limit of **30 unique products per kit**

---

## 📝 API Response Validation

For each request, the following aspects were validated:

- HTTP status code
- JSON response body structure
- Presence and correctness of response fields
- Error messages returned by the API in negative scenarios

---

## ❌ Expected Error Handling (Negative Scenarios)

The API was expected to return the following responses in negative cases:

- **400 Bad Request**
  - When product IDs do not exist
  - When request body structure is invalid (e.g. `productsList` is not an array)

- **404 Not Found**
  - When attempting to add products to a non-existent kit

- **400 Bad Request** with the following error message:
  ```json
  {
    "message": "No more than 30 items per kit"
  }
  ```
  When exceeding the maximum limit of 30 unique products per kit

---

## 🐞 Test Execution & Defect Reporting

- Test cases were executed using **Postman**
- API responses were validated based on:
  - HTTP status codes
  - JSON response body
  - Business logic enforcement
- Any discrepancies where:
  - A negative test returned a positive response, or
  - An unexpected response was returned
    were **reported as defects in Jira**, including reproduction steps and supporting evidence

---

## 🛠 Tools Used

- **Postman** - API request execution and JSON validation
- **Jira** - Defect tracking and reporting
- **Google Sheets** - Test case design and execution tracking

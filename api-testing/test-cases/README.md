# API Test Cases – Urban Grocers

## 📌 Project Overview
This section contains the **API test cases** designed and executed for the **Urban Grocers** project.

Urban Grocers is an online store that allows users to create custom shopping kits or purchase predefined kits.  
The main objective of this testing phase was to **validate the backend behavior when adding products to a kit**, covering both **positive and negative scenarios**.

---

## 🎯 Testing Objective
The API testing focused on verifying that the backend:

- Correctly adds products to an existing kit
- Properly validates request data
- Returns correct HTTP status codes
- Enforces business rules and constraints
- Handles invalid inputs gracefully

---

## 🔍 Scope of Testing
The following elements were tested:

- **Kit ID**
- **Product ID**
- **`quantity` field in the request body**
- **Structure of `productsList` array**
- **Length of `productsList`**
- **Maximum limit of unique products per kit (30 products)**

---

## 🧪 Test Design Techniques Applied
The test cases were designed using the following techniques:

- Positive and Negative Testing
- Equivalence Class Partitioning
- Boundary Value Analysis

---

## 📄 Test Case Structure
Each test case includes:

- Test case ID
- Test description
- Endpoint and HTTP method
- Request parameters and body
- Expected result
- Actual result
- Status (Passed / Failed)
- Link to Jira bug report (when applicable)

---

## ✅ Positive Test Cases
Examples of validated scenarios:

- Adding an existing product to an existing kit
- Adding multiple valid products within the allowed limit
- Sending a correctly structured request body

**Expected result:**
- HTTP status code `200 OK`
- Product successfully added to the kit

---

## ❌ Negative Test Cases
The following negative scenarios were tested and validated:

### 1. Non-existent Product ID
- **Expected:** `400 Bad Request`

### 2. Non-existent Kit ID
- **Expected:** `404 Not Found`

### 3. Invalid Request Body Structure
Examples:
- `productsList` is not an array  
- Missing required fields

- **Expected:** `400 Bad Request`

### 4. Exceeding Product Limit
- Adding more than **30 unique products** to a kit

- **Expected:**
```json
  {
    "message": "No más de 30 artículos por conjunto"
  }
```
- HTTP status code: 400n Bad Request

---

## 🐞 Bug Reporting

Any test case that produced:
- An unexpected success response
- An incorrect error response
was reported in Jira, including:
- Steps to reproduce
- Expected vs actual results
- Environment details
- Evidence when applicable
Links to Jira tickets are included directly in the test cases.

---

## 🛠 Tools Used

- Postman – API request execution
- Jira – Bug tracking and reporting
- GitHub – Test documentation and version control

---

## 📁 Related Resources

- Postman Collection:
  `api-testing/postman-collections/urban-grocers.postman_collection.json`

---

## 📌 Notes

- All API responses were validated in JSON format
- Testing focused on backend validation, independent of UI beha

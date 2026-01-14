# Equivalence Classes

## 📌 Overview

This section documents the application of **Equivalence Class Partitioning (ECP)** as a test design technique in two projects:

- **Urban Routes** (Web Application)
- **Urban Grocers** (REST API)

Equivalence Classes were used to reduce the total number of test cases while maintaining effective coverage by grouping inputs that are expected to produce the same system behavior.

---

## 🎯 Purpose of Equivalence Class Testing

Equivalence Class Partitioning helps to:

- Identify valid and invalid input groups
- Optimize test coverage without redundant cases
- Detect defects related to input validation
- Ensure consistent system behavior across similar inputs

---

## 🧪 Projects Covered

### 🚗 Urban Routes – Web Application

Equivalence classes were designed for user input fields and functional flows, including:

#### 📍 Route Input Fields

**“From” and “To” fields**
- Valid class: Existing and valid addresses
- Invalid class: Non-existing addresses
- Invalid class: Empty input
- Invalid class: Unsupported characters or formats

Expected behavior:
- Routes are generated only for valid address combinations
- Travel options remain disabled when inputs are invalid

---

#### 💳 Payment Method Form

**Card Number field**
- Valid class: Numeric input with exact required length
- Invalid class: Numeric input with incorrect length
- Invalid class: Non-numeric characters
- Invalid class: Empty field

**Security Code field**
- Valid class: Numeric input with required length
- Invalid class: Incorrect length
- Invalid class: Non-numeric input
- Invalid class: Empty field

Expected behavior:
- The **“Add”** button is enabled only when both fields belong to valid equivalence classes

---

### 🛒 Urban Grocers – API

Equivalence classes were applied to API request parameters when adding products to a kit.

#### 📦 Request Parameters

**Kit ID**
- Valid class: Existing kit ID
- Invalid class: Non-existing kit ID

**Product ID**
- Valid class: Existing product ID
- Invalid class: Non-existing product ID
- Invalid class: Unsupported or malformed ID

**Request Body (`productsList`)**
- Valid class: Array with valid product objects
- Invalid class: Non-array data type
- Invalid class: Empty array
- Invalid class: Exceeding allowed product limit

Expected behavior:
- Valid classes return successful responses (`200 OK`)
- Invalid classes return appropriate error responses (`400 Bad Request`, `404 Not Found`)

---

## 🛠 Tools Used

- Manual testing (Web UI)
- Postman (API testing)
- Google Sheets (test case design)
- Jira (defect tracking)

---

## ✅ Key QA Focus

- Clear separation of valid vs invalid input groups
- Reduction of redundant test cases
- Effective coverage of input validation logic
- Alignment with business and technical requirements


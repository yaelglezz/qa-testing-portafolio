
# Boundary Value Analysis

## 📌 Overview

This folder contains artifacts created using **Boundary Value Analysis (BVA)** as a test design technique.  
The objective is to validate system behavior at the **edges of allowed input ranges**, where defects are more likely to occur.

Boundary Value Analysis was applied to both **web UI** and **API** testing scenarios to improve coverage and detect edge-case defects efficiently.

---

## 🎯 Why Boundary Value Analysis

Boundary Value Analysis helps to:
- Detect defects at minimum and maximum limits
- Validate business rules and constraints
- Reduce redundant test cases while maintaining strong coverage
- Identify unexpected system behavior at edge conditions

---

## 🧪 Application by Project

### 🚗 Urban Routes (Web Application)

Boundary values were considered for:
- Required form fields (empty vs filled states)
- Input behavior before and after required fields are completed
- UI state changes when reaching valid/invalid input conditions

Examples:
- Empty input vs first valid character
- Transition from invalid to valid form state
- UI behavior when mandatory fields are just completed

---

### 🛒 Urban Grocers (API)

Boundary Value Analysis was applied to API endpoints related to **adding products to shopping kits**, focusing on:

- `quantity` field values:
  - Minimum allowed value
  - Maximum allowed value
  - Values just outside valid limits
- Number of unique products per kit:
  - Maximum allowed: **30**
  - Boundary scenarios:
    - 29 products
    - 30 products
    - 31 products (invalid)
- Request body structure limits:
  - Empty arrays
  - Single-element arrays
  - Arrays exceeding allowed limits

---

## 📝 Test Design Artifacts

The boundary value scenarios documented in this folder include:
- Valid boundary cases
- Invalid boundary cases
- Expected API responses (status codes and error messages)
- Alignment with backend business rules

All test cases were designed before execution and later validated during API testing.

---

## 🐞 Defect Detection

When boundary conditions resulted in:
- Unexpected positive responses
- Incorrect error codes
- Missing or incorrect validation

The issues were **reported and tracked in Jira**, including detailed reproduction steps and evidence.

---

## 🛠 Tools Used

- Google Sheets – Boundary value documentation
- Postman – API execution and response validation
- Jira – Defect tracking

---

## ✅ Key QA Focus

- Identifying edge cases early
- Validating system behavior at limits
- Ensuring backend constraints are properly enforced
- Applying test design techniques aligned with real QA workflows

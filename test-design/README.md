# Test Design

## 📌 Overview

This section contains test design artifacts created as part of my QA training and practice.  
The goal of this folder is to demonstrate how **test design techniques** are applied to ensure effective test coverage, reduce redundancy, and identify edge cases in both **UI** and **API** testing.

The test design techniques documented here were applied to real practice projects:
- **Urban Routes** (Web / Manual Testing)
- **Urban Grocers** (API Testing)

---

## 🎯 Test Design Techniques Applied

The following techniques were used to design structured and effective test cases:

### 🔹 Equivalence Classes
Used to divide input data into valid and invalid groups that are expected to behave similarly, allowing test coverage with fewer but more meaningful test cases.

### 🔹 Boundary Value Analysis
Used to validate system behavior at the limits of acceptable input values, where defects are more likely to occur.

---

## 🧪 Application by Project

### 🚗 Urban Routes (Web Application)

Test design techniques were applied to:
- Form input validation (origin and destination fields)
- UI behavior and interaction flows
- Functional restrictions when required fields are missing or invalid

Techniques used:
- Equivalence Classes
- Boundary Value Analysis

Artifacts related to this project can be found in:
- `manual-testing/`
- `test-design/equivalence-classes/`
- `test-design/boundary-values/`

---

### 🛒 Urban Grocers (API)

Test design techniques were applied to API endpoints related to **adding products to shopping kits**, focusing on:

- Kit ID validation
- Product ID validation
- `quantity` field validation
- Structure and limits of the `productsList` array
- Business rule enforcing a maximum of **30 unique products per kit**

Techniques used:
- Equivalence Classes
- Boundary Value Analysis
- Positive and Negative test scenarios

Artifacts related to this project can be found in:
- `api-testing/`
- `test-design/equivalence-classes/`
- `test-design/boundary-values/`

---

## 📂 Folder Structure

- `equivalence-classes/`  
  Contains documentation and examples of equivalence class partitioning applied to both UI and API scenarios.

- `boundary-values/`  
  Contains boundary value analysis applied to critical input fields and business limits.

---

## 🛠 Tools Used

- Google Sheets – Test design documentation
- Postman – API validation
- Jira – Defect reporting and tracking

---

## ✅ Key QA Focus

- Designing tests before execution
- Improving test coverage with fewer but effective cases
- Identifying edge cases and negative scenarios
- Applying test design techniques aligned with real QA workflows

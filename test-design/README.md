# Test Design – Urban Grocers API

## 📌 Overview

This section documents the **test design process** applied during API testing for the **Urban Grocers** project.

The goal of this folder is to demonstrate how test cases were **systematically designed** using formal QA techniques before execution, ensuring proper coverage of business rules, validations, and edge cases related to adding products to shopping kits.

---

## 🎯 Purpose of Test Design

Test design was used to:
- Identify valid and invalid input scenarios
- Reduce redundant test cases while maintaining coverage
- Validate backend constraints and business rules
- Detect edge cases that could lead to unexpected API behavior

These techniques were applied **before executing requests in Postman**.

---

## 🧠 Test Design Techniques Applied

The following techniques were used:

### 1️⃣ Equivalence Classes
Used to group input data into **valid and invalid categories**, allowing efficient test coverage without testing every possible value.

Examples:
- Valid vs invalid Kit IDs
- Existing vs non-existing Product IDs
- Valid vs invalid `quantity` values
- Correct vs incorrect request body structure

📂 See details in:
   *test-design/equivalence-classes/*

---

### 2️⃣ Boundary Value Analysis
Used to test **edge values** around defined limits, especially where business constraints exist.

Examples:
- Minimum and maximum allowed values for `quantity`
- Limits on Kit IDs and Product IDs
- Maximum limit of **30 unique products per kit**

📂 See details in:
   *test-design/boundary-values/*

---

## 🔗 Relationship with Test Cases

- Test cases documented in `api-testing/test-cases/` were derived from:
  - Equivalence Classes
  - Boundary Value Analysis
- This ensures that test execution is:
  - Traceable
  - Structured
  - Based on QA best practices, not ad-hoc testing

---

## 🛠 Tools Used

- Test design documentation: Google Sheets
- Test execution: Postman
- Defect tracking: Jira

---

## ✅ Why This Matters

This folder demonstrates:
- Understanding of **formal test design techniques**
- Ability to design tests **before execution**
- Alignment with real-world QA processes used in professional teams

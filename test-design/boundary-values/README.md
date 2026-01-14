# Boundary Value Analysis (BVA)

## 📌 Overview

This section documents the application of **Boundary Value Analysis (BVA)** as a test design technique across two projects:

- **Urban Routes** (Web Application)
- **Urban Grocers** (REST API)

Boundary Value Analysis was used to validate system behavior at the **edges of allowed input ranges**, where defects are more likely to occur.

---

## 🎯 Purpose of Boundary Testing

Boundary testing helps ensure that the system:

- Correctly accepts **valid boundary values**
- Properly rejects **invalid values outside defined limits**
- Enforces business rules and data validation consistently
- Handles edge cases without unexpected behavior

---

## 🧪 Projects Covered

### 🚗 Urban Routes – Web Application

Boundary values were analyzed for:

#### ⏰ Time-Based Pricing (Shared Car / Taxi)

The system behavior (travel cost and duration) was validated across time boundaries where pricing rules change:

- 18:01 – 22:00  
- 22:01 – 00:00  
- 00:01 – 08:00  
- 08:01 – 12:00  
- 12:01 – 18:00  

These tests ensured that:
- Pricing logic switches correctly at boundary times
- No gaps or overlaps exist between time ranges
- Costs and durations update according to business rules

---

#### 💳 Payment Method Form – Input Validation

Boundary values were tested for the **“Add Payment Method”** form to validate frontend input rules:

**Card Number field**
- Exact boundary: 12 digits (valid)
- Lower boundary: 11 digits (invalid)
- Upper boundary: 13 digits (invalid)
- Non-numeric characters (invalid)

**Security Code field**
- Exact boundary: 2 digits (valid)
- Lower boundary: 1 digit (invalid)
- Upper boundary: 3 digits (invalid)
- Non-numeric characters (invalid)

Additional validation:
- The **“Add”** button remains disabled when one or both fields are empty
- The button is enabled only when both fields contain valid boundary values

---

### 🛒 Urban Grocers – API

Boundary Value Analysis was applied to API inputs when adding products to a kit:

#### 📦 Validated Boundaries

- Kit ID (existing vs non-existing)
- Product ID (valid, invalid, non-existing)
- `quantity` field limits
- Structure and length of the `productsList` array
- Maximum limit of **30 unique products per kit**

#### 🚫 Boundary Enforcement

- Requests exceeding 30 unique products return:
  ```json
  {
    "message": "No mas de 30 artículos por conjunto"
  }
- Invalid boundary inputs correctly return 400 Bad Request or 404 Not Found

---

## 🛠 Tools Used

- Manual testing (Web UI)
- Postman (API requests)
- Google Sheets (test design and tracking)
- Jira (defect reporting)

---

## ✅ Key QA Focus

- Validation of edge cases
- Enforcement of business rules
- Detection of defects at boundary conditions
- Clear separation between valid and invalid input behavior

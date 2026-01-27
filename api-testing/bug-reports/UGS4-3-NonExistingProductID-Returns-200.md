# Bug Report - USGS4-3: Non-existing Product ID Returns 200 OK

### **Environment:**

- Postman
- JSON REST API
- Base URL: *URL*
- Headers: Content-Type: application/json

---

### Steps to Reproduce

1. Send POST request to URL + /api/v1/kits/:id/products
2. Use body with a non-existing product ID, for example:
   ```json
   {
   "productsList": [
    { "id": 99999,
      "quantity": 1
    }
   ]
   }
   ```
3. Observe reponse
 
 ---

 ### **Expected Result**

 The API should return:
 - **HTTP status code:** `404 Not Found`
 - A JSON error body indicanting product not found 
   Example:
   ```json
   {
   "message": "Product not found"
   }
   ```

---

### **Actual Result**
The API returns:
- HTTP status code: 200 OK
- Successful response, allowing a product that should not exist to be added
This indicates incorrect validation of product IDs.

---

### Severity
High

### Priority
Medium

---

## Notes

This behavior violates the expected API contract for invalid identifiers and could lead to data inconsistency or downstream errors if products that do not exist are accepted.

---

## Screenshot Evidence

### Request with Non-existing Product ID
![Request showing invalid product ID](./screenshots/UGS4-3_request_invalid_product.png)

### Incorrect API Response (Bug)
![API returns 200 OK instead of 404](./screenshots/UGS4-3_response_200_ok.png)


   
   

# Postman Collections – Urban Grocers API

This folder contains a Postman collection used to test the **Urban Grocers API**, focusing on adding products to shopping kits.

## Scope
The collection covers:
- Positive scenarios for adding existing products to existing kits
- Negative scenarios validating backend error handling
- Boundary value analysis and equivalence classes
- Validation of HTTP status codes and JSON responses

## Validated Scenarios
- Adding products with valid kit and product IDs (200 OK)
- Adding products with non-existing product IDs (400 Bad Request)
- Adding products to non-existing kits (404 Not Found)
- Invalid request body structure (400 Bad Request)
- Exceeding the limit of 30 unique products per kit (400 Bad Request)

## Tools
- Postman
- JSON-based REST API

All detected issues were reported and tracked in Jira.


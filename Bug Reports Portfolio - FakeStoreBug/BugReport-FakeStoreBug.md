# Bug Reports Portfolio – FakeStore

This document contains professionally structured bug reports identified during testing of the FakeStore demo eCommerce API and UI behaviors. These defects focus on API responses, data handling, UI behavior, and validation consistency.

---

## 1. GET /products returns inconsistent response time

Module: Products API
Severity: Medium

Steps to Reproduce:

1. Send multiple GET /products requests.
2. Observe response time.

Expected Result:
Response time should remain consistent under normal load.

Actual Result:
Response time fluctuates significantly without traffic simulation.

---

## 2. GET product by invalid ID returns 200 instead of error

Module: Product Details API
Severity: High

Steps:

1. Call GET /products/9999.

Expected Result:
API should return 404 or meaningful error.

Actual Result:
API returns 200 with empty or unexpected response.

---

## 3. POST /products accepts empty title

Module: Product Creation API
Severity: High

Steps:

1. Call POST /products with empty "title".

Expected Result:
Validation error should be returned.

Actual Result:
API accepts empty value and creates product.

---

## 4. POST /products accepts negative price

Module: Product Creation API
Severity: Critical

Steps:

1. Submit product with negative price.

Expected Result:
API should reject negative values.

Actual Result:
Product created successfully with negative price.

---

## 5. PUT /products updates product without verifying ID existence

Module: Product Update API
Severity: High

Steps:

1. Call PUT /products/9999.

Expected Result:
API should return error for non-existing product.

Actual Result:
API returns successful update response.

---

## 6. DELETE /products returns success for already deleted product

Module: Product Deletion API
Severity: Medium

Steps:

1. DELETE a product.
2. DELETE the same ID again.

Expected Result:
Second delete should return error.

Actual Result:
Both calls return successful response.

---

## 7. Product category field accepts random text

Module: Product Validation
Severity: Medium

Steps:

1. Create product with invalid category name.

Expected Result:
API should restrict categories to known values.

Actual Result:
Random category is accepted.

---

## 8. GET /categories returns duplicate values

Module: Categories API
Severity: Low

Steps:

1. Call GET /products/categories.

Expected Result:
Each category value should be unique.

Actual Result:
Duplicate category values appear in list.

---

## 9. Cart API allows adding product with zero quantity

Module: Cart API
Severity: High

Steps:

1. POST cart with product quantity set to zero.

Expected Result:
API should reject zero or negative quantities.

Actual Result:
Request succeeds with zero quantity.

---

## 10. Cart API allows negative quantity in cart

Module: Cart API
Severity: Critical

Steps:

1. POST cart with negative quantity.

Expected Result:
API should reject negative quantity.

Actual Result:
Cart created successfully.

---

## 11. User API accepts password without minimum length

Module: User Registration API
Severity: High

Steps:

1. Create user with short password.

Expected Result:
Password should meet minimum security requirements.

Actual Result:
User created with weak password.

---

## 12. User API allows duplicate email registration

Module: User Registration
Severity: High

Steps:

1. Register two users with same email.

Expected Result:
Second registration should be blocked.

Actual Result:
Both users created successfully.

---

## 13. Login API returns generic error for all failure cases

Module: Authentication API
Severity: Medium

Steps:

1. Attempt login with invalid credentials.

Expected Result:
Clear message specifying invalid username/password.

Actual Result:
Generic error returned.

---

## 14. Invalid token still allows access to protected endpoints

Module: Authentication / Security
Severity: Critical

Steps:

1. Access protected endpoint using invalid token.

Expected Result:
Request should be denied.

Actual Result:
Request processed successfully.

---

## 15. GET /carts returns carts for all users

Module: Authorization
Severity: High

Steps:

1. Call GET /carts without user filtering.

Expected Result:
API should restrict carts by user.

Actual Result:
All carts returned.

---

## 16. Product image URL allows broken external links

Module: Product Media Validation
Severity: Low

Steps:

1. Create product with invalid image URL.

Expected Result:
API should validate image URL.

Actual Result:
Invalid URLs accepted.

---

## 17. Rating object missing validation

Module: Product Ratings
Severity: Medium

Steps:

1. Submit invalid rating structure.

Expected Result:
API should enforce rating schema.

Actual Result:
Invalid rating object accepted.

---

## 18. GET /products limit parameter ignored

Module: Product Listing API
Severity: Medium

Steps:

1. Call GET /products?limit=5.

Expected Result:
Only 5 products returned.

Actual Result:
All products returned regardless of limit.

---

## 19. Price rounding inconsistency in product list

Module: Pricing Display
Severity: Low

Steps:

1. Fetch products list.

Expected Result:
Prices should follow consistent decimal precision.

Actual Result:
Some prices show inconsistent decimal formatting.

---

## 20. DELETE /users allows deletion without authentication

Module: User Management / Security
Severity: Critical

Steps:

1. Call DELETE /users/{id} without token.

Expected Result:
Unauthorized access should be blocked.

Actual Result:
User deleted successfully without authentication.

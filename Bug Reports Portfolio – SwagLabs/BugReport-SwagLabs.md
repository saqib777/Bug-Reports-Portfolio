# Bug Reports Portfolio – SwagLabs (SauceDemo)

This document contains a structured set of bug reports identified during testing of the SwagLabs (saucedemo) demo application. These defects focus on login validation, cart behavior, checkout workflow, UI consistency, and data handling.

---

## 1. Login allows empty username and password submission

Module: Login Page
Severity: High

Steps:

1. Open SwagLabs login page.
2. Leave both fields empty.
3. Click Login.

Expected Result:
User should receive a validation message indicating required fields.

Actual Result:
Generic error displayed without specifying missing fields.

---

## 2. Locked-out user login error message is unclear

Module: Login Page
Severity: Medium

Steps:

1. Enter locked_out_user credentials.
2. Click Login.

Expected Result:
Clear message explaining the user is locked out.

Actual Result:
Message does not explicitly mention locked account.

---

## 3. Inventory page loads slowly for standard users

Module: Inventory
Severity: Low

Steps:

1. Login as standard_user.
2. Observe page load time.

Expected Result:
Page loads within acceptable limits.

Actual Result:
Delayed load observed intermittently.

---

## 4. Add to cart button does not update cart count instantly

Module: Cart
Severity: Medium

Steps:

1. Add any product to cart.
2. Observe cart icon.

Expected Result:
Count should update immediately.

Actual Result:
Count updates only after page interaction.

---

## 5. Removing an item from cart does not refresh total price

Module: Cart Summary
Severity: High

Steps:

1. Add multiple items.
2. Remove one item.

Expected Result:
Total price recalculates correctly.

Actual Result:
Price remains unchanged until refresh.

---

## 6. Checkout form accepts numeric characters in First Name

Module: Checkout Step One
Severity: Medium

Steps:

1. Enter numbers in First Name.
2. Submit.

Expected Result:
Field should restrict non-alphabetic values.

Actual Result:
Numeric values accepted.

---

## 7. ZIP code field accepts special characters

Module: Checkout Step One
Severity: Medium

Steps:

1. Enter special characters in ZIP field.

Expected Result:
Only numeric input allowed.

Actual Result:
Special characters accepted.

---

## 8. Checkout allows progressing with missing Last Name

Module: Checkout Step One
Severity: High

Steps:

1. Leave Last Name empty.
2. Continue.

Expected Result:
System should block submission.

Actual Result:
Checkout proceeds to next step.

---

## 9. Item quantity not displayed in checkout overview

Module: Checkout Step Two
Severity: Low

Steps:

1. Add multiple items.
2. Proceed to overview.

Expected Result:
Quantity should be visible.

Actual Result:
Only item name and price shown.

---

## 10. Total price does not include tax until final confirmation

Module: Checkout
Severity: Medium

Steps:

1. Reach overview page.

Expected Result:
Price should show tax breakdown.

Actual Result:
Tax appears only after final confirmation.

---

## 11. Inventory sorting (Price Low to High) is inconsistent

Module: Sorting
Severity: Medium

Steps:

1. Sort inventory by Price Low to High.

Expected Result:
Prices should be in ascending order.

Actual Result:
Order appears incorrect.

---

## 12. Product images fail to load intermittently

Module: Inventory
Severity: Low

Steps:

1. Scroll through product list.

Expected Result:
All product images should load properly.

Actual Result:
Some images show broken placeholders.

---

## 13. Back button from product details returns to top of inventory list

Module: Product Details
Severity: Medium

Steps:

1. Scroll down inventory.
2. Open a product.
3. Click Back.

Expected Result:
Return to same scroll position.

Actual Result:
Page resets to top.

---

## 14. Cart icon still visible after logout

Module: Session Management
Severity: High

Steps:

1. Add item to cart.
2. Logout.
3. Observe UI.

Expected Result:
Cart icon should reset.

Actual Result:
Cart icon displays previous count.

---

## 15. Checkout complete page allows refreshing without warning

Module: Checkout Completion
Severity: Low

Steps:

1. Finish checkout.
2. Refresh page.

Expected Result:
System should warn or redirect.

Actual Result:
Page reloads with broken layout.

---

## 16. Side menu overlaps page content on mobile

Module: Responsive UI
Severity: Medium

Steps:

1. Open mobile layout.
2. Click hamburger menu.

Expected Result:
Menu should slide without obstructing text.

Actual Result:
Menu overlaps content.

---

## 17. Performance issue when filtering inventory repeatedly

Module: Inventory Filters
Severity: Low

Steps:

1. Change filter values repeatedly.

Expected Result:
Smooth transitions.

Actual Result:
Lag observed.

---

## 18. Checkout form resets if user navigates backward

Module: Checkout Step One
Severity: Medium

Steps:

1. Fill checkout form.
2. Navigate back.

Expected Result:
Form should retain values.

Actual Result:
All fields reset.

---

## 19. Inventory badge count not matching actual items displayed

Module: Inventory
Severity: Medium

Steps:

1. Observe item count header.

Expected Result:
Displayed item count should match actual items.

Actual Result:
Numbers mismatch.

---

## 20. Error message placement overlaps form fields

Module: Checkout Step One
Severity: Low

Steps:

1. Trigger validation error.

Expected Result:
Message should display cleanly.

Actual Result:
Message overlaps fields causing readability issues.

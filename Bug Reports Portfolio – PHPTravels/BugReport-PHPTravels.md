# Bug Reports Portfolio – PHPTravels

This document contains a structured set of bug reports identified during testing of the PHPTravels demo application. These defects focus on booking flows, authentication, form validation, UI behavior, and data consistency.

---

## 1. Login allows submission with empty email and password

Module: Authentication
Severity: High

Steps to Reproduce:

1. Open PHPTravels login page.
2. Leave Email and Password empty.
3. Click Login.

Expected Result:
System should display field-level validation messages.

Actual Result:
Form submits and shows a generic error.

---

## 2. Invalid email format accepted during registration

Module: Registration
Severity: Medium

Steps:

1. Enter invalid email format during signup.
2. Submit the form.

Expected Result:
System should block invalid email formats.

Actual Result:
Registration proceeds without validation.

---

## 3. Password field does not enforce minimum length

Module: Registration
Severity: High

Steps:

1. Enter a very short password.
2. Submit the form.

Expected Result:
System should enforce minimum password length.

Actual Result:
Account created with weak password.

---

## 4. Search results show hotels outside selected location

Module: Hotel Search
Severity: Medium

Steps:

1. Select a city.
2. Search for hotels.

Expected Result:
Only hotels from selected city should appear.

Actual Result:
Results include hotels from other cities.

---

## 5. Date picker allows check-out date earlier than check-in

Module: Booking Date Selection
Severity: High

Steps:

1. Select a future check-in date.
2. Select a check-out date earlier than check-in.

Expected Result:
System should block invalid date sequence.

Actual Result:
Booking search proceeds.

---

## 6. Booking search button remains enabled with empty fields

Module: Booking Search
Severity: Medium

Steps:

1. Do not fill any booking fields.
2. Click Search.

Expected Result:
Search button should be disabled.

Actual Result:
Search is executed with empty criteria.

---

## 7. Price filter does not update results correctly

Module: Filters
Severity: Medium

Steps:

1. Apply minimum and maximum price filter.

Expected Result:
Only products within selected price range should appear.

Actual Result:
Results do not respect filter range.

---

## 8. Currency selection does not update prices dynamically

Module: Currency Converter
Severity: Medium

Steps:

1. Change currency from USD to another.

Expected Result:
Prices should update immediately.

Actual Result:
Prices remain unchanged until refresh.

---

## 9. Guest count allows zero adults

Module: Booking Form
Severity: High

Steps:

1. Set adult count to zero.
2. Attempt search.

Expected Result:
System should enforce minimum one adult.

Actual Result:
Search proceeds with zero adults.

---

## 10. Room selection does not reflect in final booking price

Module: Booking Summary
Severity: High

Steps:

1. Select a premium room.
2. Continue booking.

Expected Result:
Price should reflect selected room type.

Actual Result:
Basic room price shown in summary.

---

## 11. Payment page loads without total amount displayed

Module: Payment
Severity: Critical

Steps:

1. Complete booking till payment page.

Expected Result:
Total payable amount should be visible.

Actual Result:
Payment page loads without showing total.

---

## 12. Card number field accepts alphabetic characters

Module: Payment Validation
Severity: High

Steps:

1. Enter letters in card number field.

Expected Result:
Field should accept digits only.

Actual Result:
Alphabets accepted.

---

## 13. CVV field allows more than 3 digits

Module: Payment Validation
Severity: Medium

Steps:

1. Enter more than 3 digits in CVV.

Expected Result:
Field should restrict input length.

Actual Result:
Field accepts more than allowed digits.

---

## 14. Booking confirmation page does not show booking reference ID

Module: Booking Confirmation
Severity: High

Steps:

1. Complete booking.

Expected Result:
Unique booking reference ID should be displayed.

Actual Result:
Confirmation page loads without reference ID.

---

## 15. Email confirmation not received after booking

Module: Notifications
Severity: Medium

Steps:

1. Complete a booking with valid email.

Expected Result:
Confirmation email should be sent.

Actual Result:
No confirmation email received.

---

## 16. Logout does not immediately redirect to homepage

Module: Session Management
Severity: Low

Steps:

1. Click Logout.

Expected Result:
User should be redirected to homepage.

Actual Result:
User stays on same page until refresh.

---

## 17. Browser back button after logout restores session

Module: Security
Severity: Critical

Steps:

1. Login.
2. Logout.
3. Press browser back button.

Expected Result:
User session should not be restored.

Actual Result:
User is logged in again.

---

## 18. Profile update allows empty mandatory fields

Module: User Profile
Severity: High

Steps:

1. Clear required profile fields.
2. Save changes.

Expected Result:
System should block empty required fields.

Actual Result:
Profile updated with missing data.

---

## 19. Mobile view booking form overlaps UI elements

Module: Responsive UI
Severity: Medium

Steps:

1. Open booking form on mobile resolution.

Expected Result:
UI elements should align properly.

Actual Result:
Text fields and buttons overlap.

---

## 20. Search results page shows inconsistent sorting by price

Module: Sorting
Severity: Medium

Steps:

1. Sort results by price low to high.

Expected Result:
Results should be sorted in ascending order.

Actual Result:
Sorting appears random.

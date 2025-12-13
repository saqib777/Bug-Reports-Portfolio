# Bug Reports Portfolio – Parasoft Demo Application

This document contains a set of structured bug reports identified during testing of the Parasoft demo application. The focus is on form validation, workflow consistency, UI behavior, data handling, and basic security-related scenarios.

---

## 1. Registration form allows submission with empty mandatory fields

Module: Registration
Severity: High

Steps to Reproduce:

1. Open Parasoft registration page.
2. Leave mandatory fields empty.
3. Click Submit.

Expected Result:
System should block submission and show field-level validation messages.

Actual Result:
Form submits and navigates forward without validation.

---

## 2. Email field accepts invalid email formats

Module: Registration
Severity: Medium

Steps:

1. Enter invalid email format (e.g., abc@).
2. Submit the form.

Expected Result:
Email field should validate correct format.

Actual Result:
Invalid email accepted.

---

## 3. Password field does not enforce minimum strength rules

Module: Registration
Severity: High

Steps:

1. Enter a very short or simple password.
2. Submit.

Expected Result:
Password strength rules should be enforced.

Actual Result:
Weak password accepted.

---

## 4. Confirm password mismatch not validated

Module: Registration
Severity: High

Steps:

1. Enter different values in Password and Confirm Password.
2. Submit.

Expected Result:
System should block submission and show mismatch error.

Actual Result:
Account created successfully.

---

## 5. Login error message is generic for all failure scenarios

Module: Login
Severity: Medium

Steps:

1. Enter incorrect credentials.
2. Click Login.

Expected Result:
Error message should clearly indicate invalid credentials.

Actual Result:
Generic error displayed.

---

## 6. Forgot password link redirects to incorrect page

Module: Authentication
Severity: Medium

Steps:

1. Click Forgot Password.

Expected Result:
User should be redirected to password recovery page.

Actual Result:
Incorrect or blank page loaded.

---

## 7. User session remains active after logout using browser back button

Module: Session Management
Severity: Critical

Steps:

1. Login to application.
2. Click Logout.
3. Press browser Back button.

Expected Result:
Session should not be restored.

Actual Result:
User session is restored.

---

## 8. Dashboard loads without access control checks

Module: Authorization
Severity: Critical

Steps:

1. Access dashboard URL directly without logging in.

Expected Result:
User should be redirected to login page.

Actual Result:
Dashboard loads successfully.

---

## 9. Form error messages overlap input fields

Module: UI Validation
Severity: Low

Steps:

1. Trigger validation errors on form.

Expected Result:
Error messages should display clearly without overlapping fields.

Actual Result:
Messages overlap input fields.

---

## 10. Dropdown values not loading consistently

Module: UI Components
Severity: Medium

Steps:

1. Open page containing dropdown.

Expected Result:
Dropdown values should load consistently.

Actual Result:
Dropdown appears empty intermittently.

---

## 11. Search functionality returns results unrelated to keyword

Module: Search
Severity: Medium

Steps:

1. Enter specific keyword.
2. Execute search.

Expected Result:
Results should match keyword.

Actual Result:
Unrelated results displayed.

---

## 12. Pagination controls do not navigate correctly

Module: Pagination
Severity: Medium

Steps:

1. Navigate to paginated list.
2. Click Next page.

Expected Result:
Next set of results should load.

Actual Result:
Same page reloads.

---

## 13. Sorting option does not apply selected order

Module: Sorting
Severity: Medium

Steps:

1. Select sorting option (e.g., Date).

Expected Result:
Results sorted accordingly.

Actual Result:
Sorting not applied.

---

## 14. Table data alignment breaks on smaller screens

Module: Responsive UI
Severity: Low

Steps:

1. Resize browser window.

Expected Result:
Table should remain readable.

Actual Result:
Columns overlap or break layout.

---

## 15. File upload accepts unsupported file formats

Module: File Upload
Severity: High

Steps:

1. Upload unsupported file type.

Expected Result:
System should reject invalid file types.

Actual Result:
File accepted without validation.

---

## 16. Upload progress indicator does not reflect actual progress

Module: File Upload
Severity: Low

Steps:

1. Upload a large file.

Expected Result:
Progress bar should update smoothly.

Actual Result:
Progress jumps or freezes.

---

## 17. Confirmation message missing after successful form submission

Module: User Feedback
Severity: Medium

Steps:

1. Submit valid form.

Expected Result:
Success confirmation should be shown.

Actual Result:
Page reloads without message.

---

## 18. Error page displays stack trace to user

Module: Error Handling
Severity: Critical

Steps:

1. Trigger application error.

Expected Result:
User-friendly error page without technical details.

Actual Result:
Stack trace visible on UI.

---

## 19. Browser refresh causes duplicate form submission

Module: Form Handling
Severity: High

Steps:

1. Submit a form.
2. Refresh browser.

Expected Result:
System should prevent duplicate submission.

Actual Result:
Form submitted again.

---

## 20. Footer links redirect to incorrect destinations

Module: Navigation
Severity: Low

Steps:

1. Click footer links.

Expected Result:
Links should redirect to correct pages.

Actual Result:
Incorrect or broken pages opened.

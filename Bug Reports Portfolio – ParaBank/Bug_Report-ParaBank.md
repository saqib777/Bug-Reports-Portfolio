# Bug Reports Portfolio – ParaBank

This document contains a set of detailed bug reports identified during testing of the ParaBank demo application. Each report follows a clear, structured format suitable for QA documentation and SDET portfolios.

---

## 1. Login accepts blank username and password

Module: Login Page
Severity: High
Environment: ParaBank Demo

Steps to Reproduce:

1. Open ParaBank login page.
2. Leave username and password fields empty.
3. Click the Login button.

Expected Result:
System should display a validation error stating that credentials are required.

Actual Result:
System shows a generic login error without specifying missing fields.

---

## 2. Login error message is not descriptive

Module: Login Page
Severity: Medium

Steps:

1. Enter incorrect username and password.
2. Click Login.

Expected Result:
Message should specify that credentials are invalid.

Actual Result:
Shows a vague error without specific details.

---

## 3. Register link sometimes redirects to a blank page

Module: Registration
Severity: High

Steps:

1. Click the Register link in the login area.
2. Observe page load.

Expected Result:
Registration page loads consistently.

Actual Result:
Occasional blank white screen.

---

## 4. Registration form allows numeric characters in first name and last name

Module: Registration
Severity: Medium

Steps:

1. Open registration page.
2. Enter numbers in First Name and Last Name.
3. Submit.

Expected Result:
Validation message should restrict non-alphabetic characters.

Actual Result:
Form accepts numeric values.

---

## 5. Phone number field accepts letters

Module: Registration
Severity: Medium

Steps:

1. Open registration page.
2. Enter alphabetic characters in the Phone field.

Expected Result:
Phone field should accept digits only.

Actual Result:
Form allows letters without error.

---

## 6. Password and Confirm Password mismatch not validated

Module: Registration
Severity: High

Steps:

1. Enter a password.
2. Enter a different value in Confirm Password.
3. Submit form.

Expected Result:
System should block submission.

Actual Result:
Account is created without matching passwords.

---

## 7. Fund Transfer page throws error when amount is left empty

Module: Transfer Funds
Severity: High

Steps:

1. Go to Transfer Funds.
2. Leave Amount empty.
3. Click Transfer.

Expected Result:
Validation error for missing amount.

Actual Result:
Application error message displayed.

---

## 8. Transfer succeeds with negative amount

Module: Transfer Funds
Severity: Critical

Steps:

1. Enter a negative number in Amount field.
2. Click Transfer.

Expected Result:
System should reject negative values.

Actual Result:
Transfer completes successfully.

---

## 9. Transfer funds confirmation page shows wrong source account

Module: Transfer Funds
Severity: Medium

Steps:

1. Select a source account.
2. Enter amount.
3. Submit.

Expected Result:
Confirmation page should display selected account.

Actual Result:
Displays a different account ID.

---

## 10. Account Overview page shows inconsistent balance format

Module: Account Overview
Severity: Low

Steps:

1. Login to ParaBank.
2. Navigate to Accounts Overview.

Expected Result:
All balances should follow the same decimal format.

Actual Result:
Some balances show no decimals.

---

## 11. Account activity not updating after a fund transfer

Module: Account Activity
Severity: Medium

Steps:

1. Transfer funds.
2. Open Account Activity.

Expected Result:
Latest transaction should appear.

Actual Result:
Transaction does not appear even after refresh.

---

## 12. Bill Pay accepts alphanumeric characters in amount

Module: Bill Pay
Severity: High

Steps:

1. Open Bill Pay.
2. Enter letters in Amount.

Expected Result:
Field must allow only numeric values.

Actual Result:
Accepts alphanumeric values.

---

## 13. Bill Pay form allows past due date

Module: Bill Pay
Severity: Medium

Steps:

1. Enter a bill pay date older than current date.
2. Submit form.

Expected Result:
System should warn about invalid date.

Actual Result:
Payment proceeds without warning.

---

## 14. New Account creation fails silently

Module: Open New Account
Severity: High

Steps:

1. Navigate to Open New Account.
2. Select account type.
3. Submit.

Expected Result:
Success or failure message displayed.

Actual Result:
Page reloads with no message.

---

## 15. New Account creation dropdown values not loading consistently

Module: Open New Account
Severity: Medium

Steps:

1. Navigate to Open New Account.

Expected Result:
Dropdown should always load valid account types.

Actual Result:
Occasionally loads empty dropdown.

---

## 16. Logout does not invalidate session fully

Module: Authentication
Severity: High

Steps:

1. Login.
2. Click Logout.
3. Press Back in browser.

Expected Result:
Session should not be accessible.

Actual Result:
User session is restored.

---

## 17. Forgot login info link redirects to wrong URL

Module: Authentication
Severity: Medium

Steps:

1. Click Forgot login link.

Expected Result:
Leads to recovery page.

Actual Result:
Redirects to incorrect or blank page.

---

## 18. Invalid account number in Account Details throws server error

Module: Account Details
Severity: Critical

Steps:

1. Access an invalid account ID via URL.

Expected Result:
User-friendly error message.

Actual Result:
Returns server error.

---

## 19. Contact page form allows empty submission

Module: Contact Page
Severity: Medium

Steps:

1. Open Contact page.
2. Click Send without filling any fields.

Expected Result:
Field-level validation.

Actual Result:
Form submits with no checks.

---

## 20. UI overlap in mobile view for header menu

Module: Responsive UI
Severity: Low

Steps:

1. Resize browser to mobile width.
2. Observe header navigation.

Expected Result:
Menu should collapse properly.

Actual Result:
Elements overlap visually.

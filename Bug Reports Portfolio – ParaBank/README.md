# Bug Reports Portfolio – ParaBank

This section of the Bug Reports Portfolio contains a structured collection of defects identified during exploratory and functional testing of the ParaBank demo application. The goal of this documentation is to present clear, professional bug reporting aligned with QA and SDET expectations.

---

## Overview

ParaBank is a commonly used demo banking application that includes modules such as authentication, account management, fund transfers, bill payments, and customer information. This makes it an ideal target for practicing defect identification across both functional and non-functional areas.

This folder contains 20 detailed bug reports covering:

* Login and authentication
* Registration
* Transfer funds
* Bill payment
* Account overview and activity
* UI consistency and responsiveness
* Form validation and data handling

Each report follows a consistent, readable structure to demonstrate clarity and proper testing methodology.

---

## What This Folder Includes

```
Bug Reports Portfolio – ParaBank/
│
├── Bug_Reports_ParaBank.md       # 20 detailed bug reports
├── Screenshots/                  # Optional evidence folder (if added)
└── Templates/                    # Bug report templates (if required)
```

---

## Scope of Testing

The ParaBank bug reports focus on the following areas:

### Functional Testing

* Incorrect validation handling
* Workflow failures
* Incorrect error messages
* Data inconsistencies between pages

### Usability and UI Testing

* Confusing behavior during form submissions
* Missing or unclear messages
* Navigation issues

### Data Validation

* Fields accepting invalid characters
* Missing required-field checks
* Incorrect handling of edge cases such as negative or empty values

### Security and Session Behavior

* Session persistence after logout
* Accessing invalid account IDs via URL

---

## Highlights of Identified Issues

A few examples of the types of bugs documented:

* Negative fund transfers being processed successfully
* Password and confirm-password mismatch allowed during registration
* Session not invalidated after logout
* Account dropdown values not loading consistently
* Blank or incorrect redirects for forgotten-login and registration flows

These reflect realistic issues seen in financial or transactional systems.

---

## Purpose of This Portfolio Section

This set of bug reports demonstrates:

* Ability to identify defects across modules
* Clear reproduction steps and expected vs actual behavior
* Understanding of severity levels
* Professional QA documentation style
* Coverage of multiple types of testing

This is suitable for interviews where candidates are asked to:

* Share example bug reports
* Describe actual issues found in a system
* Explain how they think about severity and impact

---

## Future Enhancements

* Add screenshot evidence for selected defects
* Expand to include more complex scenarios such as multi-account transfers
* Add CSV or Excel versions of the bug reports
* Include severity/priority matrix files specific to ParaBank

---

## About the Author

Created as part of a structured QA/SDET learning path by Mohammed Saqib. This module contributes to a comprehensive bug-reporting portfolio spanning multiple demo applications.

# SauceDemo Manual QA Testing Project

## Overview

This repository contains an independent manual QA testing project performed on the SauceDemo web application.

The project demonstrates practical manual testing skills including test planning, test case design, functional testing, negative testing, exploratory testing, defect reporting, and test result documentation.

> **Disclaimer:** This is an independent educational portfolio project and is not affiliated with or performed on behalf of Sauce Labs.

---

## Test Environment

- **Device:** iPhone 12
- **Operating System:** iOS 26.6.2
- **Browser:** Google
- **Application:** SauceDemo
- **Testing Type:** Manual

---

## Testing Scope

The primary testing covered:

- Authentication
- Product inventory
- Product details
- Product sorting
- Shopping cart
- Checkout
- Form validation
- Order completion

Additional exploratory testing covered:

- All Items
- Dynamic Catalog
- Lazy Load
- Spinner
- Slider
- About
- Logout
- Reset App State

---

## Test Results

### Structured Testing

**20 test cases executed**

| Result | Count |
|---|---:|
| PASS | 20 |
| FAIL | 0 |
| BLOCKED | 0 |
| NOT EXECUTED | 0 |
| **Total** | **20** |

Two confirmed defects were identified during the overall testing effort.

### Confirmed Defects

**Issue #1 — Mobile error notification extends outside viewport**

Observed during invalid login testing. The error notification extended outside the visible mobile viewport.

**Issue #2 — Reset App State leaves product controls in incorrect state**

After resetting the application state, the cart was cleared but a product control remained displayed as "Remove" until navigating away and returning.

Both defects are documented in GitHub Issues with reproduction steps, expected behavior, actual behavior, severity, priority, and supporting evidence.

---

## Documentation

### Test Plan

Defines the testing objectives, scope, testing approach, severity definitions, test result statuses, and overall workflow.

➡️ [View Test Plan](Test-plan/test-plan.md)

### Test Cases

Contains 20 structured manual test cases covering authentication, inventory, sorting, cart functionality, and checkout.

➡️ [View Test Cases](Test-cases/test-cases.md)

### Exploratory Testing

Documents exploratory testing of the application's navigation menu and Dynamic Catalog functionality.

➡️ [View Exploratory Testing](exploratory-testing/exploratory-menu-testing.md)

### Test Execution Summary

Provides the overall execution results, confirmed defects, additional observations, and testing limitations.

➡️ [View Test Execution Summary](test-execution-summary.md)

---

## Testing Methods Demonstrated

- Functional Testing
- Negative Testing
- Smoke Testing
- Regression Testing
- Exploratory Testing
- UI Testing
- Usability Observation
- Defect Reporting
- Test Case Design
- Test Execution
- Retesting

---

## Tools

- GitHub
- GitHub Issues
- Excel / Google Sheets
- Manual Testing

---

## Project Workflow

The testing process followed a basic QA workflow:

**Plan → Design Test Cases → Execute Tests → Identify Defects → Report Defects → Retest → Regression → Document Results**

---

## Portfolio Purpose

This project was created to demonstrate practical manual QA testing skills through hands-on testing of a publicly accessible web application.

It is intended as a portfolio project for QA and software testing applications.

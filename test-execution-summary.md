# Test Execution Summary — SauceDemo

## Test Information

**Application:** SauceDemo  
**Test Type:** Manual QA Testing  
**Device:** iPhone 12  
**Operating System:** iOS 26.6.2  
**Browser:** Google  
**Tester:** Independent QA Portfolio Project

---

## Testing Scope

Testing covered the primary user workflows of the SauceDemo application, including:

- User authentication
- Product inventory
- Product sorting
- Product details
- Shopping cart
- Checkout
- Form validation
- Order completion

Additional exploratory testing was performed on the application's navigation menu and Dynamic Catalog features.

---

## Test Execution Results

| Category | Test Cases | Result |
|---|---:|---|
| Authentication | TC-001 – TC-005 | 5 PASS |
| Product Inventory | TC-006 – TC-007 | 2 PASS |
| Product Sorting | TC-008 – TC-011 | 4 PASS |
| Shopping Cart | TC-012 – TC-015 | 4 PASS |
| Checkout | TC-016 – TC-020 | 5 PASS |
| **Total** | **20** | **20 PASS** |

---

## Defects Identified

### Defect #1 — Mobile Error Notification Extends Outside Viewport

**Related Test Cases:** TC-002, TC-003

When an invalid username or password was entered, the resulting error notification extended outside the visible mobile viewport.

The issue was reproduced during testing and documented as GitHub Issue #1.

**Severity:** Low  
**Priority:** Medium

---

### Defect #2 — Reset App State Leaves Product Controls in Incorrect State

**Related Test:** Exploratory Testing — EXP-007

After using Reset App State, the cart was successfully emptied, but a product's control remained displayed as "Remove" instead of changing to "Add to cart."

Navigating away from the page and returning caused the control to display "Add to cart."

The behavior was reproducible and documented as GitHub Issue #2.

**Severity:** Medium  
**Priority:** Medium

---

## Additional Observations

### Session / Authentication Behavior

During checkout and cart testing, authentication errors occurred after periods of testing. After logging in again, the workflows could be completed successfully.

The exact session timeout behavior was not formally measured, so it was treated as an observation rather than a confirmed defect.

### Product Details Navigation

During product detail testing, an unexpected navigation error occurred once when using the back navigation control. The behavior could not be reproduced during subsequent attempts and was therefore not logged as a confirmed defect.

---

## Exploratory Testing

An exploratory testing session was performed on the application's navigation menu.

Areas tested included:

- All Items
- Dynamic Catalog — Lazy Load
- Dynamic Catalog — Spinner
- Dynamic Catalog — Slider
- About
- Logout
- Reset App State

The exploratory session resulted in one confirmed defect involving Reset App State and the product control state.

Detailed results are documented in the Exploratory Testing document.

---

## Overall Result

The primary SauceDemo workflows were successfully tested across 20 structured test cases.

Two confirmed defects were identified and documented during testing. Additional observations were recorded where unexpected behavior occurred but could not be reproduced sufficiently to classify as confirmed defects.

This project demonstrates manual QA practices including:

- Test planning
- Test case design
- Functional testing
- Negative testing
- Exploratory testing
- Defect identification
- Defect documentation
- Retesting
- Regression-oriented verification
- Test result documentation

---

## Testing Limitations

This was an independent manual QA portfolio project.

Testing was performed from a mobile environment and did not include:

- Automated testing
- Backend testing
- Database testing
- Load or performance testing
- Security penetration testing
- Source-code review

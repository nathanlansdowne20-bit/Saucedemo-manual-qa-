# Test Cases — SauceDemo

## Test Information

**Application:** SauceDemo  
**Test Type:** Manual Functional Testing  
**Device:** iPhone 12  
**Operating System:** iOS 26.6.2  
**Browser:** Google  
**Tester:** Independent QA Portfolio Project

---

## Authentication

### TC-001 — Login with Valid Credentials

**Priority:** High

**Preconditions:** User is on the SauceDemo login page.

**Test Data:**
- Username: `standard_user`
- Password: Valid SauceDemo password

**Steps:**
1. Enter a valid username.
2. Enter a valid password.
3. Tap the Login button.

**Expected Result:**  
User is successfully logged in and redirected to the Products page.

**Actual Result:**  
Successfully logged in and reached the Products page. No error messages or unusual behavior observed.

**Status:** PASS

---

### TC-002 — Login with Invalid Password

**Priority:** High

**Preconditions:** User is on the SauceDemo login page.

**Test Data:**
- Username: `standard_user`
- Password: Incorrect password

**Steps:**
1. Enter a valid username.
2. Enter an incorrect password.
3. Tap Login.

**Expected Result:**  
An appropriate error message is displayed and the user remains on the login page.

**Actual Result:**  
Error message displayed: "Epic sadface: Username and password do not match any user in this service." The error notification extended outside the visible viewport on the mobile screen.

**Status:** PASS

**Related Defect:** GitHub Issue #1

---

### TC-003 — Login with Invalid Username

**Priority:** High

**Preconditions:** User is on the SauceDemo login page.

**Test Data:**
- Username: Invalid username
- Password: Valid password

**Steps:**
1. Enter an invalid username.
2. Enter a valid password.
3. Tap Login.

**Expected Result:**  
An appropriate error message is displayed and the user remains on the login page.

**Actual Result:**  
Error message displayed: "Epic sadface: Username and password do not match any user in this service." The same mobile error notification layout issue observed in TC-002 was present.

**Status:** PASS

**Related Defect:** GitHub Issue #1

---

### TC-004 — Login with Blank Username

**Priority:** High

**Preconditions:** User is on the SauceDemo login page.

**Steps:**
1. Leave the username field blank.
2. Enter a valid password.
3. Tap Login.

**Expected Result:**  
An error message indicates that a username is required.

**Actual Result:**  
Error message displayed: "Epic sadface: Username is required." The notification fit within the visible screen area.

**Status:** PASS

---

### TC-005 — Login with Blank Password

**Priority:** High

**Preconditions:** User is on the SauceDemo login page.

**Steps:**
1. Enter a valid username.
2. Leave the password field blank.
3. Tap Login.

**Expected Result:**  
An error message indicates that a password is required.

**Actual Result:**  
Error message displayed: "Epic sadface: Password is required." The notification fit within the visible screen area.

**Status:** PASS

---

# Product Inventory

### TC-006 — Display Product Inventory

**Priority:** High

**Preconditions:** User is logged in.

**Steps:**
1. Navigate to the Products page.
2. Review the displayed products.

**Expected Result:**  
Products are displayed with appropriate images, names, prices, and Add to Cart controls.

**Actual Result:**  
Products displayed with images, names, prices, and Add to Cart controls. No confirmed defects were identified.

**Status:** PASS

**Notes:**  
The product layout contained a large amount of space between some product descriptions and the price/Add to Cart controls. This was observed but was not confirmed to be a defect.

---

### TC-007 — Open Product Details

**Priority:** High

**Preconditions:** User is logged in and on the Products page.

**Steps:**
1. Select a product.
2. Review the product details page.

**Expected Result:**  
The selected product's details page opens and displays the correct product name, image, description, price, and Add to Cart control.

**Actual Result:**  
Sauce Labs Backpack opened correctly. The product name, image, description, price, Add to Cart control, and back navigation were displayed correctly.

An unexpected navigation/error was observed once when using the back arrow, but the behavior could not be reproduced during subsequent testing.

**Status:** PASS

**Notes:**  
The unreproduced navigation issue was not logged as a defect.

---

# Product Sorting

### TC-008 — Sort Products A-Z

**Priority:** Medium

**Preconditions:** User is logged in and on the Products page.

**Steps:**
1. Open the sorting menu.
2. Select "Name (A to Z)."

**Expected Result:**  
Products are displayed in alphabetical order from A to Z.

**Actual Result:**  
Products were displayed in alphabetical order from A to Z. This was also the default sorting option.

**Status:** PASS

---

### TC-009 — Sort Products Z-A

**Priority:** Medium

**Preconditions:** User is logged in and on the Products page.

**Steps:**
1. Open the sorting menu.
2. Select "Name (Z to A)."

**Expected Result:**  
Products are displayed in reverse alphabetical order.

**Actual Result:**  
Products were displayed in reverse alphabetical order.

**Status:** PASS

---

### TC-010 — Sort Products by Price Low to High

**Priority:** Medium

**Preconditions:** User is logged in and on the Products page.

**Steps:**
1. Open the sorting menu.
2. Select "Price (low to high)."

**Expected Result:**  
Products are displayed from the lowest price to the highest price.

**Actual Result:**  
Product prices increased from the top of the list toward the bottom.

**Status:** PASS

---

### TC-011 — Sort Products by Price High to Low

**Priority:** Medium

**Preconditions:** User is logged in and on the Products page.

**Steps:**
1. Open the sorting menu.
2. Select "Price (high to low)."

**Expected Result:**  
Products are displayed from the highest price to the lowest price.

**Actual Result:**  
The highest-priced product appeared at the top and the lowest-priced product appeared at the bottom.

**Status:** PASS

---

# Shopping Cart

### TC-012 — Add One Product to Cart

**Priority:** High

**Preconditions:** User is logged in and on the Products page.

**Steps:**
1. Select Add to Cart for Sauce Labs Backpack.
2. Open the shopping cart.

**Expected Result:**  
The selected product is added to the cart and the cart indicator displays one item.

**Actual Result:**  
Sauce Labs Backpack was added successfully. The button changed from Add to Cart to Remove and the cart indicator displayed one item.

**Status:** PASS

---

### TC-013 — Add Multiple Products to Cart

**Priority:** High

**Preconditions:** User is logged in and on the Products page.

**Steps:**
1. Add one product to the cart.
2. Add two additional products.
3. Open the cart.

**Expected Result:**  
All selected products are added and the cart indicator reflects the correct number of items.

**Actual Result:**  
Three products were added successfully. The cart indicator displayed three items and the Add to Cart buttons changed to Remove.

**Status:** PASS

---

### TC-014 — Remove Product from Cart

**Priority:** High

**Preconditions:** User is logged in and has multiple products in the cart.

**Steps:**
1. Open the cart.
2. Remove a product.
3. Verify the cart contents.

**Expected Result:**  
The selected product is removed and the cart count decreases accordingly.

**Actual Result:**  
The selected product was removed successfully. The cart indicator decreased from three items to two. Additional product removal also worked correctly.

**Status:** PASS

**Notes:**  
An authentication error occurred during an earlier attempt to access the cart, but the behavior was not reproduced after logging back in and was not logged as a confirmed defect.

---

### TC-015 — Verify Cart Item Count

**Priority:** Medium

**Preconditions:** User is logged in and has products in the cart.

**Steps:**
1. Add or remove products.
2. Observe the cart indicator.
3. Open the cart and compare the displayed products with the cart count.

**Expected Result:**  
The cart indicator accurately reflects the number of products in the cart.

**Actual Result:**  
After removing products, the cart indicator displayed one item and the cart contained exactly one product.

**Status:** PASS

---

# Checkout

### TC-016 — Checkout with Valid Information

**Priority:** High

**Preconditions:** User is logged in and has a product in the cart.

**Test Data:**
- First Name: Valid
- Last Name: Valid
- Postal Code: Valid

**Steps:**
1. Open the cart.
2. Select Checkout.
3. Enter valid customer information.
4. Continue to the order overview.
5. Verify order information.
6. Select Finish.

**Expected Result:**  
The order overview displays the correct product and pricing information, and the order is successfully completed.

**Actual Result:**  
The order overview displayed the correct product, price, payment information, shipping information, item total, tax, and total. An initial attempt produced an authentication error, but after logging back in and repeating the checkout workflow, the order completed successfully and displayed the Checkout Complete confirmation.

**Status:** PASS

**Notes:**  
An apparent session/authentication interruption occurred during the first attempt. The exact session timeout behavior was not formally measured or confirmed.

---

### TC-017 — Checkout with Missing First Name

**Priority:** High

**Preconditions:** User is logged in and has a product in the cart.

**Steps:**
1. Begin checkout.
2. Leave the First Name field blank.
3. Enter a valid last name and postal code.
4. Continue.

**Expected Result:**  
The user is prevented from continuing and an error message indicates that the first name is required.

**Actual Result:**  
Error message displayed: "Error: first name required."

**Status:** PASS

---

### TC-018 — Checkout with Missing Postal Code

**Priority:** High

**Preconditions:** User is logged in and has a product in the cart.

**Steps:**
1. Begin checkout.
2. Enter a valid first and last name.
3. Leave the Postal Code field blank.
4. Continue.

**Expected Result:**  
The user is prevented from continuing and an error message indicates that a postal code is required.

**Actual Result:**  
"Postal code error" was displayed.

**Status:** PASS

---

### TC-019 — Cancel Checkout

**Priority:** Medium

**Preconditions:** User is logged in and has a product in the cart.

**Steps:**
1. Open the cart.
2. Select Checkout.
3. Select Cancel.

**Expected Result:**  
The user returns to the Products page and the cart contents remain available.

**Actual Result:**  
The user returned to the Products page and the item remained in the cart.

**Status:** PASS

---

### TC-020 — Complete Valid Purchase

**Priority:** High

**Preconditions:** User is logged in and has a product in the cart.

**Test Data:**
- First Name: Valid
- Last Name: Valid
- Postal Code: Valid

**Steps:**
1. Open the cart.
2. Select Checkout.
3. Enter valid customer information.
4. Continue to the order overview.
5. Verify order information.
6. Select Finish.

**Expected Result:**  
The order is completed and a confirmation page is displayed.

**Actual Result:**  
The checkout workflow completed successfully. The confirmation page displayed "Checkout: Complete!" and "Thank you for your order!" along with order-dispatch confirmation.

**Status:** PASS


Exploratory Menu Testing — SauceDemo

Test Information

• Application: SauceDemo
• Testing Type: Exploratory / Navigation / Functional UI testing
• Device: iPhone 12
• OS: iOS 26.6.2
• Browser: Google Chrome
• Tester: Independent QA Portfolio Project
• Purpose: Expand coverage beyond the original scripted test cases
by testing functionality available through the application’s
navigation menu.

Scope

The following menu options were explored:

1. All Items
2. Dynamic Catalog
  • Lazy Load
  • Spinner
  • Slider
3. About
4. Logout
5. Reset App State

────────

EXP-001 — All Items Navigation

Objective: Verify that the All Items menu option returns the user to
the complete product catalog.

Observed Result: - Selecting All Items returned to the Products
page. - The full product catalog loaded. - Products appeared consistent
with the catalog previously displayed.

Status: PASS

────────

EXP-002 — Dynamic Catalog: Lazy Load

Objective: Explore the Lazy Load catalog behavior and verify basic
product presentation and interaction.

Observed Result: - Selecting Lazy Load opened the dynamic
catalog. - Products loaded repeatedly as the user scrolled. - The tester
did not scroll far enough to establish whether the catalog was literally
infinite. - Products displayed through this catalog did not open a
detailed product view when their image, name, or product area was
selected.

Status: PASS / Observation

Notes: - Repeated product loading was not classified as a defect
because lazy loading can intentionally load additional content. - No
requirement was established that Dynamic Catalog products must provide
the same product-detail navigation as the standard All Items catalog. -
The lack of product-detail navigation was documented as an exploratory
observation rather than a confirmed defect.

────────

EXP-003 — Dynamic Catalog: Spinner

Objective: Explore the Spinner catalog behavior and verify basic
product presentation and interaction.

Observed Result: - Selecting Spinner opened a page visually
similar to the Lazy Load catalog. - The repeating/infinite-loading
behavior observed with Lazy Load was not observed here. - Products
displayed through this catalog did not open a detailed product view when
their image, name, or product area was selected.

Status: PASS / Observation

Notes: - No defect was filed because the intended functional
requirements for this demonstration catalog were not available. - The
difference in loading behavior between Lazy Load and Spinner was
documented for exploratory coverage.

────────

EXP-004 — Dynamic Catalog: Slider

Objective: Verify automatic and manual interaction with the Slider
catalog.

Observed Result: - Products automatically cycled through the
slider. - The tester could manually select products. - Slider
interaction appeared functional. - Products displayed through the slider
did not open a detailed product view when their image, name, or product
area was selected.

Status: PASS / Observation

Notes: - Automatic and manual slider behavior appeared functional. -
Lack of product-detail navigation was documented as an observation
rather than a confirmed defect because the expected behavior for Dynamic
Catalog products was not established.

────────

EXP-005 — About Navigation

Objective: Verify that the About menu option successfully navigates
to its intended destination.

Observed Result: - Selecting About navigated to the Sauce Labs
website. - The destination loaded successfully. - The external page
could be scrolled normally. - No broken page or navigation error was
observed during the test.

Status: PASS

Notes: - This test verifies the navigation link and successful
loading of the external destination. - Content and functionality
belonging to the external Sauce Labs website were not treated as
SauceDemo defects.

────────

EXP-006 — Logout and Protected-Page Access

Objective: Verify that Logout ends the authenticated session and
that previously protected pages cannot be accessed through browser
navigation.

Observed Result: - Selecting Logout fully logged the user out. -
Attempting to return to the previously viewed authenticated page using
the browser Back button did not restore access. - The application
displayed:
Epic sadface: You can only access '/dynamic-catalog-slider.html' when you are logged in.

Status: PASS

Notes: - The authentication error was considered expected behavior
because access to the protected page was correctly denied after
logout. - This test also verified that browser Back navigation did not
bypass the authenticated-session requirement.

────────

EXP-007 — Reset App State

Objective: Verify that Reset App State clears application state and
that the UI immediately reflects the reset state.

Observed Result: - Selecting Reset App State successfully
emptied the cart. - No other obvious application functionality appeared
to break. - However, product buttons remained Remove even though the
products were no longer in the cart. - Navigating away from the product
listing and returning caused the buttons to correctly change back to
Add to cart. - The behavior was reproduced consistently.

Status: FAIL

Confirmed Defect

GitHub Issue: #2 — Reset App State leaves product buttons as
“Remove” after clearing cart

Severity: Medium
Priority: Medium

Impact: The application’s underlying cart state is reset, but the
product controls temporarily display an incorrect state. A user could
reasonably believe a product remains in the cart because its button
still says Remove, even though the cart is empty.

Recovery: Navigating away from the product listing and returning
causes the product button to update to Add to cart.

────────

Exploratory Testing Summary

ID        Area                             Result

────────

EXP-001   All Items                        PASS
EXP-002   Dynamic Catalog — Lazy Load    PASS / Observation
EXP-003   Dynamic Catalog — Spinner      PASS / Observation
EXP-004   Dynamic Catalog — Slider       PASS / Observation
EXP-005   About                            PASS
EXP-006   Logout / Protected Page Access   PASS
EXP-007   Reset App State                  FAIL — Defect #2

Key Exploratory Findings

• Core navigation options were generally functional.
• Dynamic Catalog modes behaved differently from one another and were
explored for loading and interaction behavior.
• Dynamic Catalog products did not open the same detailed product view
available from the standard All Items catalog; this was documented
as an observation because the intended requirement was not
established.
• Logout correctly prevented access to the previously authenticated
page through browser Back navigation.
• Reset App State successfully cleared the cart but left product
controls displaying an incorrect Remove state until navigation
refreshed the product listing.
• The Reset App State UI defect was reproducible and documented as
GitHub Issue #2.

Testing Note

Exploratory results are based on observed application behavior during
this independent QA portfolio project. Where expected behavior could not
be established from the application’s visible functionality,
observations were documented without being classified as confirmed
defects.

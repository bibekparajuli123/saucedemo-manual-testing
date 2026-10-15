# Checkout Test Cases — SauceDemo

**Module:** Checkout
**URL:** https://www.saucedemo.com/checkout-step-one.html
**Precondition:** Logged in, at least 1 item in cart

## Test Cases

| ID | Title | Steps | Test Data | Expected Result | Priority |
|----|-------|-------|-----------|-----------------|----------|
| TC-CHK-001 | Checkout with valid info | 1. Click Checkout<br>2. Fill first name, last name, zip<br>3. Click Continue | John / Doe / 44600 | Navigate to checkout overview | High |
| TC-CHK-002 | Checkout with empty first name | 1. Checkout<br>2. Leave first name blank<br>3. Continue | (blank) / Doe / 44600 | Error: "First Name is required" | High |
| TC-CHK-003 | Checkout with empty last name | 1. Checkout<br>2. Leave last name blank<br>3. Continue | John / (blank) / 44600 | Error: "Last Name is required" | High |
| TC-CHK-004 | Checkout with empty zip | 1. Checkout<br>2. Leave zip blank<br>3. Continue | John / Doe / (blank) | Error: "Postal Code is required" | High |
| TC-CHK-005 | Checkout with all fields empty | 1. Checkout<br>2. Click Continue without filling | (blank) / (blank) / (blank) | Error for first name shown first | High |
| TC-CHK-006 | Verify order summary | 1. Complete info<br>2. Observe overview | — | Item total + tax = total, all correct | High |
| TC-CHK-007 | Cancel from step one | 1. Click Checkout<br>2. Click Cancel | — | Return to cart | Medium |
| TC-CHK-008 | Cancel from overview | 1. Reach overview<br>2. Click Cancel | — | Return to inventory | Medium |
| TC-CHK-009 | Complete full order | 1. Fill info<br>2. Click Finish | — | "Thank you for your order!" confirmation page | High |
| TC-CHK-010 | Back Home after order | 1. Complete order<br>2. Click "Back Home" | — | Redirect to inventory, cart empty | Medium |
| TC-CHK-011 | Zip accepts non-numeric | 1. Enter "ABCDE" as zip | ABCDE | Observe — accept or reject (document behavior) | Low |
| TC-CHK-012 | Verify tax calculation | 1. Complete checkout<br>2. Check tax value | — | Tax = 8% of item total (verify math) | Medium |

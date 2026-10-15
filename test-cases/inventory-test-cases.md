# Inventory Test Cases — SauceDemo

**Module:** Inventory / Product Listing
**URL:** https://www.saucedemo.com/inventory.html
**Precondition:** Logged in as standard_user

## Test Cases

| ID | Title | Steps | Test Data | Expected Result | Priority |
|----|-------|-------|-----------|-----------------|----------|
| TC-INV-001 | Verify product count on inventory page | 1. Log in as standard_user<br>2. Observe product grid | — | 6 products displayed | High |
| TC-INV-002 | Sort products by Name (A to Z) | 1. Select "Name (A to Z)" from sort dropdown | Name (A to Z) | Products sorted alphabetically ascending | High |
| TC-INV-003 | Sort products by Name (Z to A) | 1. Select "Name (Z to A)" | Name (Z to A) | Products sorted alphabetically descending | High |
| TC-INV-004 | Sort products by Price (low to high) | 1. Select "Price (low to high)" | Price (low to high) | Cheapest product first | High |
| TC-INV-005 | Sort products by Price (high to low) | 1. Select "Price (high to low)" | Price (high to low) | Most expensive first | High |
| TC-INV-006 | Open product detail page | 1. Click product name/image | Any product | Navigate to product detail page with full info | High |
| TC-INV-007 | Add single product to cart | 1. Click "Add to cart" on one product | Any product | Button changes to "Remove", cart badge shows 1 | High |
| TC-INV-008 | Add multiple products to cart | 1. Click "Add to cart" on 3 products | 3 products | Cart badge shows 3 | High |
| TC-INV-009 | Verify broken images (problem_user) | 1. Log in as problem_user<br>2. Observe product images | problem_user | BUG: images broken/wrong — observe and document | Medium |
| TC-INV-010 | Back to products from detail page | 1. Open product<br>2. Click "Back to products" | — | Returns to inventory page | Medium |

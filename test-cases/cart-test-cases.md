# Cart Test Cases — SauceDemo

**Module:** Shopping Cart
**URL:** https://www.saucedemo.com/cart.html
**Precondition:** Logged in as standard_user

## Test Cases

| ID | Title | Steps | Test Data | Expected Result | Priority |
|----|-------|-------|-----------|-----------------|----------|
| TC-CART-001 | View empty cart | 1. Log in<br>2. Click cart icon without adding items | — | Cart page shows 0 items, "Continue Shopping" visible | High |
| TC-CART-002 | Verify cart badge count | 1. Add 2 items<br>2. Observe cart icon | 2 items | Badge shows "2" | High |
| TC-CART-003 | Remove item from cart page | 1. Add 1 item<br>2. Go to cart<br>3. Click "Remove" | — | Item removed, badge disappears | High |
| TC-CART-004 | Remove item from inventory page | 1. Add item<br>2. Click "Remove" on inventory page | — | Item removed, badge updates | High |
| TC-CART-005 | Cart persists across page navigation | 1. Add item<br>2. Navigate to product detail<br>3. Back to inventory | — | Badge still shows 1 | Medium |
| TC-CART-006 | Cart persists after logout/login | 1. Add item<br>2. Logout<br>3. Login as same user | — | Cart items restored | Medium |
| TC-CART-007 | Verify item details in cart | 1. Add product<br>2. Open cart | — | Name, description, price, quantity all correct | Medium |
| TC-CART-008 | Continue Shopping button | 1. Open cart<br>2. Click "Continue Shopping" | — | Returns to inventory page | Medium |
| TC-CART-009 | Checkout button navigates | 1. Add item<br>2. Open cart<br>3. Click "Checkout" | — | Navigate to checkout step one | High |
| TC-CART-010 | Cart badge hidden when empty | 1. Add then remove all items | — | Cart badge not visible | Low |

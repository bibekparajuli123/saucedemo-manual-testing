# Login Test Cases — SauceDemo

**Module:** Login
**URL:** https://www.saucedemo.com/
**Test Data:** See credentials table below

## Credentials
| User | Password | Behavior |
|---|---|---|
| standard_user | secret_sauce | Normal user |
| locked_out_user | secret_sauce | Blocked from login |
| problem_user | secret_sauce | Has intentional bugs |
| performance_glitch_user | secret_sauce | Slow load times |

## Test Cases

| ID | Title | Preconditions | Steps | Test Data | Expected Result | Priority |
|----|-------|---------------|-------|-----------|-----------------|----------|
| TC-LOGIN-001 | Login with valid standard user | On login page | 1. Enter username<br>2. Enter password<br>3. Click Login | standard_user / secret_sauce | Redirect to /inventory.html, 6 products displayed | High |
| TC-LOGIN-002 | Login with locked out user | On login page | 1. Enter username<br>2. Enter password<br>3. Click Login | locked_out_user / secret_sauce | Error: "Sorry, this user has been locked out." | High |
| TC-LOGIN-003 | Login with invalid username | On login page | 1. Enter wrong username<br>2. Enter valid password<br>3. Click Login | wrong_user / secret_sauce | Error: "Username and password do not match" | High |
| TC-LOGIN-004 | Login with invalid password | On login page | 1. Enter valid username<br>2. Enter wrong password<br>3. Click Login | standard_user / wrongpass | Error: "Username and password do not match" | High |
| TC-LOGIN-005 | Login with empty username | On login page | 1. Leave username blank<br>2. Enter password<br>3. Click Login | (blank) / secret_sauce | Error: "Username is required" | Medium |
| TC-LOGIN-006 | Login with empty password | On login page | 1. Enter username<br>2. Leave password blank<br>3. Click Login | standard_user / (blank) | Error: "Password is required" | Medium |
| TC-LOGIN-007 | Login with both fields empty | On login page | 1. Leave both blank<br>2. Click Login | (blank) / (blank) | Error: "Username is required" | Medium |
| TC-LOGIN-008 | Username with leading/trailing spaces | On login page | 1. Enter " standard_user "<br>2. Enter password<br>3. Click Login | " standard_user " / secret_sauce | Login succeeds OR error shown — observe behavior | Low |
| TC-LOGIN-009 | Password field masks input | On login page | 1. Type password in password field | any password | Characters shown as dots/asterisks | Low |
| TC-LOGIN-010 | Login with problem_user | On login page | 1. Enter username<br>2. Enter password<br>3. Click Login | problem_user / secret_sauce | Redirect to inventory — note any visual/functional bugs | Medium |

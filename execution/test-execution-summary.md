# Test Execution Summary — SauceDemo

**Execution Date:** October 2026
**Tester:** [Your Name]
**Environment:** Chrome (latest), Windows 11
**Target URL:** https://www.saucedemo.com/

## Executive Summary
A total of 42 manual test cases were executed across 4 core modules: Login, Inventory, Cart, and Checkout. 

Testing was performed primarily using the `standard_user` account, with specific negative/edge-case scenarios executed using the `problem_user` account.

## Overall Results
| Module | Total Cases | Passed | Failed | Blocked | Pass Rate |
| :--- | :--- | :--- | :--- | :--- | :--- |
| **Login** | 10 | 9 | 1 | 0 | 90% |
| **Inventory** | 10 | 9 | 1 | 0 | 90% |
| **Cart** | 10 | 10 | 0 | 0 | 100% |
| **Checkout** | 12 | 11 | 1 | 0 | 92% |
| **TOTAL** | **42** | **39** | **3** | **0** | **93%** |

*(Note: Adjust the Pass/Fail numbers above if your actual test runs differed, e.g., if the Zip Code accepted letters, count that as a Fail).*

## Defect Summary
| Bug ID | Module | Severity | Summary |
| :--- | :--- | :--- | :--- |
| [BUG-001](../bug-reports/BUG-001.md) | Inventory | Medium | All product images display the same incorrect image for `problem_user`. |
| [BUG-002](../bug-reports/BUG-002.md) | Checkout | Critical | Cannot enter text into the "Last Name" field for `problem_user`. |

## Detailed Execution Log

### Login Module
- Total: 10 | Pass: 9 | Fail: 1
- **Notes:** Tested valid, invalid, locked-out, and empty inputs. TC-LOGIN-010 failed due to issues with `problem_user` inventory images (see BUG-001).

### Inventory Module
- Total: 10 | Pass: 9 | Fail: 1
- **Notes:** Sorting by Name (A-Z, Z-A) and Price (Low-High, High-Low) works as expected. TC-INV-009 failed (see BUG-001).

### Cart Module
- Total: 10 | Pass: 10 | Fail: 0
- **Notes:** Adding, removing, and verifying cart persistence across page navigation and logouts worked perfectly.

### Checkout Module
- Total: 12 | Pass: 11 | Fail: 1
- **Notes:** Form validation works correctly for `standard_user` (First Name, Last Name, Zip required). TC-CHK-001 fails specifically for `problem_user` due to the Last Name input being broken (see BUG-002).

# SauceDemo Manual Testing Portfolio

This repository contains a complete manual QA testing portfolio for [SauceDemo (Swag Labs)](https://www.saucedemo.com/), a demo e-commerce site built for testing practice.

## 📊 Project Overview
- **Total Test Cases:** 42
- **Pass Rate:** 93%
- **Bugs Found:** 2
- **Modules Tested:** Login, Inventory, Cart, Checkout
- **Testing Techniques Used:** Boundary Value Analysis, Equivalence Partitioning, Negative Testing, State Transition

## 📁 Repository Structure
- [`/test-cases`](./test-cases) — Detailed Markdown test cases organized by module.
- [`/bug-reports`](./bug-reports) — Professional bug reports with steps to reproduce and evidence.
- [`/execution`](./execution) — Final test execution summary and metrics.
- [`/evidence`](./evidence) — Screenshots proving the defects.

## 🐛 Key Defects Found
1. **[BUG-001](./bug-reports/BUG-001.md):** Broken image rendering on the Inventory page for `problem_user`.
2. **[BUG-002](./bug-reports/BUG-002.md):** Unable to input text into the "Last Name" field on the Checkout page for `problem_user`.

## 🔑 Test Credentials
- `standard_user` / `secret_sauce` (Happy Path)
- `problem_user` / `secret_sauce` (Bug Discovery)
- `locked_out_user` / `secret_sauce` (Negative Testing)

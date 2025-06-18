# 📘 PlaywrightTestKopius  
**Playwright Challenge**

This project is an automated test suite built with [Playwright](https://playwright.dev/) for validating core functionality of the Playwright documentation website. It follows a **Page Object Model (POM)** design to ensure modular, maintainable, and scalable test code.

---

## 📁 Project Structure

```text
.
├── pages/
│   ├── pageActions.page.js       # Encapsulates user interactions (POM)
│   └── pageObjects.js            # Reusable dynamic locator utilities
├── tests/
│   └── playwright-docs.spec.js   # Functional test cases
├── package.json
└── README.md


### 1. Install dependencies

npx playwright test

### 2. Run the Test

npx playwright test --headed



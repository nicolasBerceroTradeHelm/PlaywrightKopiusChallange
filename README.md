# 📘 PlaywrightTestKopius  
**Playwright Challenge**

This project is an automated test suite built with [Playwright](https://playwright.dev/) for validating core functionality of the Playwright documentation website. It follows a **Page Object Model (POM)** design to ensure modular, maintainable, and scalable test code.

Autor Nicolas Bercero

This Playwright test project automates the functional validation of the Playwright documentation site
It uses a modular Page Object Model (POM) structure to promote code reusability and maintainability
The pageActions class encapsulates user interactions such as navigating to the homepage, clicking buttons, interacting with the search bar, verifying text on the page, and validating the resulting URL.
Each interaction is abstracted behind descriptive methods, making the test flow clean and readable

The actual test, Search browserContext and validate URL, mimics a realistic user scenario: 
    the user navigates to the Docs section
    verifies the landing page
    searches for browserContext using the site's built-in search feature
    clicks on the first result
    and finally confirms the URL change corresponds to the BrowserContext class documentation 
    
Utility locators in pageObjects.js abstract selectors by role, class, and text, which enables dynamic element resolution without hardcoding complex selectors
This structure supports scalable, readable, and maintainable automated testing

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


1. Install dependencies

npx playwright test

2. Run the Test

npx playwright test --headed



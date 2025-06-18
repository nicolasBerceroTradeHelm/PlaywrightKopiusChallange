# PlaywrightTestKopius
Playwright Challenge

This project is an automated test suite built with Playwright for validating core functionality of the Playwright documentation website. It follows a Page Object Model (POM) design to ensure modular, maintainable, and scalable test code.

Project Structure.
├── pages/
│   ├── pageActions.page.js       # Encapsulates user interactions (POM)
│   └── pageObjects.js            # Reusable dynamic locator utilities
├── tests/
│   └── playwright-docs.spec.js   # Functional test cases
├── package.json
└── README.md

Getting Started
1. Install dependencies
npm install

2. Run the test
npx playwright test
Tip: Add --headed to see the browser UI during the test
Example: npx playwright test --headed

Created by Nicolas Bercero

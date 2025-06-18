# 📘 Part 1 - PlaywrightTestKopius  
**Playwright Challenge**

This project is an automated test suite built with [Playwright](https://playwright.dev/) for validating core functionality of the Playwright documentation website. It follows a **Page Object Model (POM)** design to ensure modular, maintainable, and scalable test code.

Autor 
-Nicolas Bercero

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
```

# 📝 Part 2 – Functional test case

User Story:
As a user, I want to edit my phone number in the profile section so I can keep my contact
information up to date.
Acceptance Criteria:
● The "Phone" field shows the current phone number.
● The Save button is only enabled if the field was modified with a valid value.
● The phone number must be validated (10 numeric digits).
● A confirmation message appears after saving.
● If there's a network error, a clear error message must be displayed.

Test Case:
Edit Phone Number with Valid Input and Handle Network Failure

Test Data
Figma Mockups
Valid Phone Numbers
Valid User

Preconditions:
User is logged in (Valid LogIn)
User navigates to the Profile section
The Phone field is visible and displays the current phone number.

1 - Validate that a valid phone number is on the Phone field and the save button is disabled by default
2 - Clear the Phone field
3 - Fill a new valid Phone Number
4 - Validate that save button is enabled as soon as a valid phone number is inputed
5 - click Save
6 - A confirmation Message appears after saving

Expected Result:
After entering a valid 10-digit number, the Save button becomes active
When Save is clicked and a network error occurs:
    A error message appears
    No change is saved

To simulate an error, you can do it the complicated way using DevTools by blocking the save request to simulate a failed submission, or by using tools like Requestly to mimic this scenario
You could also modify the back end to temporarily return the expected error response
There's also the easy way — simply turn off your network or Wi-Fi before clicking Save

To accurately test the error message:
First, confirm that the error is correctly shown through the UI after the expected steps are performed
Then verify the message text and style according to the design or UX guidelines
Ensure that the page doesn't crash or reload unexpectedly
Depending on the type of request failure, confirm that the error is logged and handled correctly (i.e., no unhandled exceptions in the console)



# Young Living QA Automation Project - Cypress

## Overview
This project contains an automated end-to-end test for the Young Living checkout flow based on a QA Automation Assignment.

The purpose of this project is to demonstrate:
- UI test automation skills
- End-to-end testing
- Test case interpretation
- Assertions and validations
- Automation framework structure using Cypress

---

## Tech Stack

- Language: JavaScript
- Framework: Cypress
- Test Runner: Cypress Test Runner
- IDE: Visual Studio Code

---

## Test Scenario

### Test Description
Validate that a user can successfully proceed through the checkout process without submitting the final order.

### Automated Flow

The automation performs the following steps:

1. Open Young Living website
2. Login with valid credentials
3. Search and add a product to the shopping cart
4. Open shopping cart
5. Proceed to checkout
6. Continue without sponsor
7. Fill out shipping address information
8. Handle Verify Address popup if displayed
9. Select shipping method
10. Enter payment information
11. Accept Terms and Conditions
12. Stop before submitting the order

---

## Validations Performed

The automation verifies:

- Product was successfully added to the cart
- Product price matches the Order Summary price in cart view
- Product price matches during checkout
- Shipping address verification was completed
- Payment information was added successfully

---

## Project Structure

```bash
YoungLiving/
│
├── cypress/
│   ├── e2e/
│   │   └── checkout.cy.js
│   │
│   ├── fixtures/
│   ├── support/
│
├── cypress.config.js
├── package.json
└── README.md
```

---

## Installation

Clone the repository:

```bash
git clone https://github.com/gabscardenasz/YoungLiving.git
```

Navigate into the project folder:

```bash
cd YoungLiving
```

Install dependencies:

```bash
npm install
```

---

## Running the Tests

Open Cypress Test Runner:

```bash
npx cypress open
```

Run tests in headless mode:

```bash
npx cypress run
```

Run a specific test:

```bash
npx cypress run --spec "cypress/e2e/checkout.cy.js"
```

---

## API Test Recommendation

One recommended API test for this application would be validating the Add to Cart API response.

### Suggested API Assertions

Verify that:
- The product is successfully added to the cart
- Correct product ID is returned
- Quantity updates correctly
- Cart subtotal matches expected value
- API response status is 200

This helps validate backend functionality independently from the UI and improves overall test reliability.

---

## Notes

- This project was created as part of a QA Automation technical assessment.
- The final order submission is intentionally not executed.
- Sensitive data such as credentials and payment information should be stored securely using environment variables or Cypress configuration files.

---

## Author

Gloria Gabriela Hassid  
Software QA Engineer  
San Francisco, CA

GitHub: https://github.com/gabscardenasz
LinkedIn: https://www.linkedin.com

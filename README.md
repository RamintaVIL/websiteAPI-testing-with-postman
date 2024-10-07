# API Testing with Postman & Newman

This project implements 7 automated API tests using Postman to test the API documented at Automation Exercise API (https://www.automationexercise.com/api_list). The API uses form-data instead of JSON for sending data in requests. The test suite includes a mix of GET, POST, and DELETE requests, with checks for response status codes and assertions for response body formats, ensuring flexibility when data changes.

This project provides a robust framework for testing APIs using Postman and Newman, ensuring that tests are flexible, re-runnable, and integrated into a CI/CD pipeline for automated execution. You can extend the suite by adding more API endpoints or additional test cases.

## Prerequisites

API Documentation: https://www.automationexercise.com/api_list

Before you begin, ensure the following tools are installed:

-   **Postman**: You can download it from [here](https://www.postman.com/downloads/).
-   **GitHub Actions** for setting up CI/CD with pipelines.
-   **Newman**: for running tests in a pipeline:

    ```bash
    npm install -g newman
    ```

    Test Cases

The test suite consists of the following 7 test cases, covering different types of requests:

GET /productsList
Fetches the list of products and verifies the status code and the response format (e.g., array of products with required fields like id, name, price).
POST /searchProduct
Submits a search query for a product and checks the status code. Validates that the response contains the expected structure for product search results.
POST /login
Sends a form-data request to log in a user and checks the response status and structure, ensuring fields like message and userId exist.
POST /signup
Tests user signup by sending form-data with user details. The test ensures the response contains expected fields like status, and the email format is validated.
DELETE /deleteAccount
Deletes an existing user account and verifies the status code. The test checks that the response contains a success message in the expected format.
GET /brandsList
Fetches a list of brands and checks the response for proper structure (array with brand names and ids). Validates that the response is correctly formatted.
POST /addToCart
Adds a product to the cart and checks the response for status and data integrity (e.g., correct product ID and quantity fields).

### 📝 Test Results

Once the tests are complete, the results will be displayed in the terminal or in the HTML report, including the number of tests that passed or failed. If a test fails, you can inspect the logs to troubleshoot the issue. The pipeline logs in GitHub Actions will provide additional details, such as error messages or failed assertions, helping you identify the cause of failure.

### 🙋🏽‍♀️ Authors

[RamintaVIL](https://github.com/RamintaVIL)

### 📜 License

Distributed under the ISC License. See [LICENSE.txt](./LICENSE.txt) for more information.

## 🧪 Test Cases

The following test cases have been implemented using Cypress:

✅ **Test Case 1: Register User**

    - Verifies that a new user can successfully register on the website.

✅ **Test Case 6: Contact Us Form**

    - Ensures that the "Contact Us" form works as expected and submits user inquiries correctly.

✅ **Test Case 7: Verify Test Cases Page**

    - Validates that the Test Cases page loads properly and displays the required information.

✅ **Test Case 9: Search Product**

    - Confirms the search functionality works by querying for a specific product and returning accurate results.

✅ **Test Case 10: Verify Subscription on Home Page**

    - Verifies that users can subscribe to the newsletter via the homepage.

✅ **Test Case 13: Verify Product Quantity in Cart**

    - Checks if the correct product quantity is displayed in the shopping cart.

✅ **Test Case 17: Remove Products From Cart**

    - Ensures users can successfully remove items from their shopping cart.

✅ **Test Case 21: Add Review on Product**

    - Validates that users can submit a product review.

## 🎯 Getting Started

### 💫 Prerequisites

Before you can run the test cases locally, ensure you have the following installed:

-   **Node.js** – [Download Node.js](https://nodejs.org)
-   **NPM** (included with Node.js)
-   **Git** – [Download Git](https://git-scm.com)

### 💻 Installation

To get the project set up locally, follow these steps:

1. Clone the repository:

```
git clone: https://github.com/RamintaVIL/website-testing-with-cypress
```

2. Install the necessary dependencies:

```
npm install
```

### 💨 Running Locally

There are two ways to run Cypress tests:

1. Interactive Mode

If you want to see the tests running step-by-step in a graphical interface, use the interactive mode. This will open a Cypress Test Runner where you can select specific test files and view their execution in a browser:

```bash
npm run test
```

2. Headless Mode

If you prefer to run all tests in the background without opening a browser, use headless mode. This is faster and runs the tests directly in the terminal:

```bash
npm run test:cmd
```

After running the tests in headless mode, you will see the results in your terminal, including details on any failed or passed tests.

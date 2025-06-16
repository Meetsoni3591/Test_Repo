# Test Cases for T1 - E-Commerce Website Project Development

Okay, I understand. As a senior QA engineer, I'll create two test cases based on the provided "E-Commerce Website Project Development" outline. These test cases will focus on different, but critical, aspects of a typical e-commerce site: User Registration and Product Browsing.

Here are the two detailed test cases:

**Test Case 1: User Registration - Valid Credentials**

*   **Title:** User Registration - Successful Registration with Valid Credentials

*   **Description:** This test case verifies the successful registration of a new user account on the e-commerce website using valid email address, password and other required details. It ensures the system creates a new user account without errors, and the user receives the necessary confirmation (if any).

*   **Steps:**

    1.  Navigate to the e-commerce website's homepage.
    2.  Click on the "Register" or "Create Account" link/button (depending on UI design).
    3.  On the registration form, enter the following valid data:
        *   First Name:  "Test"
        *   Last Name: "User"
        *   Valid Email Address: "test.user@example.com" (replace with a real, valid email address for testing)
        *   Password: "Password123!" (Password should meet complexity requirements if specified)
        *   Confirm Password: "Password123!" (Must match the password field)
        *   Date of Birth: "01/01/1990" (if required)
        *   Accept Terms and Conditions: Check the checkbox (if applicable)
        *   Address: 123 Main St, Anytown, CA 91234
        *   Phone Number: 555-123-4567
    4.  Click the "Register" or "Submit" button.

*   **Expected Result:**

    1.  The user is successfully registered and redirected to their account dashboard or a welcome page.
    2.  A success message is displayed to the user, confirming successful registration (e.g., "Registration Successful!").
    3.  The user's email address appears in the database of users.
    4.  If email confirmation is required, a confirmation email is sent to the provided email address. The user must be able to successfully verify their account by clicking the link in the email.
    5.  The user is able to login to their account using the provided email and password.

*   **Priority:** High

**Test Case 2: Product Browsing - Verify Product Listing and Filtering**

*   **Title:** Product Browsing - Verify Product Listing and Filtering Functionality

*   **Description:** This test case verifies the ability to browse products on the e-commerce website, confirming that products are displayed correctly and that filtering options are working as expected.

*   **Steps:**

    1.  Navigate to the e-commerce website's homepage.
    2.  Click on a category link in the navigation menu (e.g., "Electronics," "Clothing," etc.).
    3.  Observe the product listing page.  Verify that products are displayed with appropriate information (e.g., product image, name, price, short description).
    4.  Locate the available filtering options (e.g., price range, brand, color, size).
    5.  Select a filter option (e.g., select the "Brand: Nike" filter if available).
    6.  Verify that the product listing is updated to display only products that match the selected filter.
    7.  Clear the filter.
    8.  Select multiple filters (e.g., "Brand: Nike" and "Price: $50-$100").
    9.  Verify that the product listing is updated to display only products that match ALL selected filters.
    10. Repeat steps 5-9 with different filters and filter combinations.
    11. Sort the Product Listing based on Price High to Low.
    12. Verify that the product listing is sorted as expected.
    13. Sort the Product Listing based on Price Low to High.
    14. Verify that the product listing is sorted as expected.

*   **Expected Result:**

    1.  Products are displayed correctly with the expected information (image, name, price, description).
    2.  The correct number of products are returned based on the defined parameters.
    3.  The filter options are functioning correctly:
        *   Selecting a filter updates the product listing to display only products matching the selected filter.
        *   Clearing a filter returns the product listing to the unfiltered state.
        *   Selecting multiple filters displays only products matching ALL selected filters.
        *   Verify that the total count is displayed in the filter section and the total count displayed for the products on the page, match the filter.
    4.  Sorting the products based on "Price High to Low" displays the products in descending order of price.
    5.  Sorting the products based on "Price Low to High" displays the products in ascending order of price.
    6.  That the application should not crash with the product loading and filtering and sorting being applied.

*   **Priority:** High

These test cases cover critical functionalities of the e-commerce website. Further test cases would be needed to fully cover the project development outline.
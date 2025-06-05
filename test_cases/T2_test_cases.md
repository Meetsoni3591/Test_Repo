# Test Cases for T2 - Venues Management

Okay, here are two detailed test cases based on the Venues Management task. I've tried to cover different aspects of the functionality and have prioritized them appropriately.

**Test Case 1: Create a New Venue with Valid Data**

*   **Title:** Verify Venue Creation with Valid Data

*   **Description:** This test case verifies that an administrator can successfully create a new venue profile using valid input data for all required and optional fields. It focuses on positive data input and basic system functionality.

*   **Steps:**

    1.  **Precondition:** User is logged in as an administrator with appropriate permissions to access the Venue Management module.
    2.  Navigate to the Venue Management section within the application.
    3.  Click on the "Create New Venue" or similar button/link.
    4.  On the Venue Creation form, populate the following required fields with valid data:
        *   Venue Name: "The Grand Ballroom"
        *   Venue Type: "Ballroom"
        *   Address Line 1: "123 Main Street"
        *   City: "Anytown"
        *   State: "CA"
        *   Zip Code: "91234"
        *   Contact Email: "info@grandballroom.com"
        *   Contact Phone: "555-123-4567"
    5.  Populate the following optional fields with valid data:
        *   Address Line 2: "Suite 200"
        *   Website URL: "www.grandballroom.com"
        *   Description: "A luxurious ballroom perfect for weddings and events."
        *   Capacity: "500"
        *   Parking Information: "On-site parking available"
        *   Accessibility Information: "Wheelchair accessible"
    6.  Click on the "Save" or "Create" button.

*   **Expected Result:**

    1.  A success message is displayed indicating that the venue has been created successfully. (e.g., "Venue 'The Grand Ballroom' created successfully.")
    2.  The user is redirected to the Venue Details page for the newly created venue, displaying all the entered information.
    3.  The new venue appears in the list of venues in the Venue Management section.
    4.  The database should contain a new record for "The Grand Ballroom" with all the entered details.

*   **Priority:** High (Core functionality)

**Test Case 2: Attempt to Create a Venue with Invalid Data**

*   **Title:** Verify Venue Creation Failure with Invalid Data

*   **Description:** This test case verifies that the system correctly prevents an administrator from creating a new venue profile using invalid or missing data in required fields. It focuses on negative data input and validation mechanisms.

*   **Steps:**

    1.  **Precondition:** User is logged in as an administrator with appropriate permissions to access the Venue Management module.
    2.  Navigate to the Venue Management section within the application.
    3.  Click on the "Create New Venue" or similar button/link.
    4.  On the Venue Creation form, populate the following required fields with *invalid* data:
        *   Venue Name: "" (Empty field)
        *   Venue Type: "!!!!" (Invalid characters)
        *   Address Line 1: "123 Main Street"
        *   City: "" (Empty field)
        *   State: "ZZ" (Invalid state code)
        *   Zip Code: "1234" (Invalid zip code)
        *   Contact Email: "invalidemail" (Invalid email format)
        *   Contact Phone: "123" (Invalid phone number format)
    5.  Leave all optional fields blank.
    6.  Click on the "Save" or "Create" button.

*   **Expected Result:**

    1.  An error message is displayed indicating that required fields are missing or contain invalid data. The error messages should be specific and informative.  Examples:
        *   "Venue Name is required."
        *   "Venue Type contains invalid characters."
        *   "City is required."
        *   "State must be a valid 2-character state code."
        *   "Zip Code must be a valid 5-digit zip code."
        *   "Contact Email is not a valid email address."
        *   "Contact Phone must be a valid phone number."
    2.  The Venue Details page does not get created and the screen remains on the Venue Creation page.
    3.  The invalid data fields should be highlighted or otherwise visually indicated to the user.
    4.  No new venue record should be created in the database.

*   **Priority:** High (Core functionality and data integrity)

These test cases cover the basic creation of a venue. You would need to create further test cases to cover other aspects mentioned in the task description, such as:

*   **Editing Existing Venues:** Test cases for modifying venue details, including positive and negative data input scenarios.
*   **Deleting Venues:** Test cases to ensure venues can be deleted and that appropriate confirmation messages are displayed. Consider the implications of deleting a venue (e.g., any associated events are also deleted or orphaned).
*   **Venue Performance Tracking:** Test cases to verify that performance metrics are being tracked and displayed correctly. This might require creating dummy data and running reports.
*   **Event Setup:** Test cases for creating and managing events associated with a venue, including setting dates, times, capacities, and ticket prices.
*   **Discount and Guestlist Management:** Test cases for creating and applying discounts, and for managing guestlists for events at the venue.
*   **User Permissions:** Test cases to ensure that only users with the correct permissions can access and modify venue information.

Remember to document your test cases thoroughly and keep them updated as the application evolves. Good luck!
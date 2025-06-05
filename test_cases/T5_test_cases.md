# Test Cases for T5 - Users Management

Okay, I'm ready to craft two detailed test cases for the "Users Management" functionality of the PuraVida platform, based on your provided task description.

Here are the two test cases, focusing on different aspects of user management:

**Test Case 1: User Invitation and Activation Workflow**

*   **Title:** Verify successful user invitation and subsequent account activation.

*   **Description:** This test case verifies the end-to-end process of inviting a new user to the PuraVida platform, including the successful delivery of the invitation, the user's ability to activate their account via the invitation link, and the creation of a new, active user account with the expected profile information.

*   **Steps:**

    1.  **Precondition:** An administrator account with the "Manage Users" permission is logged into the PuraVida platform.
    2.  Navigate to the "Users Management" section.
    3.  Click on the "Invite User" button.
    4.  Enter a valid, unused email address in the "Email Address" field.
    5.  Enter the user's "First Name".
    6.  Enter the user's "Last Name".
    7.  Select the desired role (e.g., "Basic User", "Premium User") from the "Role" dropdown menu.
    8.  (Optional) Add any additional user information (e.g., phone number, company).
    9.  Click on the "Send Invitation" button.
    10. **Verification Step 1:** Observe a confirmation message indicating that the invitation was successfully sent.
    11. **Verification Step 2:** Check the invitation email (sent to the email address used in Step 4) for:
        *   Correct Sender (PuraVida platform).
        *   Appropriate Subject Line (e.g., "Invitation to join PuraVida").
        *   Clear and concise message body.
        *   A valid "Activate Account" link.
    12. **Verification Step 3:** Click on the "Activate Account" link in the invitation email. This should redirect to the PuraVida platform.
    13. On the activation page, enter a strong, valid password in the "Password" field.
    14. Confirm the password in the "Confirm Password" field.
    15. Click the "Activate Account" button.
    16. **Postcondition:** Successfully log in with the new username and password.
    17. Navigate to the Users Management page, search for the newly created user.
    18. Verify the username, first name, last name, and the status of the user.

*   **Expected Result:**

    1.  A success message "Invitation sent successfully" should be displayed after Step 9.
    2.  The invitation email should be received within a reasonable timeframe (e.g., under 5 minutes) and should contain all the expected elements listed in Step 11.
    3.  Clicking the activation link should redirect to the account activation page.
    4.  The user should be able to successfully create a password and activate their account.
    5.  The user should be successfully logged in after account activation.
    6.  The newly created user's profile should be present in the "Users Management" list, with the correct name, email, role, and a status indicating that the account is active.

*   **Priority:** High

**Test Case 2: User Profile Viewing and Status Verification**

*   **Title:** Verify the user profile display and status.

*   **Description:** This test case verifies the accuracy and completeness of user profile information displayed within the "Users Management" section. It also verifies the correct display of user status (e.g., active, inactive, pending activation) and the consistency of that status across different sections of the application.

*   **Steps:**

    1.  **Precondition:** An administrator account with the "Manage Users" permission is logged into the PuraVida platform.
    2.  Navigate to the "Users Management" section.
    3.  Search for a specific user by email address, first name, or last name. (Assume there are multiple users with varying statuses).
    4.  Click on the user's name or profile to view their detailed profile information.
    5.  **Verification Step 1:** Verify that the following information is accurately displayed:
        *   User's full name
        *   Email address
        *   Account Status (e.g., Active, Inactive, Pending Activation)
        *   Role (e.g., Basic User, Premium User, Administrator)
        *   Date of registration
        *   Last login date
        *   Other profile details (if applicable)
    6.  **Verification Step 2:** Check if the status of the user matches the expected status:
        *   If the user has activated their account, status displayed is "Active".
        *   If the user has not yet activated their account, status displayed is "Pending Activation".
        *   If the user has been deactivated by an admin, the status displayed is "Inactive".
    7.  Navigate to a different section of the application (e.g., a reporting dashboard, a user activity log) where the same user information might be displayed.
    8.  **Verification Step 3:** Verify that the user's status is consistent across all sections of the application.

*   **Expected Result:**

    1.  The search functionality should correctly locate the specified user.
    2.  All the user profile information listed in Step 5 should be accurately displayed and match the information that was originally entered or updated.
    3.  The user's status should accurately reflect their current account state.
    4.  The user's status should be consistent across all sections of the application where the user's information is displayed.

*   **Priority:** High
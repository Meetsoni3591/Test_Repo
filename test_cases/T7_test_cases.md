# Test Cases for T7 - Roles & Permissions

Okay, here are two detailed test cases based on the provided "Roles & Permissions" task, simulating what a Senior QA Engineer would create:

**Test Case 1:  Verification of Role Creation and Basic Permissions**

*   **Title:**  Role Creation and Basic Permission Assignment - Verify Success and UI Accuracy
*   **Description:**  This test case verifies that a user with appropriate administrative privileges can successfully create a new role and assign basic (read-only) permissions. The UI elements should accurately reflect the changes. This will test the core functionality of the role management system.
*   **Steps:**

    1.  **Pre-condition:** Log in to the application as a user with "Administrator" Role/permissions (or equivalent privilege).
    2.  Navigate to the "Roles & Permissions" management section (e.g., `Settings > User Management > Roles`).
    3.  Click on the "Create New Role" (or similar) button.
    4.  Enter a unique and descriptive "Role Name" (e.g., "Read-Only Analyst").
    5.  Enter a brief "Description" (e.g., "Role with read-only access to analytics data").
    6.  In the permission selection area, locate and select only the "Read" permission for the "Analytics Data" module. Ensure no "Create," "Update," or "Delete" permissions are selected for this module.
    7.  Click the "Save" or "Create" button to finalize the role creation.
    8. Verify the successful creation of the role.
    9. Verify that the new role "Read-Only Analyst" shows up in the roles list with appropriate details.
    10. Verify that the newly created role has only the "Read" permission assigned to the "Analytics Data" module.

*   **Expected Result:**

    1.  The new role "Read-Only Analyst" should be successfully created without any errors.
    2.  A success message (e.g., "Role created successfully") should be displayed.
    3.  The "Read-Only Analyst" role should be visible in the roles list with its name and description.
    4.  The role details view should show only the "Read" permission for "Analytics Data" assigned to the role.  No other permissions for "Analytics Data" or permissions for other modules should be assigned.
    5. The UI elements should render correctly (e.g. no overlapping text, correct color scheme).

*   **Priority:** High (Core Functionality)

**Test Case 2:  Deny Access Based on Missing Role and Permissions**

*   **Title:**  Role Based Access Control (RBAC) - Verify Access Denied with No Read Permission
*   **Description:**  This test case verifies that a user assigned a role without "Read" access to a specific module (in this case, the "Analytics Data" module, but could be generalized) is correctly denied access to that module. This validates the RBAC functionality's enforcement of permission restrictions.
*   **Steps:**

    1.  **Pre-condition 1:** The "Read-Only Analyst" role created in Test Case 1 must exist.
    2.  **Pre-condition 2:** Create a user account (e.g., "analyst1") and assign them the "Read-Only Analyst" role.
    3.  **Pre-condition 3:** Create a second user account (e.g., "analyst2") that has NO role assigned.
    4.  Log in to the application as "analyst1" user (with assigned "Read-Only Analyst" Role).
    5.  Navigate to the "Analytics Data" module.
    6.  Log in to the application as "analyst2" user (with NO Role assigned).
    7.  Navigate to the "Analytics Data" module.

*   **Expected Result:**

    1.  As "analyst1", the user should be able to view the "Analytics Data" module, but not be able to create, update, or delete any data within it. The UI should not show any buttons to create, update, or delete.
    2.  As "analyst2", the user should be denied access to the "Analytics Data" module. This could manifest as:
        *   A clear "Access Denied" message with informative text about the required permissions.
        *   The "Analytics Data" module being completely hidden from the user's navigation menu.
        *   If the user attempts to directly access the module via URL, they are redirected to a "Permission Denied" page or their dashboard.
    3.  The UI should not display any confusing or misleading information to the user.

*   **Priority:** High (Security and Data Integrity)

**Important Considerations for Roles & Permissions Testing (Beyond these Test Cases):**

*   **Negative Testing:**  Actively try to break the system by assigning conflicting permissions, modifying roles while users are logged in, etc.
*   **Edge Cases:** Roles with no permissions assigned, roles with all permissions assigned, very long role names, special characters in role names.
*   **User Experience:**  Are the error messages clear and helpful?  Is the UI intuitive for managing roles and permissions?
*   **Performance:**  Does the system slow down significantly when a large number of roles or permissions are defined?
*   **Concurrency:**  What happens if multiple administrators try to modify the same role simultaneously?
*   **Auditing:** Are role changes logged for auditing purposes?
*   **Hierarchy of Permissions:** If there are parent and child roles, test whether the child roles inherit the permissions of the parent roles.
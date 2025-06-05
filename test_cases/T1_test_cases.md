# Test Cases for T1 - Dashboard

Okay, I'm ready to write some test cases for the Dashboard. Here are two detailed test cases, focusing on core functionality and data accuracy:

**Test Case 1: Data Accuracy and Relevance of Key Metrics on the Dashboard**

*   **Title:** Validate Accuracy and Relevance of Key Metrics on Admin Dashboard

*   **Description:** This test case verifies that the key metrics displayed on the Admin Dashboard are accurate, up-to-date, and relevant to providing a useful overview of the platform's performance. It covers checks on user counts, venue statistics, and overall platform performance metrics.

*   **Steps:**

    1.  **Log in as an Admin user.** Use valid Admin credentials to access the platform.
    2.  **Navigate to the Dashboard.** (This may involve clicking a "Dashboard" link or being automatically redirected after login.)
    3.  **Identify the displayed key metrics.** (Examples: "Total Users", "Active Venues", "Total Transactions", "New Users This Week", "Revenue This Month"). Document each metric name.
    4.  **For each displayed metric, perform the following validation:**
        *   **User Count Verification (for "Total Users", "New Users This Week"):**
            *   Query the database directly (e.g., using SQL) to retrieve the actual count of users matching the metric's criteria.  Ensure the database query accurately reflects the dashboard metric's definition (e.g., users with "active" status, users created within the last 7 days).
            *   Compare the database result with the value displayed on the Dashboard.
        *   **Venue Statistics Verification (for "Active Venues", "Total Venues"):**
            *   Query the database to retrieve the actual count of venues matching the metric's criteria (e.g., venues with "active" status, all venues regardless of status).
            *   Compare the database result with the value displayed on the Dashboard.
        *   **Transaction and Revenue Verification (for "Total Transactions", "Revenue This Month"):**
            *   Query the database to retrieve the actual count and total value of transactions matching the metric's criteria (e.g., all successful transactions, transactions completed within the current month).
            *   Compare the database result with the value displayed on the Dashboard.
        *   **Check Data Update Frequency:** Examine the dashboard to see if there is an indication of when the data was last updated. If there is, note the timestamp. Manually trigger an event that should change one of the metrics and confirm that the change is reflected in the dashboard within a reasonable timeframe (e.g., within 5 minutes).
    5.  **Document any discrepancies.** Record the expected value (from the database), the actual value (from the Dashboard), and the difference.
    6.  **Verify the Time Period Covered:** Ensure each metric clearly indicates the time period it covers. For example, "Users Registered Last Month".

*   **Expected Result:**

    *   All key metrics displayed on the Admin Dashboard should accurately reflect the corresponding data in the database, with no discrepancies.
    *   The displayed values should be up-to-date, reflecting recent changes in the platform's data within the expected update frequency.
    *   Each metric should have a clear and unambiguous label, indicating the metric's name and the time period covered.
    *   The dashboard's update frequency, if displayed, should be accurate and reasonable.

*   **Priority:** High (Critical for trust and usability of the platform)

**Test Case 2: Admin Dashboard Responsiveness and Layout Across Different Screen Sizes**

*   **Title:** Validate Responsiveness and Layout of Admin Dashboard on Different Screen Sizes

*   **Description:** This test case verifies that the Admin Dashboard's layout and content display correctly and are usable across a range of screen sizes, including desktop, tablets, and mobile devices. This ensures a consistent and optimal user experience regardless of the device being used.

*   **Steps:**

    1.  **Log in as an Admin user.** Use valid Admin credentials to access the platform.
    2.  **Navigate to the Dashboard.**
    3.  **Using a desktop browser, resize the browser window to simulate different screen sizes.** Start with a large screen (e.g., 1920x1080) and gradually decrease the width and height to simulate tablet and mobile screen sizes.  Common sizes to test include:
        *   1920x1080 (Desktop)
        *   1366x768 (Desktop/Laptop)
        *   768x1024 (Tablet - Portrait)
        *   1024x768 (Tablet - Landscape)
        *   375x667 (Mobile - Portrait - e.g., iPhone 6/7/8)
        *   414x896 (Mobile - Portrait - e.g., iPhone 11/12)
        *   360x640 (Mobile - Portrait - Common Android)

    4.  **For each simulated screen size, observe the following:**
        *   **Overall Layout:**  Does the dashboard layout adapt correctly to the screen size? Are elements positioned logically? Are there any overlapping elements?
        *   **Text Readability:** Is the text legible and appropriately sized?  Does text wrap correctly within its containers?
        *   **Image and Icon Scaling:** Are images and icons scaled proportionally? Do they appear blurry or distorted?
        *   **Scrolling:** Is horizontal scrolling avoided?  Is vertical scrolling implemented appropriately when content exceeds the screen height?
        *   **Button and Link Functionality:** Are buttons and links easily clickable and accessible?
        *   **Element Visibility:** Are all dashboard elements (metrics, charts, navigation elements) visible and accessible? Are any elements being cut off or hidden?
        *   **Component Alignment:** Check that all components are properly aligned and there's no significant visual clutter.

    5.  **Repeat the above steps using actual devices:** Test on a representative sample of tablets (e.g., iPad, Android tablet) and mobile devices (e.g., iPhone, Android phone) in both portrait and landscape orientations. This validates the responsiveness on real-world hardware.

    6.  **Document any layout issues, visual defects, or usability problems encountered on each screen size and device.**  Include screenshots where appropriate.

*   **Expected Result:**

    *   The Admin Dashboard should be fully responsive and adapt its layout appropriately to different screen sizes, ensuring a consistent and optimal user experience.
    *   All elements on the Dashboard should be visible, legible, and accessible regardless of screen size.
    *   Text should wrap correctly and be appropriately sized for readability.
    *   Images and icons should scale proportionally without distortion.
    *   Horizontal scrolling should be avoided.
    *   Buttons and links should be easily clickable and accessible.
    *   The overall layout should be logically organized and visually appealing on all tested devices and screen sizes.

*   **Priority:** High (Important for accessibility and user satisfaction, especially with the increasing use of mobile devices for administration)
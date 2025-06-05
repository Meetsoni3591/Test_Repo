# Test Cases for T9 - KPIs to Track for Growth

Okay, I'm ready to write the test cases. Here are two detailed test cases based on the provided "KPIs to Track for Growth" task:

**Test Case 1**

*   **Title:** Verify Correct Calculation and Display of Monthly Active Users (MAU) KPI

*   **Description:** This test case verifies that the Monthly Active Users (MAU) KPI is calculated correctly based on user activity within the specified month and is displayed accurately in the designated dashboard/report.  MAU is a crucial indicator of user engagement and overall platform health.

*   **Steps:**

    1.  **Precondition:** The platform is live and receiving user activity. Ensure a mechanism exists for accurately tracking user actions and associated timestamps (e.g., database logging, event tracking).
    2.  **Data Setup:**  Ensure there is sufficient user data for the previous month and the current month. This includes:
        *   Users who were active in the previous month and are also active in the current month.
        *   Users who were only active in the previous month.
        *   Users who are newly active in the current month.
        *   Ensure edge case data, like users that have been deleted.
    3.  **Execution:**
        a.  Navigate to the dashboard/report displaying the MAU KPI.
        b.  Identify the reporting period being displayed (e.g., "Current Month").
        c.  Manually calculate the expected MAU value for the specified reporting period. This requires querying the database/tracking system for the number of unique users who performed at least one defined "active" action (e.g., login, posting content, making a purchase) within that period.
        d.  Compare the displayed MAU value on the dashboard with the manually calculated value.
    4.  **Repeat** Step 3 for Previous month
    5.  **Repeat** Step 3 for edge cases such as deleted users.

*   **Expected Result:**

    *   The displayed MAU value on the dashboard/report should exactly match the manually calculated MAU value for the specified reporting period (taking into account potential rounding conventions, which should be clearly defined).
    *   The displayed MAU value is consistent across all dashboards.
    *   Deleted users are not counted in the MAU calculation

*   **Priority:** High (Critical for assessing user engagement and platform health)

**Test Case 2**

*   **Title:** Validate Cohort Retention Rate Calculation and Visualization

*   **Description:** This test case verifies the accurate calculation and display of cohort retention rates.  Cohort analysis helps identify trends in user behavior and the long-term value of acquired users.  The test focuses on ensuring that users are correctly categorized into cohorts based on their acquisition date (e.g., month of signup) and that their continued activity is accurately tracked over time.

*   **Steps:**

    1.  **Precondition:** The platform is live and acquiring new users. Data on user sign-up dates and subsequent activity is being tracked and stored. A cohort retention analysis dashboard/report exists.
    2.  **Data Setup:** Identify a few cohorts (e.g., users who signed up in January, February, and March of the same year).  Ensure these cohorts have sufficient numbers of users and varying levels of activity in subsequent months. Include cohorts that are several months/years old to check long-term retention.
    3.  **Execution:**
        a.  Navigate to the cohort retention analysis dashboard/report.
        b.  Select a specific cohort (e.g., "January Signups").
        c.  Note the retention rate displayed for different periods following the cohort's signup date (e.g., 1-month retention, 3-month retention, 6-month retention, 12-month retention).
        d.  Manually calculate the expected retention rates for those periods. This requires:
            *   Identifying all users in the selected cohort.
            *   Determining how many of those users were active in each of the specified subsequent periods (e.g., how many January signups were active in February, April, July, and the following January).
            *   Dividing the number of active users in each period by the total number of users in the initial cohort to get the retention rate.
        e.  Compare the displayed retention rates on the dashboard/report with the manually calculated retention rates.
    4.  **Repeat** steps b-e for all cohorts.
    5.  **Repeat** Steps b-e for edge cases such as users that have been banned

*   **Expected Result:**

    *   The displayed retention rates for each cohort and each period should accurately match the manually calculated retention rates (again, accounting for any defined rounding conventions).
    *   The cohort definitions (e.g., date range for inclusion in the cohort) should be clear and consistently applied.
    *   Banned users are not included in the cohort.
    *   The visual representation of the cohort retention data (e.g., graphs, tables) should be clear, easy to understand, and accurately reflect the underlying data.

*   **Priority:** High (Critical for understanding user behavior and predicting long-term growth)

These two test cases provide a starting point for testing your KPI tracking. Remember to adapt them to the specific details of your platform and data tracking implementation.  Also, consider adding test cases for other important KPIs, such as Customer Acquisition Cost (CAC), Customer Lifetime Value (CLTV), Churn Rate, and Revenue Growth Rate. Good luck!
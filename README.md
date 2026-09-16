Exactly. The **Landing Page section is over-split**. Since your senior wants fewer, more meaningful UAT cases, we can combine the common Landing Page checks without losing coverage.

I’d reduce the common Landing Page from **13 → 6 cases**:

### LANDING PAGE — COMMON FRA FUNCTIONALITY

| Test Case ID | Test Scenario | Test Steps | Expected Result |
|---|---|---|---|
| FRA-LP-001 | Verify FRA Landing Page and case views | Log in as a PM and open the FRA Landing Page. Select **My Cases** and **All Cases**. | The FRA Landing Page is displayed successfully. My Cases displays cases created/owned by the logged-in PM, and All Cases displays all FRA cases accessible to the PM. |
| FRA-LP-002 | Verify Initiative Category and Status display | Select each Initiative Category — **New Product / Product Change, Corporate Action, Material Change in Process, NICRA and Other** — and review the available case statuses. | Cases are displayed under the selected category and each case appears under its correct status, including In Progress, Pending Endorsement, Refer Back, Endorsement by RFO and Completed. |
| FRA-LP-003 | Verify status counts and common case information | Compare the counts shown for each status with the displayed cases. Open an existing case and review **Status, Created By, Created Date, Last Updated Date and Completed Date**. | Status counts match the applicable records, and the common case information is displayed correctly for the selected case. |
| FRA-LP-004 | Verify FRA search and filtering | Search using an existing FRA case value and apply an available filter. Repeat the search using a non-existing value and clear the filter. | The matching case is displayed for an existing value, no record is displayed for a non-existing value, the applied filter displays only matching records, and clearing the filter restores the applicable records. |
| FRA-LP-005 | Verify FRA Landing Page sorting, pagination and scrolling | Sort a sortable column in ascending and descending order. Navigate through the available pages and scroll horizontally across the grid. | Records are displayed in the selected sort order, pagination works correctly without missing or duplicate records, and all configured columns are accessible through horizontal scrolling. |
| FRA-LP-006 | Verify FRA Landing Page category-specific fields | Select each FRA category and review the fields displayed in the Landing Page grid. | The configured fields for the selected category are displayed correctly, including the applicable category-specific fields and common case information. |

This is much cleaner. **Six cases cover the same functionality without creating a separate row for every tiny Landing Page behavior.**

For the category-specific sheets, I'd also keep an eye out for places where we can combine **entry + validation + character limit** when they're logically related, instead of unnecessarily creating 2–3 cases for one field.

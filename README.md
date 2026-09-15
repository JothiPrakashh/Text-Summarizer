I need you to create a COMPLETE, DETAILED UAT test-case workbook for the COI (Conflict of Interest) PRT assessment in Service Bench.

IMPORTANT: Do NOT give me a high-level summary of test areas/modules. I need actual individual UAT test cases. Every individual test case must be represented as ONE ROW in the Excel sheet.

The previous output was incorrect because it created rows such as:
"Category Selection | Landing page access and category switching | Select each category..."
That is only a test area, NOT an individual UAT test case.

I need:
ONE TEST CASE ID → ONE TEST SCENARIO → ONE SET OF TEST STEPS → ONE EXPECTED RESULT.

Do not group multiple validations into a single row.

==================================================
1. SOURCE OF TRUTH
==================================================

Use all information available in:
- The files/documents attached to this conversation
- The COI UAT test cases/workbooks already provided
- The Combined Business Requirements document
- The COI requirements/user stories
- The screenshots of the actual Service Bench UAT application provided in this conversation
- Any existing COI PM/RFO UAT workbook available in the attached files

Use the actual application screenshots and requirements to determine the fields, workflow stages, landing-page columns, export columns and role behaviour.

Do NOT invent fields, workflow stages, statuses or functionality.

Where the screenshots/requirements show something explicitly, use that exact terminology.

If a requirement is unclear or genuinely unavailable, flag it as "Requirement clarification required" rather than inventing a behaviour.

==================================================
2. COI ROLE SEPARATION
==================================================

Create separate UAT coverage for:

A. COI PM / Maker
B. COI RFO

The PM and RFO are NOT the same role.

CRITICAL:
The "Initiative" / "Initiate Risk Assessment" functionality is for the PM/Maker.

DO NOT create an "Initiative" sheet for RFO.

For PM:
Initiative → Landing Page → Landing Page Export → Workflow → Workflow Export

For RFO:
Landing Page → Landing Page Export → Workflow → Workflow Export

The RFO test cases must focus on what an RFO can actually see, access, review, endorse, refer back, etc.

Do not assume that RFO can perform PM/Maker actions.

==================================================
3. WORKBOOK STRUCTURE
==================================================

Create the following sheets:

COI_PM_Initiative
COI_PM_Landing_Page
COI_PM_Landing_Page_Export
COI_PM_Workflow
COI_PM_Workflow_Export

COI_RFO_Landing_Page
COI_RFO_Landing_Page_Export
COI_RFO_Workflow
COI_RFO_Workflow_Export

If a separate summary/index sheet is useful, create:
COI_Test_Case_Index

But the actual detailed test cases must be in the above sheets.

DO NOT create a sheet containing only module summaries.

==================================================
4. REQUIRED COLUMNS FOR EVERY TEST CASE SHEET
==================================================

Each detailed UAT sheet must contain these columns:

Test Case ID
Module
Test Scenario
Preconditions
Test Steps
Test Data
Expected Result
Status
Actual Result
Evidence / Screenshot
Remarks

Use "Not Executed" as the default value for Status.

Do not leave Test Scenario, Test Steps or Expected Result at a generic level.

==================================================
5. PM – INITIATIVE
==================================================

Create detailed individual test cases for the PM/Maker's Initiate Risk Assessment page.

The screenshots show that Initiative Category is selected on the Initiate Risk Assessment page.

The available initiative categories shown in the requirements/application include:

- OTCR – Investment-funded Change
- New Product / Product Change Assessment / New Product / Product Change
- Corporate Actions
- NICRA – New Initiatives Change Risk Assessment
- Others

For FRA there is an additional Material Change in Process category, but this is NOT a COI category unless explicitly supported by the COI requirements. Do not incorrectly add FRA-only functionality to COI.

For COI, create individual test cases for:

- Access to Initiate Risk Assessment
- Initiative Category field
- Each applicable category option
- Category switching
- Category-specific fields appearing after category selection
- Mandatory fields
- Field validation
- Field source/population behaviour
- PSID-based fields
- Business Function selection
- CFCR RFO population
- Save as draft, where supported
- Clear/reset behaviour, where supported
- Submission
- Validation when mandatory information is missing
- Successful submission with valid information
- Data persistence after submission
- Any category-specific behaviour explicitly stated in the requirements

IMPORTANT:
Do not create one test case called "Validate all fields".

Create separate test cases for each important field and each meaningful validation.

==================================================
6. CATEGORY-SPECIFIC INITIATIVE FIELDS
==================================================

Use the Combined Business Requirements document as the authoritative source for category-specific fields.

For example, the requirements/screenshots show that different categories have different fields.

For New Product / Product Change, fields include items such as:
- Programme code
- Programme Name
- Product manager
- Business head / Product head
- Business line
- CFCR RFO
- Product description & scope
- Applicable-to options where applicable

For Corporate Action, fields include:
- Project Name
- Transaction
- Rationale
- Responsible Person
- Accountable Executive
- MT Sponsor
- Business/Function
- CFCR RFO

For NICRA, fields include:
- New Initiative Name
- New Initiative Summary
- First Line
- Senior Manager / Group Business Head
- Country Coverage
- Business/Function
- CFCR RFO

For Other, fields include:
- New Initiative Name
- New Initiative Summary
- First Line
- Approver
- Country Coverage
- Business/Function
- CFCR RFO

Use the exact current requirements and application labels wherever available.

Do NOT assume all categories have identical fields.

==================================================
7. PM – LANDING PAGE
==================================================

Create detailed individual test cases for the COI PM landing page.

The landing page must be tested independently from the workflow.

Create individual test cases for:

ACCESS / VIEW
- PM can access the COI landing page
- My Cases view
- All Cases view
- Switching between My Cases and All Cases
- Correct records displayed for each view

CATEGORY
- Initiative Category selector
- Each COI category
- Switching between categories
- Grid refresh after category selection
- Correct category-specific records displayed

STATUS TILES
Test each status individually.

The common statuses shown in the application include:
- In Progress
- Pending Endorsement
- Refer Back
- Endorsement by RFO
- Completed

Create a separate test case for EACH status tile.

Also test:
- Status count
- Count consistency with grid records
- Selecting a status tile
- Correct records after selecting a status

GRID FUNCTIONS
Create individual test cases for:
- Search
- Search with valid value
- Search with invalid/non-matching value
- Clear search
- Filter
- Applying filter
- Clearing filter
- Ascending sort
- Descending sort
- Pagination
- Changing page
- Horizontal scrolling where applicable

==================================================
8. LANDING PAGE COLUMNS
==================================================

This is VERY IMPORTANT.

For EVERY category, the landing-page grid contains:

CATEGORY-SPECIFIC COLUMNS
+
COMMON COLUMNS.

The following columns are COMMON across categories:

Status
Created By
Created Date
Last Updated Date
Completed Date

Therefore, do NOT treat these as Corporate Action-only columns.

Create separate test cases for each common column.

For category-specific columns, use the exact columns shown in the requirements/application.

For example, Corporate Action has fields such as:

Case ID
Trigger Event / Driver
Project Name
Responsible Person
Transaction
Rationale
Accountable Executive / Key Stakeholder
MT Sponsor
Business Function
CFCR RFO

Then the common columns:

Status
Created By
Created Date
Last Updated Date
Completed Date

Create an individual test case for EACH column.

==================================================
9. LARGE DESCRIPTION FIELDS
==================================================

Some fields such as:

Transaction
Rationale

contain large text/description content.

In the landing page they may appear as "Click to View" rather than displaying the full text.

Therefore create separate test cases for:

1. Transaction displays as Click to View
2. Clicking Transaction opens/displays the full transaction
3. Full Transaction text is accurate
4. Rationale displays as Click to View
5. Clicking Rationale opens/displays the full rationale
6. Full Rationale text is accurate
7. Long text is not incorrectly truncated

Do NOT treat "Click to View" as the actual field value.

==================================================
10. PM – LANDING PAGE EXPORT
==================================================

Create a separate detailed sheet for Landing Page Export.

Do NOT create one test case called:
"Verify landing page export".

Create individual test cases for:

- Export option availability
- Export from My Cases
- Export from All Cases
- Export after category selection
- Export for each applicable COI category
- Successful file download
- Downloaded file opens correctly
- Exported data matches landing page data
- Exported Case ID
- Every category-specific field
- Common Status field
- Common Created By field
- Common Created Date field
- Common Last Updated Date field
- Common Completed Date field
- Export after applying search
- Export after applying filters
- Export after selecting status
- Exported filtered records match the filtered landing-page records
- Long text fields are correctly exported
- Transaction data is complete
- Rationale data is complete
- No unintended columns are missing
- No unrelated category data is included

Each field validation must be its own test case.

==================================================
11. PM – WORKFLOW
==================================================

Create detailed individual workflow test cases.

Use the actual COI workflow and existing COI requirements/workbook as the source of truth.

Do NOT invent stages.

The workflow test cases should cover, as applicable:

- Opening an assessment from the landing page
- Workflow loads successfully
- Workflow stages displayed correctly
- Current workflow stage
- Current status
- PM's available actions
- Actions that should NOT be available to PM
- Details panel
- Info tab
- History tab
- Case ID
- Initiative Category
- Trigger Event / Driver
- Category-specific information
- Common information
- Transaction
- Rationale
- RFO information
- Data carried from initiation into workflow
- Risk assessment responses
- Mitigation plan
- RFO assignment/coverage where applicable
- Submission for endorsement
- Refer-back behaviour
- Re-submission after refer back
- RFO endorsement status
- Final completion
- Any offline endorsement functionality explicitly present in the COI requirements
- Final submission/confirmation where applicable

For every workflow stage, test:
- Correct visibility
- Correct fields
- Correct role access
- Mandatory validations
- Correct action buttons
- Correct transition to the next stage
- Incorrect/invalid transition where applicable

==================================================
12. PM – WORKFLOW EXPORT
==================================================

Create a completely expanded Workflow Export sheet.

Each validation must be an individual test case.

Cover:

- Workflow Export availability
- Successful export
- Export file download
- File opens
- Case ID
- Initiative Category
- Trigger Event / Driver
- All category-specific fields
- All workflow-stage information that is intended to be exported
- Status
- Created By
- Created Date
- Last Updated Date
- Completed Date
- RFO information
- Risk assessment information where included
- Mitigation plan information where included
- Endorsement information where included
- Complete Transaction
- Complete Rationale
- No truncation of long-text fields
- Exported data matches workflow UI
- Correct data after refer back/re-submission
- Correct final data after completion

Use the actual Workflow Export requirements/workbook if provided.

==================================================
13. RFO – LANDING PAGE
==================================================

Now create a completely separate RFO test suite.

IMPORTANT:
RFO is NOT the PM.

Do not include PM-only initiation actions.

RFO landing-page coverage should include:

- RFO access
- My Cases / relevant RFO view
- All Cases where the RFO has access
- Category selection
- Category switching
- Status tiles
- Status counts
- Search
- Filter
- Sort
- Pagination
- Grid behaviour
- Category-specific columns
- Common columns

Common columns must still be tested:

Status
Created By
Created Date
Last Updated Date
Completed Date

Test the RFO's visibility based on the actual access/permission requirements.

Do not assume that RFO can see or edit everything that PM can.

==================================================
14. RFO – LANDING PAGE EXPORT
==================================================

Create individual test cases for:

- Export availability for RFO
- Export successful
- Exported records
- Exported columns
- Category-specific fields
- Common fields
- Status
- Created By
- Created Date
- Last Updated Date
- Completed Date
- Search/filter/status-based export
- Exported data matches RFO landing page
- Access-controlled data
- Long text fields
- Transaction
- Rationale

Use the actual application behaviour and requirements.

==================================================
15. RFO – WORKFLOW
==================================================

Create detailed individual RFO workflow test cases.

Focus on what the RFO actually does.

Include, where applicable:

- RFO opening an assigned assessment
- RFO viewing assessment information
- RFO viewing risk assessment responses
- RFO read-only access to PM-entered information
- RFO reviewing applicable risk areas
- RFO reviewing mitigation plan
- RFO/coverage status
- RFO comments
- Endorsement
- Refer Back
- Mandatory comments when referring back, if required
- Endorsement validation
- Multiple RFO behaviour, where applicable
- Individual RFO endorsement
- Other RFOs' status after one RFO endorses
- Final endorsement/completion behaviour
- Offline endorsement behaviour if applicable
- Access restrictions
- Fields that RFO cannot edit
- Correct workflow transitions
- History/audit trail

Use the existing COI requirements and previous COI UAT test cases as the source of truth.

==================================================
16. RFO – WORKFLOW EXPORT
==================================================

Create detailed individual test cases for RFO Workflow Export.

Cover:

- Export availability
- Successful export
- Correct Case ID
- Category
- Category-specific fields
- Common fields
- Workflow information
- RFO information
- RFO status
- RFO comments
- Endorsement information
- Refer-back information
- Risk assessment information
- Mitigation information
- Transaction
- Rationale
- Created By
- Created Date
- Last Updated Date
- Completed Date
- Data accuracy
- Complete long-text data
- Exported data matching the workflow UI
- Access-controlled information

==================================================
17. STATUS HANDLING
==================================================

Do NOT interpret "different statuses" as different categories.

Categories are:
- OTCR – Investment-funded Change
- New Product / Product Change
- Corporate Action
- NICRA
- Other

Statuses are separate concepts.

The landing page has common status tiles such as:
- In Progress
- Pending Endorsement
- Refer Back
- Endorsement by RFO
- Completed

Test categories and statuses separately.

==================================================
18. TEST CASE QUALITY
==================================================

Every test case must be executable by a UAT tester.

Bad example:

"Validate landing page columns."

Good example:

Test Case ID:
COI-PM-LP-XXX

Module:
Landing Page

Test Scenario:
Verify that the Case ID column displays the correct Case ID for each COI assessment.

Preconditions:
PM is logged into Service Bench and has access to the COI landing page. At least one COI assessment is available.

Test Steps:
1. Navigate to the COI landing page.
2. Select the applicable category.
3. Locate the Case ID column.
4. Compare the Case ID displayed in the landing page with the Case ID of the corresponding assessment.

Expected Result:
The Case ID column is displayed and shows the correct Case ID for each assessment.

This is the level of detail required.

==================================================
19. NEGATIVE TEST CASES
==================================================

Where the requirement supports validation, include negative test cases.

Examples:

- Mandatory field left blank
- Invalid value
- Invalid format
- Exceeding maximum character limit
- Attempting to submit without required information
- Unauthorized role attempting an action
- RFO attempting PM-only action
- PM attempting RFO-only action
- Invalid workflow transition
- Missing endorsement/comments where mandatory
- Invalid filter/search
- Empty result set

Do not invent validation rules that are not specified.

Only include negative tests where the requirements/application indicate such validation exists.

==================================================
20. DO NOT DUPLICATE USELESSLY
==================================================

Do not create hundreds of meaningless variations of the same test.

However, DO create separate cases when:
- A different field is being tested
- A different category is being tested
- A different role is being tested
- A different workflow action is being tested
- A different status is being tested
- A different export is being tested
- A different validation is being tested
- A different access/permission rule is being tested

==================================================
21. TEST CASE ID FORMAT
==================================================

Use clear IDs.

PM:
COI-PM-INIT-001
COI-PM-LP-001
COI-PM-LPE-001
COI-PM-WF-001
COI-PM-WFE-001

RFO:
COI-RFO-LP-001
COI-RFO-LPE-001
COI-RFO-WF-001
COI-RFO-WFE-001

Number sequentially within each sheet.

Do not use "XXX".

==================================================
22. IMPORTANT: DO NOT STOP AT A SUMMARY
==================================================

I want the actual expanded test cases.

DO NOT return:

Category Selection
Status Tiles
Grid Functions
Category Columns
Workflow
Export

as individual rows.

Those are MODULES.

Instead, expand each of them into all the individual test cases underneath them.

For example:

Module = Status Tiles

Test Case 1 = Verify In Progress tile
Test Case 2 = Verify Pending Endorsement tile
Test Case 3 = Verify Refer Back tile
Test Case 4 = Verify Endorsement by RFO tile
Test Case 5 = Verify Completed tile
Test Case 6 = Verify In Progress count
Test Case 7 = Verify Pending Endorsement count
etc.

==================================================
23. USE THE EXISTING COI UAT CONTENT
==================================================

If an existing COI UAT workbook contains detailed test cases, do NOT throw them away.

Use them as the baseline and EXPAND/IMPROVE them.

Preserve valid existing scenarios.

Add missing scenarios based on:
- Current requirements
- Current Service Bench screenshots
- Landing Page behaviour
- Landing Page Export
- Workflow
- Workflow Export
- PM/RFO role separation
- Category-specific fields
- Common columns
- Status tiles
- Search/filter/sort/pagination
- Click-to-view fields
- Data accuracy

Do not blindly copy COI test cases into RFO if the role behaviour differs.

==================================================
24. FINAL QUALITY CHECK BEFORE GIVING ME THE OUTPUT
==================================================

Before generating the workbook, perform a self-review.

Check:

1. Is every row an individual test case?
2. Does every test case have a unique ID?
3. Does every test case have Preconditions?
4. Does every test case have detailed Test Steps?
5. Does every test case have a specific Expected Result?
6. Are PM and RFO separated?
7. Is Initiative only under PM?
8. Are all applicable COI categories covered?
9. Are categories separated from statuses?
10. Are all five common landing-page columns tested?
11. Are category-specific columns tested individually?
12. Are Transaction and Rationale Click-to-View behaviours tested?
13. Are full Transaction/Rationale values tested?
14. Are Landing Page and Landing Page Export separated?
15. Are Workflow and Workflow Export separated?
16. Are export fields individually validated?
17. Are role permissions tested?
18. Are negative tests included where supported?
19. Are duplicate/useless tests avoided?
20. Have you used the actual requirements rather than inventing functionality?

If any answer is NO, fix the workbook before presenting it.

==================================================
25. OUTPUT
==================================================

Generate the actual Excel workbook with the detailed individual UAT test cases.

Do NOT just describe what the workbook should contain.

Do NOT give me a summary instead of the test cases.

The goal is a production-ready UAT test-case workbook where a tester can execute each row independently and record:

Status
Actual Result
Evidence / Screenshot
Remarks

The workbook should be detailed even if this results in a large number of test cases.

Accuracy and completeness are more important than keeping the number of test cases small.

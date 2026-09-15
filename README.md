Yes — **this gives us the missing piece.** I’ve now incorporated the Corporate Action screenshots into the COI test-case design, especially the **actual landing-page grid, status tiles, export structure, Details panel, Info/History tabs, and hyperlink behaviour for long-text fields**.

And I’m correcting the earlier version: **we should not make generic “data grid” cases only.** The grid/export cases need to validate the **actual columns applicable to each category**.

Below is the **COI PM + COI RFO test-case content** you can directly put into the workbook.

---

# COI — PM UAT TEST CASES

**Role: Project Manager**

For COI Non-Investment, the applicable categories are:

1. **New Product / Product Change**
2. **Corporate Action**
3. **NICRA – New Initiatives Change Risk Assessment**
4. **Other**

**OTCR – Investment-funded Change is excluded from Non-Investment testing.**

---

# A. COI PM — LANDING PAGE

### LP-01 — Access Landing Page

**Test Scenario:** Verify PM can access the COI Risk Assessment landing page.

**Test Steps:**
1. Login to Service Bench as a Project Manager.
2. Navigate to the COI Risk Assessment application.
3. Open the landing/home page.

**Expected Result:**  
COI Risk Assessment landing page is displayed successfully with the Initiative Category selector, status summary and assessment data grid.

---

### LP-02 — Initiative Category Selector

**Test Scenario:** Verify Initiative Category selector is available on the landing page.

**Test Steps:**
1. Open the COI landing page.
2. Click the Initiative Category dropdown.

**Expected Result:**  
The applicable COI assessment categories are displayed and can be selected.

---

### LP-03 — Select New Product / Product Change

**Expected Result:**  
Landing page refreshes to display assessments belonging to **New Product / Product Change**.

---

### LP-04 — Select Corporate Action

**Expected Result:**  
Landing page refreshes to display assessments belonging to **Corporate Action**.

---

### LP-05 — Select NICRA

**Expected Result:**  
Landing page refreshes to display assessments belonging to **NICRA**.

---

### LP-06 — Select Other

**Expected Result:**  
Landing page refreshes to display assessments belonging to **Other**.

---

# B. COI PM — MY CASES / ALL CASES

The screenshot shows **My cases** and **All cases**.

### LP-07 — My Cases

**Test Steps:**
1. Select **My cases**.
2. Review the assessment list.

**Expected Result:**  
Only assessments relevant to the logged-in PM are displayed.

---

### LP-08 — All Cases

**Test Steps:**
1. Select **All cases**.
2. Review the assessment list.

**Expected Result:**  
All assessments accessible to the PM for the selected category are displayed.

---

### LP-09 — Switch Between My Cases and All Cases

**Expected Result:**  
The grid refreshes correctly when switching between My cases and All cases, without retaining incorrect records from the previous view.

---

# C. COI PM — STATUS TILES

The UAT screen clearly shows:

- **In progress**
- **Pending endorsement**
- **Refer back**
- **Endorsement by RFO**
- **Completed**

These should be explicitly tested.

### LP-10 — In Progress

**Expected Result:**  
Selecting **In progress** displays assessments currently in In Progress status and the displayed count corresponds to the available records.

### LP-11 — Pending Endorsement

**Expected Result:**  
Selecting **Pending endorsement** displays assessments currently pending endorsement.

### LP-12 — Refer Back

**Expected Result:**  
Selecting **Refer back** displays assessments that have been referred back.

### LP-13 — Endorsement by RFO

**Expected Result:**  
Selecting **Endorsement by RFO** displays assessments currently at the RFO endorsement stage.

### LP-14 — Completed

**Expected Result:**  
Selecting **Completed** displays completed assessments.

### LP-15 — Status Count

**Test Steps:**
1. Select each available status.
2. Compare the count displayed on the status tile with the records displayed in the grid.

**Expected Result:**  
The status count accurately represents the number of applicable assessments for that status.

### LP-16 — Status and Grid Consistency

**Expected Result:**  
Every record displayed after selecting a status has the corresponding status.

### LP-17 — Status Reset

**Test Steps:**
1. Select a status.
2. Change to another status/category.

**Expected Result:**  
Grid refreshes correctly and does not retain records from the previous selection.

---

# D. COI PM — DATA GRID COMMON FUNCTIONALITY

### LP-18 — Grid Display

Verify the assessment data grid is displayed successfully.

### LP-19 — Required Columns

Verify all columns configured for the selected category are displayed.

### LP-20 — Column Order

Verify the configured columns are displayed in the expected order.

### LP-21 — Data Accuracy

Compare grid values against the corresponding assessment.

**Expected:**  
Grid values match the underlying assessment.

### LP-22 — Search

Search using a valid Case ID/available searchable value.

**Expected:**  
Matching assessment is displayed.

### LP-23 — Invalid Search

Search using a value for which no assessment exists.

**Expected:**  
No unrelated records are displayed and an appropriate no-data result is shown.

### LP-24 — Column Filter

Apply a filter using an available grid column.

**Expected:**  
Only matching records are displayed.

### LP-25 — Clear Filter

Clear the applied filter.

**Expected:**  
The applicable complete record set is restored.

### LP-26 — Ascending Sort

Sort an available sortable column in ascending order.

**Expected:**  
Records are correctly sorted.

### LP-27 — Descending Sort

Sort the same column in descending order.

**Expected:**  
Records are correctly sorted in descending order.

### LP-28 — Multiple Records

Verify multiple assessments can be displayed without data duplication or incorrect mapping.

### LP-29 — Pagination

Where multiple pages exist, navigate between pages.

**Expected:**  
Correct records are displayed on each page and pagination operates correctly.

### LP-30 — Horizontal Scroll

Verify horizontally scrolling the grid allows all configured columns to be accessed.

**Expected:**  
Additional columns can be viewed without losing data alignment.

---

# E. CATEGORY-SPECIFIC LANDING GRID

This is **very important** based on your screenshots.

## E1. New Product / Product Change

The screenshot shows columns including:

- Case ID
- Product description & scope
- Applicable to
- Status
- Created by
- Created date
- Last updated date
- Completed date

### LP-31

Verify **Case ID** is displayed correctly.

### LP-32

Verify **Product Description & Scope** is displayed correctly.

### LP-33

Verify **Applicable To** information is displayed correctly.

### LP-34

Verify **Status** is displayed correctly.

### LP-35

Verify **Created By** is displayed correctly.

### LP-36

Verify **Created Date** is displayed correctly.

### LP-37

Verify **Last Updated Date** is displayed correctly.

### LP-38

Verify **Completed Date** is displayed correctly where applicable.

### LP-39

Verify completed date remains blank/not populated for an assessment that is not completed.

---

# E2. Corporate Action

Based on the actual UAT screen, the grid contains category-specific fields such as:

- Case ID
- Trigger event / driver
- Project name
- Responsible person
- Transaction
- Rationale
- Accountable Executive / Key Stakeholder
- MT Sponsor
- Business Function
- CFCR RFO
- Status
- Created By
- Created Date
- Last Updated Date
- Completed Date

### LP-40

Verify Case ID.

### LP-41

Verify Trigger Event / Driver.

### LP-42

Verify Project Name.

### LP-43

Verify Responsible Person.

### LP-44

Verify Transaction.

### LP-45

Verify Rationale.

### LP-46

Verify Accountable Executive / Key Stakeholder.

### LP-47

Verify MT Sponsor.

### LP-48

Verify Business Function.

### LP-49

Verify CFCR RFO.

### LP-50

Verify Status.

### LP-51

Verify Created By.

### LP-52

Verify Created Date.

### LP-53

Verify Last Updated Date.

### LP-54

Verify Completed Date.

---

# F. LONG-TEXT HYPERLINKS

This is another thing you specifically clarified and **we absolutely need to capture it**.

Transaction and Rationale are large text boxes, therefore the grid displays **“Click to View”** rather than the complete text.

### LP-55 — Transaction Hyperlink

**Test Steps:**
1. Select Corporate Action.
2. Locate Transaction in the grid.
3. Click **Click to View**.

**Expected Result:**  
The complete Transaction description associated with the selected assessment is displayed.

### LP-56 — Rationale Hyperlink

**Expected Result:**  
The complete Rationale description is displayed when **Click to View** is selected.

### LP-57 — Transaction Data Integrity

Compare the full Transaction text displayed through the hyperlink with the Transaction entered during initiation.

**Expected:**  
Text matches exactly.

### LP-58 — Rationale Data Integrity

Compare the full Rationale text with the information entered during initiation.

**Expected:**  
Text matches exactly.

---

# G. NICRA LANDING GRID

Validate category-specific fields and the common fields.

Relevant NICRA fields include:

- Case ID
- Trigger Event / Driver
- New Initiative Name
- New Initiative Summary
- First Line
- Senior Manager / Group Business Head
- Country Coverage
- Business/Function
- CFCR RFO
- Status
- Created By
- Created Date
- Last Updated Date
- Completed Date

### LP-59 to LP-73

Create one test case for each of the above fields verifying that:

**Expected:**  
The value displayed in the landing grid matches the corresponding assessment information.

For **New Initiative Summary**, because it is a large text field, verify the configured **Click to View** behaviour if the application renders it as a hyperlink.

---

# H. OTHER LANDING GRID

Validate:

- Case ID
- Trigger Event / Driver
- New Initiative Name
- New Initiative Summary
- First Line
- Approver
- Country Coverage
- Business/Function
- CFCR RFO
- Status
- Created By
- Created Date
- Last Updated Date
- Completed Date

Again, each displayed value should match the underlying assessment.

---

# I. COI PM — LANDING PAGE EXPORT

This needs to be tested **category by category**, not just once.

### LP-74 — Export Availability

Verify Export option is available on the landing page.

### LP-75 — Export New Product

**Steps:**
1. Select New Product / Product Change.
2. Select applicable records.
3. Export.

**Expected:**  
New Product assessment data is exported successfully.

### LP-76 — Export Corporate Action

Export Corporate Action records.

**Expected:**  
Corporate Action records are exported successfully.

### LP-77 — Export NICRA

Export NICRA records.

### LP-78 — Export Other

Export Other records.

---

### LP-79 — Export File Opens

Open the downloaded file.

**Expected:**  
File opens successfully without corruption.

### LP-80 — New Product Export Columns

Verify export contains the configured New Product columns:

**Case ID, Product Description & Scope, Applicable To, Status, Created By, Created Date, Last Updated Date, Completed Date** and any other configured category columns.

### LP-81 — Corporate Action Export Columns

Verify export contains the configured Corporate Action fields including the category-specific data and common audit/status fields.

### LP-82 — NICRA Export Columns

Verify configured NICRA fields plus:

- Status
- Created By
- Created Date
- Last Updated Date
- Completed Date

### LP-83 — Other Export Columns

Verify configured Other fields plus common status/audit fields.

### LP-84 — Export Data Accuracy

Compare exported values against the landing-page records.

**Expected:**  
Exported values exactly correspond to the displayed records.

### LP-85 — Filtered Export

Apply a filter → Export.

**Expected:**  
Export reflects the applicable filtered dataset.

### LP-86 — Status Export

Select each status → Export.

**Expected:**  
Export contains records applicable to the selected status.

### LP-87 — My Cases Export

Select My cases → Export.

**Expected:**  
Export contains only records displayed within My cases.

### LP-88 — All Cases Export

Select All cases → Export.

**Expected:**  
Export contains all records accessible in All cases.

---

# J. COI PM — INITIATE RISK ASSESSMENT

Now the important part.

## Common

### PM-01

Verify PM can access **Initiate Risk Assessment**.

### PM-02

Verify Initiative Category dropdown.

### PM-03

Verify applicable categories:

- New Product / Product Change
- Corporate Action
- NICRA
- Other

### PM-04

Verify selecting a category dynamically loads the appropriate fields.

### PM-05

Verify changing category removes the previous category's fields and loads the newly selected category fields.

### PM-06

Verify Trigger Event / Driver dropdown is displayed.

### PM-07

Verify Trigger Event / Driver is mandatory.

### PM-08

Verify mandatory field validation prevents submission when required information is missing.

---

# K. NEW PRODUCT / PRODUCT CHANGE — PM

From your screenshots/BRD, validate:

- Programme Code
- Programme Name
- Product Manager
- Business Head / Product Head
- Business Line
- CFCR RFO
- Product Description & Scope
- Islamic Variant
- Sustainable Finance Variant

### PM-09 — Programme Code

Verify valid `PPG-` format is accepted.

### PM-10 — Programme Code Prefix

Enter value without required prefix.

**Expected:** Invalid format is rejected.

### PM-11 — Programme Code Spaces

Enter spaces.

**Expected:** Spaces are not accepted.

### PM-12 — Programme Code Length

Verify maximum permitted digits/length.

### PM-13 — Programme Name

Verify valid programme name can be entered.

### PM-14 — Programme Name Length

Verify configured maximum length.

### PM-15 — Product Manager

Verify logged-in PM is automatically populated.

### PM-16 — Business Head/Product Head

Verify valid PSID can be searched and selected.

### PM-17 — Business Line

Verify L2 Business Line can be selected.

### PM-18 — Single Business Line

Verify only one L2 Business Line can be selected.

### PM-19 — CFCR RFO

Verify CFCR RFO is populated according to CRHS logic.

### PM-20 — Single CFCR RFO

Verify only one Group RFO can be selected.

### PM-21 — Product Description & Scope

Verify valid text can be entered.

### PM-22 — Product Description & Scope Maximum

Verify maximum 5,000 characters.

### PM-23 — Islamic Variant

Verify checkbox can be selected.

### PM-24 — Sustainable Finance Variant

Verify checkbox can be selected.

### PM-25 — Applicable To Optional

Verify both checkboxes can remain unselected where applicable.

### PM-26 — Successful New Product Initiation

Populate valid mandatory fields and submit.

**Expected:**  
COI New Product / Product Change assessment is created successfully and appears on the landing page.

---

# L. CORPORATE ACTION — PM

Fields from your actual screen/BRD:

- Project Name
- Transaction
- Rationale
- Responsible Person
- Accountable Executive
- MT Sponsor
- Business/Function
- CFCR RFO

### PM-27

Verify all Corporate Action fields are displayed.

### PM-28

Verify Project Name accepts valid value.

### PM-29

Verify Project Name maximum 30 characters.

### PM-30

Verify Transaction accepts valid long-text input.

### PM-31

Verify Transaction maximum configured length.

### PM-32

Verify Rationale accepts valid long-text input.

### PM-33

Verify Rationale maximum configured length.

### PM-34

Verify Responsible Person is populated according to PSID logic.

### PM-35

Verify Accountable Executive can be selected using PSID.

### PM-36

Verify MT Sponsor can be selected using PSID.

### PM-37

Verify multiple Business/Functions can be selected.

### PM-38

Verify applicable CFCR RFOs are populated from CRHS.

### PM-39

Verify multiple CFCR RFOs can be selected.

### PM-40

Verify mandatory-field validation.

### PM-41

Verify successful Corporate Action submission.

**Expected:**  
COI Corporate Action assessment is created successfully.

---

# M. NICRA — PM

Fields:

- New Initiative Name
- New Initiative Summary
- First Line
- Senior Manager / Group Business Head
- Country Coverage
- Business/Function
- CFCR RFO

### PM-42

Verify NICRA fields.

### PM-43

Verify New Initiative Name.

### PM-44

Verify New Initiative Summary.

### PM-45

Verify First Line population.

### PM-46

Verify Senior Manager / Group Business Head PSID selection.

### PM-47

Verify Country Coverage supports multiple countries.

### PM-48

Verify maximum **5 countries**.

### PM-49

Verify sixth country cannot be selected.

### PM-50

Verify multiple Business/Functions.

### PM-51

Verify CFCR RFO population from CRHS.

### PM-52

Verify multiple CFCR RFOs.

### PM-53

Verify mandatory validation.

### PM-54

Verify successful NICRA initiation.

---

# N. OTHER — PM

Fields:

- New Initiative Name
- New Initiative Summary
- First Line
- Approver
- Country Coverage
- Business/Function
- CFCR RFO

### PM-55

Verify Other category fields.

### PM-56

Verify New Initiative Name.

### PM-57

Verify New Initiative Summary.

### PM-58

Verify First Line population.

### PM-59

Verify Approver PSID selection.

### PM-60

Verify multiple Country Coverage.

### PM-61

Verify maximum five countries.

### PM-62

Verify sixth country is prevented.

### PM-63

Verify multiple Business/Functions.

### PM-64

Verify CFCR RFO population.

### PM-65

Verify multiple CFCR RFO selection.

### PM-66

Verify mandatory validation.

### PM-67

Verify successful Other assessment initiation.

---

# O. COI PM — POST-SUBMISSION

### PM-68 — Assessment Appears in Landing Page

After successful submission, verify the new assessment appears on the COI landing page.

### PM-69 — Case ID

Verify unique Case ID is generated and displayed.

### PM-70 — Category Retention

Verify selected category is retained.

### PM-71 — Entered Data Retention

Verify submitted information is retained.

### PM-72 — Initial Status

Verify newly created assessment appears under the appropriate initial status.

### PM-73 — Landing Grid Mapping

Verify all applicable submitted fields appear against the newly created record.

---

# P. COI PM — WORKFLOW

### WF-01

Verify PM can open an assessment from the landing page.

### WF-02

Verify workflow page loads successfully.

### WF-03

Verify workflow steps are displayed.

### WF-04

Verify current status is displayed correctly.

### WF-05

Verify status shown in landing page matches workflow status.

### WF-06

Verify appropriate actions are available based on current status.

### WF-07

Verify actions not applicable to the current status are unavailable.

---

# Q. COI PM — DETAILS PANEL

Your screenshots give us a **much more specific requirement** here.

The right-side panel has **Info** and **History**.

### WF-08 — Details Panel

Verify right-side Details panel is displayed.

### WF-09 — Info Tab

Verify Info tab is available.

### WF-10 — History Tab

Verify History tab is available.

### WF-11 — Case ID

Verify correct Case ID is displayed.

### WF-12 — Initiative Category

Verify correct category is displayed.

### WF-13 — Trigger Event / Driver

Verify correct Trigger Event / Driver is displayed.

### WF-14 — Category-specific Information

Verify relevant fields for the selected category are displayed.

### WF-15 — Data Accuracy

Compare Details panel information with submitted assessment data.

**Expected:**  
Information matches the assessment.

### WF-16 — Long-text Information

Where Transaction/Rationale/New Initiative Summary/etc. is represented by **Click to View**, select it.

**Expected:**  
Complete text is displayed.

### WF-17 — Details Panel Scroll

Scroll through the Details panel.

**Expected:**  
All configured details can be accessed.

### WF-18 — View More

Select **View more** where available.

**Expected:**  
Additional configured assessment information is displayed.

### WF-19 — History

Select History.

**Expected:**  
Relevant workflow/activity history for the assessment is displayed.

### WF-20 — Assessment Switching

Open Assessment A → open Assessment B.

**Expected:**  
Details and History refresh to Assessment B; no information from Assessment A remains.

---

# R. COI PM — WORKFLOW EXPORT

This is **separate from Landing Page Export**.

### WF-21

Verify Workflow Export option is available.

### WF-22

Export a New Product assessment.

### WF-23

Export a Corporate Action assessment.

### WF-24

Export a NICRA assessment.

### WF-25

Export an Other assessment.

### WF-26

Verify downloaded workflow export opens successfully.

### WF-27

Verify Case ID in workflow export.

### WF-28

Verify Initiative Category in workflow export.

### WF-29

Verify Trigger Event / Driver.

### WF-30

Verify category-specific fields are exported.

### WF-31

Verify status is exported correctly.

### WF-32

Verify Created By.

### WF-33

Verify Created Date.

### WF-34

Verify Last Updated Date.

### WF-35

Verify Completed Date where applicable.

### WF-36

Verify exported values match the workflow screen.

### WF-37

Verify exported values match the Details panel.

### WF-38

Verify long-text fields are exported completely and are not truncated.

### WF-39

Verify export of assessment in different workflow statuses.

**Expected:**  
Correct current status and available assessment information are exported.

---

# COI — RFO UAT TEST CASES

Now **RFO does not get Initiate Risk Assessment**.

The RFO set therefore begins with the landing page.

---

# A. RFO LANDING PAGE

### RFO-01

Verify RFO can access COI Risk Assessment landing page.

### RFO-02

Verify RFO can view applicable COI assessments.

### RFO-03

Verify Initiative Category selector.

### RFO-04

Verify New Product / Product Change records.

### RFO-05

Verify Corporate Action records.

### RFO-06

Verify NICRA records.

### RFO-07

Verify Other records.

### RFO-08

Verify My Cases.

### RFO-09

Verify All Cases.

### RFO-10

Verify switching between My Cases and All Cases.

---

# B. RFO STATUS TESTING

### RFO-11 — In Progress

Verify assessments in In Progress status.

### RFO-12 — Pending Endorsement

Verify Pending endorsement assessments.

### RFO-13 — Refer Back

Verify Refer back assessments.

### RFO-14 — Endorsement by RFO

Verify assessments requiring/at RFO endorsement.

### RFO-15 — Completed

Verify completed assessments.

### RFO-16 — Status Count

Verify displayed status counts.

### RFO-17 — Status/Grid Consistency

Verify all records under a selected status have the corresponding status.

---

# C. RFO DATA GRID

### RFO-18

Verify grid is displayed.

### RFO-19

Verify required columns.

### RFO-20

Verify column order.

### RFO-21

Verify Case ID.

### RFO-22

Verify category-specific values.

### RFO-23

Verify Status.

### RFO-24

Verify Created By.

### RFO-25

Verify Created Date.

### RFO-26

Verify Last Updated Date.

### RFO-27

Verify Completed Date.

### RFO-28

Verify Search.

### RFO-29

Verify invalid Search.

### RFO-30

Verify column Filter.

### RFO-31

Verify Clear Filter.

### RFO-32

Verify ascending Sort.

### RFO-33

Verify descending Sort.

### RFO-34

Verify multiple records.

### RFO-35

Verify Pagination.

### RFO-36

Verify horizontal scrolling.

---

# D. RFO CATEGORY-SPECIFIC GRID

The **same category-specific column validation** needs to be performed for RFO:

### New Product / Product Change
- Case ID
- Product Description & Scope
- Applicable To
- Status
- Created By
- Created Date
- Last Updated Date
- Completed Date

### Corporate Action
- Case ID
- Trigger Event / Driver
- Project Name
- Responsible Person
- Transaction
- Rationale
- Accountable Executive / Key Stakeholder
- MT Sponsor
- Business Function
- CFCR RFO
- Status
- Created By
- Created Date
- Last Updated Date
- Completed Date

### NICRA
Validate the applicable NICRA fields plus the common status/audit fields.

### Other
Validate the applicable Other fields plus the common status/audit fields.

---

# E. RFO LONG-TEXT HYPERLINKS

### RFO-37

Verify Transaction displays **Click to View** where applicable.

### RFO-38

Click Transaction → verify complete text.

### RFO-39

Verify Rationale displays **Click to View** where applicable.

### RFO-40

Click Rationale → verify complete text.

### RFO-41

Verify displayed long-text values match the assessment.

---

# F. RFO — LANDING PAGE EXPORT

### RFO-42

Verify Export option.

### RFO-43

Export New Product / Product Change.

### RFO-44

Export Corporate Action.

### RFO-45

Export NICRA.

### RFO-46

Export Other.

### RFO-47

Verify downloaded file opens.

### RFO-48

Verify category-specific columns.

### RFO-49

Verify common columns.

**Common columns to explicitly validate for every category:**

- **Status**
- **Created By**
- **Created Date**
- **Last Updated Date**
- **Completed Date**

This is exactly the point you just clarified — **these are common columns for every category.**

### RFO-50

Verify exported values match landing page.

### RFO-51

Verify filtered export.

### RFO-52

Verify export by status.

### RFO-53

Verify My Cases export.

### RFO-54

Verify All Cases export.

---

# G. RFO — WORKFLOW

### RFO-55

Verify RFO can open an accessible assessment.

### RFO-56

Verify workflow page loads.

### RFO-57

Verify workflow steps.

### RFO-58

Verify current status.

### RFO-59

Verify landing-page status matches workflow status.

### RFO-60

Verify category displayed correctly.

### RFO-61

Verify category-specific assessment information.

### RFO-62

Verify status-specific information/actions available to RFO.

---

# H. RFO — DETAILS PANEL

### RFO-63

Verify Details panel is displayed.

### RFO-64

Verify **Info** tab.

### RFO-65

Verify **History** tab.

### RFO-66

Verify Case ID.

### RFO-67

Verify Initiative Category.

### RFO-68

Verify Trigger Event / Driver.

### RFO-69

Verify category-specific information.

### RFO-70

Verify Status.

### RFO-71

Verify Created By.

### RFO-72

Verify Created Date.

### RFO-73

Verify Last Updated Date.

### RFO-74

Verify Completed Date where applicable.

### RFO-75

Verify long-text **Click to View** information.

### RFO-76

Verify View More.

### RFO-77

Verify History displays appropriate assessment/workflow history.

### RFO-78

Verify Details panel refreshes when moving from one assessment to another.

---

# I. RFO — WORKFLOW EXPORT

### RFO-79

Verify Workflow Export option.

### RFO-80

Export New Product assessment.

### RFO-81

Export Corporate Action assessment.

### RFO-82

Export NICRA assessment.

### RFO-83

Export Other assessment.

### RFO-84

Verify export file opens successfully.

### RFO-85

Verify Case ID.

### RFO-86

Verify Initiative Category.

### RFO-87

Verify Trigger Event / Driver.

### RFO-88

Verify category-specific fields.

### RFO-89

Verify Status.

### RFO-90

Verify Created By.

### RFO-91

Verify Created Date.

### RFO-92

Verify Last Updated Date.

### RFO-93

Verify Completed Date where applicable.

### RFO-94

Verify exported values match workflow.

### RFO-95

Verify exported values match Details panel.

### RFO-96

Verify complete long-text information is exported.

### RFO-97

Verify export across different workflow statuses.

---

# VERY IMPORTANT — WHAT WE HAVE NOW LOCKED DOWN

For **every one of the 5 PRTs**, we should use this architecture.

### PM workbook

**1. Landing Page**
- Category selection
- My Cases / All Cases
- Status tiles
- Status counts
- Data grid
- Category-specific columns
- Common columns
- Search
- Filter
- Sort
- Pagination
- Horizontal scrolling
- Long-text hyperlinks

**2. Landing Page Export**
- Every category
- Category-specific columns
- Common columns
- Filtered export
- Status export
- My/All cases export
- Data accuracy

**3. Initiate Risk Assessment**
- Every applicable Non-Investment category
- Category-specific fields
- Validation
- Population logic
- Multi-select logic
- Character limits
- Successful submission
- Data persistence

**4. Workflow**
- Status
- Workflow steps
- Actions

**5. Details Panel**
- Info
- History
- Category-specific information
- Status
- View More
- Click to View
- Refresh between assessments

**6. Workflow Export**
- Every category
- Category-specific fields
- Common audit/status fields
- Long-text fields
- Statuses
- Data integrity

---

### RFO workbook

Exactly the same **except Initiate Risk Assessment is removed**, because RFO is not the initiating role.

So:

**Landing Page → Data Grid → Status → Search/Filter/Sort → Landing Export → Workflow → Details/History → Workflow Export**

---

And yes, your latest screenshots establish one more thing very clearly:

> **Status, Created By, Created Date, Last Updated Date and Completed Date should be treated as common landing-page columns across every category**, while the remaining columns are category-specific.

Also, **Transaction/Rationale being shown as “Click to View” is not an error** — they're large description fields, so we should specifically test both the hyperlink behaviour **and the underlying full-text data integrity**.

This COI PM/RFO set is now the **template I would use for the remaining 4 PRTs**.

For COI, you want 2 separate workbooks:
Workbook 1 — COI PM
Separate sheets such as:
1. Initiative — PM initiation/field validation for all applicable categories
2. Landing Page — category selection, status tiles, grid, common/category-specific columns, search/filter/sort, etc.
3. Landing Page Export — export validations
4. Workflow — PM workflow + Details/Info/History
5. Workflow Export — workflow export validations
Workbook 2 — COI RFO
Separate sheets:
1. Landing Page
2. Landing Page Export
3. Workflow
4. Workflow Export
No Initiative sheet for RFO, because RFO isn't initiating the assessment.
And within each sheet, the test cases cover the different categories (New Product/Product Change, Corporate Action, NICRA, Other), rather than creating a separate workbook for each category.

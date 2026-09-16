Yes. I’ll keep **exactly the screenshot format** throughout:

**Test Case ID | Test Scenario | Test Steps | Expected Result**

No Feature column, no Role column, no extra fields. I’ll also keep the section headings like **LANDING PAGE**, **INITIATE RISK ASSESSMENT**, **DETAILS**, **LANDING PAGE EXPORT**, and **WORKFLOW EXPORT**.

## 1. LANDING PAGE — COMMON FRA FUNCTIONALITY

| Test Case ID | Test Scenario | Test Steps | Expected Result |
|---|---|---|---|
| FRA-LP-001 | Verify FRA Landing Page is displayed | Log in as a PM and open the FRA Landing Page. | The FRA Landing Page is displayed successfully. |
| FRA-LP-002 | Verify My Cases view | Select My Cases on the FRA Landing Page. | Cases created/owned by the logged-in PM are displayed. |
| FRA-LP-003 | Verify All Cases view | Select All Cases on the FRA Landing Page. | All FRA cases accessible to the PM are displayed. |
| FRA-LP-004 | Verify category selection | Open the Initiative Category filter/dropdown and select New Product / Product Change, Corporate Action, Material Change in Process, NICRA and Other. | Cases belonging to the selected category are displayed. |
| FRA-LP-005 | Verify FRA cases are displayed under the correct status | Review cases in In Progress, Pending Endorsement, Refer Back, Endorsement by RFO and Completed statuses. | Each case is displayed under the status corresponding to its actual assessment status. |
| FRA-LP-006 | Verify FRA status counts | Compare the count shown for each status with the corresponding FRA cases displayed. | Each status count matches the applicable FRA records. |
| FRA-LP-007 | Verify FRA case search using an existing value | Search using an existing searchable value such as the relevant case/category field value. | The matching FRA case is displayed. |
| FRA-LP-008 | Verify FRA search with a non-existing value | Enter a value that does not exist in the FRA records. | No matching FRA record is displayed. |
| FRA-LP-009 | Verify FRA Landing Page filtering | Apply an available Landing Page filter. | Only FRA records matching the selected filter are displayed. |
| FRA-LP-010 | Verify clearing FRA filter | Apply a filter and then clear the filter. | The filter is removed and all applicable FRA records are displayed again. |
| FRA-LP-011 | Verify FRA Landing Page sorting | Sort a sortable column in ascending and descending order. | Records are displayed in the selected sort order. |
| FRA-LP-012 | Verify FRA Landing Page pagination and horizontal scrolling | Navigate through the available grid pages and scroll horizontally across the grid. | Records are displayed correctly without missing or duplicate records, and all configured columns are accessible. |
| FRA-LP-013 | Verify common case information | Review Status, Created By, Created Date, Last Updated Date and Completed Date for an existing FRA case. | Each common field displays the correct information for the selected case. |

# 2. NEW PRODUCT / PRODUCT CHANGE

### LANDING PAGE

| Test Case ID | Test Scenario | Test Steps | Expected Result |
|---|---|---|---|
| FRA-NP-001 | Verify New Product / Product Change cases are displayed | Select New Product / Product Change from Initiative Category. | New Product / Product Change cases are displayed. |
| FRA-NP-002 | Verify New Product / Product Change grid fields | Review the columns displayed for a New Product / Product Change case. | The grid displays Trigger Event, Programme Code, Programme Name, Product Manager, Business Head / Product Head, Business Line, CFCR RFO, Product Description & Scope, Applicable to – Islamic Variant and Applicable to – Sustainable Finance Variant, along with the applicable common fields. |
| FRA-NP-003 | Verify Programme Code search | Search for an existing Programme Code and then search for a non-existing Programme Code. | The matching case is displayed for the existing Programme Code, and no matching case is displayed for the non-existing Programme Code. |

### INITIATE RISK ASSESSMENT

| Test Case ID | Test Scenario | Test Steps | Expected Result |
|---|---|---|---|
| FRA-NP-004 | Verify New Product / Product Change fields are displayed | Select New Product / Product Change and open Initiate Risk Assessment. | The screen displays Trigger Event, Programme Code, Programme Name, Product Manager, Business Head / Product Head, Business Line, CFCR RFO, Product Description & Scope, Applicable to – Islamic Variant and Applicable to – Sustainable Finance Variant. |
| FRA-NP-005 | Verify Trigger Event / Driver selection | Open the Trigger Event / Driver dropdown and select a valid value. | Available values are displayed and the selected Trigger Event / Driver is retained correctly. |
| FRA-NP-006 | Verify mandatory validation for New Product / Product Change | Leave required fields blank and attempt to continue/submit the assessment. | Mandatory validation is displayed for the required fields and progression is prevented until the required information is entered. |
| FRA-NP-007 | Verify valid Programme Code format | Enter a valid Programme Code such as PPG-12345. | The Programme Code is accepted without a format validation error and is retained correctly. |
| FRA-NP-008 | Verify invalid Programme Code format | Enter Programme Code values that do not follow the configured format, such as a missing prefix, incorrect number of characters or invalid characters. | The invalid Programme Code is rejected and an appropriate validation message is displayed. |
| FRA-NP-009 | Verify Programme Name entry | Enter a valid Programme Name. | The Programme Name is accepted and retained correctly. |
| FRA-NP-010 | Verify Product Manager PSID population | Enter/select the applicable Product Manager information. | The corresponding Product Manager PSID is populated correctly based on the configured user information. |
| FRA-NP-011 | Verify Business Head / Product Head PSID population | Enter/select the applicable Business Head / Product Head. | The corresponding Business Head / Product Head PSID is populated correctly. |
| FRA-NP-012 | Verify Business Line selection | Select a valid Business Line. | The selected Business Line is accepted and retained correctly. |
| FRA-NP-013 | Verify CFCR RFO population | Complete the applicable Business Line information and review the CFCR RFO. | The applicable CFCR RFO is populated according to the configured CRHS logic. |
| FRA-NP-014 | Verify Product Description & Scope entry and mandatory validation | Enter valid text in Product Description & Scope, then repeat the test leaving the field blank and attempt to continue. | The entered Product Description & Scope is accepted and retained. When left blank, mandatory validation is displayed and progression is prevented. |
| FRA-NP-015 | Verify Product Description & Scope 5000-character limit | Enter a Product Description & Scope containing exactly 5000 characters. | The 5000-character value is accepted and retained without truncation. |
| FRA-NP-016 | Verify Product Description & Scope exceeding character limit | Attempt to enter more than 5000 characters in Product Description & Scope. | The system prevents entry beyond the configured 5000-character limit or displays the configured validation message. |
| FRA-NP-017 | Verify Applicable to – Islamic Variant selection | Select Applicable to – Islamic Variant. | The selection is retained and displayed correctly. |
| FRA-NP-018 | Verify Applicable to – Sustainable Finance Variant selection | Select Applicable to – Sustainable Finance Variant. | The selection is retained and displayed correctly. |
| FRA-NP-019 | Verify both Applicable to selections | Select both Applicable to – Islamic Variant and Applicable to – Sustainable Finance Variant. | Both selections are retained and displayed correctly. |
| FRA-NP-020 | Verify New Product / Product Change submission | Complete all mandatory New Product / Product Change information and submit the Initiative. | The assessment is created successfully and progresses to the next configured FRA stage. |

### DETAILS

| Test Case ID | Test Scenario | Test Steps | Expected Result |
|---|---|---|---|
| FRA-NP-021 | Verify New Product / Product Change Details | Open a submitted New Product / Product Change assessment and open the Details panel. | Details display Trigger Event, Programme Code, Programme Name, Product Manager, Business Head / Product Head, Business Line, CFCR RFO, Product Description & Scope, Applicable to – Islamic Variant and Applicable to – Sustainable Finance Variant. |
| FRA-NP-022 | Verify New Product / Product Change Details values | Compare the Details values with the values submitted during Initiate Risk Assessment. | All displayed New Product / Product Change values match the submitted assessment. |
| FRA-NP-023 | Verify Product Description & Scope Click to View | Select Click to View for Product Description & Scope in Details. | A popup opens and displays the complete Product Description & Scope without unintended truncation. |

### LANDING PAGE EXPORT

| Test Case ID | Test Scenario | Test Steps | Expected Result |
|---|---|---|---|
| FRA-NP-024 | Verify New Product / Product Change Landing Page Export availability | Select New Product / Product Change on the Landing Page and open Export. | Landing Page Export is available. |
| FRA-NP-025 | Verify New Product / Product Change export generation | Select Export and open the downloaded file. | The export file is generated, downloaded and opened successfully. |
| FRA-NP-026 | Verify New Product / Product Change exported fields | Review Trigger Event, Programme Code, Programme Name, Product Manager, Business Head / Product Head, Business Line, CFCR RFO, Product Description & Scope, Applicable to – Islamic Variant and Applicable to – Sustainable Finance Variant in the exported file. | Exported values match the corresponding Landing Page data. |
| FRA-NP-027 | Verify New Product / Product Change common exported fields | Review Status, Created By, Created Date, Last Updated Date and Completed Date in the exported file. | Common exported values match the Landing Page data. |
| FRA-NP-028 | Verify long Product Description & Scope in export | Export a case containing a long Product Description & Scope. | The complete Product Description & Scope is exported without unintended truncation. |
| FRA-NP-029 | Verify filtered New Product / Product Change export | Apply a filter to the New Product / Product Change Landing Page and select Export. | The exported file contains only records matching the applied filter. |
| FRA-NP-030 | Verify searched New Product / Product Change export | Search for a specific Programme Code/value and select Export. | The export reflects the applicable searched records. |
| FRA-NP-031 | Verify New Product / Product Change export accuracy | Compare the exported case information with the corresponding Landing Page data. | Exported data matches the Landing Page data. |

### WORKFLOW EXPORT

| Test Case ID | Test Scenario | Test Steps | Expected Result |
|---|---|---|---|
| FRA-NP-032 | Verify New Product / Product Change Workflow Export availability | Open a New Product / Product Change assessment and select Workflow Export. | Workflow Export is available. |
| FRA-NP-033 | Verify New Product / Product Change Workflow Export generation | Select Workflow Export and open the downloaded file. | Workflow Export is generated, downloaded and opened successfully. |
| FRA-NP-034 | Verify New Product / Product Change Workflow Export fields | Review Trigger Event, Programme Code, Programme Name, Product Manager, Business Head / Product Head, Business Line, CFCR RFO, Product Description & Scope, Applicable to – Islamic Variant and Applicable to – Sustainable Finance Variant. | Exported values match the assessment data. |
| FRA-NP-035 | Verify common Workflow Export fields | Review Case ID, Initiative Category, Status, Created By, Created Date, Last Updated Date and Completed Date. | Exported common values match the assessment data. |
| FRA-NP-036 | Verify long Product Description & Scope in Workflow Export | Export an assessment containing a long Product Description & Scope. | Complete Product Description & Scope is exported without unintended truncation. |
| FRA-NP-037 | Verify New Product / Product Change Workflow Export accuracy | Compare the assessment information with the Workflow Export. | Exported data matches the assessment data. |

# 3. MATERIAL CHANGE IN PROCESS

### LANDING PAGE

| Test Case ID | Test Scenario | Test Steps | Expected Result |
|---|---|---|---|
| FRA-MC-001 | Verify Material Change in Process cases are displayed | Select Material Change in Process from Initiative Category. | Material Change in Process cases are displayed. |
| FRA-MC-002 | Verify Material Change in Process grid fields | Review the columns displayed for a Material Change in Process case. | The grid displays Trigger Event / Driver, Process ID, Project Name, Process Description, Background of Process Change, Rationale for FRA, Accountable Executive or Key Stakeholder, Contact Point, Country Coverage, Business Function and CFCR RFO. |

### INITIATE RISK ASSESSMENT

| Test Case ID | Test Scenario | Test Steps | Expected Result |
|---|---|---|---|
| FRA-MC-003 | Verify Material Change in Process fields are displayed | Select Material Change in Process and open Initiate Risk Assessment. | All configured Material Change in Process fields are displayed. |
| FRA-MC-004 | Verify Trigger Event / Driver selection | Open Trigger Event / Driver and select an applicable value. | Available values are displayed and the selected value is retained correctly. |
| FRA-MC-005 | Verify Process ID mandatory validation | Leave Process ID blank and attempt to continue. | Mandatory validation is displayed and progression is prevented. |
| FRA-MC-006 | Verify Process ID entry | Enter a valid Process ID. | Process ID is accepted and retained correctly. |
| FRA-MC-007 | Verify Project Name entry | Enter a valid Project Name. | Project Name is accepted and retained correctly. |
| FRA-MC-008 | Verify Process Description mandatory validation | Leave Process Description blank and attempt to continue. | Mandatory validation is displayed and progression is prevented. |
| FRA-MC-009 | Verify Process Description character limit | Enter exactly 5000 characters in Process Description and then attempt to exceed the limit. | 5000 characters are accepted and retained; entry beyond the configured 5000-character limit is prevented or appropriately validated. |
| FRA-MC-010 | Verify Background of Process Change mandatory validation and character limit | Leave Background of Process Change blank and attempt to continue. Then enter exactly 5000 characters and attempt to exceed the limit. | Mandatory validation is displayed when blank. 5000 characters are accepted and entry beyond the configured limit is prevented or validated. |
| FRA-MC-011 | Verify Rationale for FRA mandatory validation and character limit | Leave Rationale for FRA blank and attempt to continue. Then enter exactly 5000 characters and attempt to exceed the limit. | Mandatory validation is displayed when blank. 5000 characters are accepted and entry beyond the configured limit is prevented or validated. |
| FRA-MC-012 | Verify Accountable Executive or Key Stakeholder selection | Search and select an applicable Accountable Executive or Key Stakeholder using the configured employee/bank ID field. | The selected user is accepted and retained correctly. |
| FRA-MC-013 | Verify Contact Point population | Enter/select the applicable user information for Contact Point. | Contact Point is populated according to the configured logic. |
| FRA-MC-014 | Verify Country Coverage selection | Select an applicable Country Coverage value. | The selected Country Coverage is retained correctly. |
| FRA-MC-015 | Verify Country Coverage maximum | Select countries up to the configured maximum and attempt to select one additional country. | The configured maximum is accepted and selection beyond the maximum is prevented or appropriately validated. |
| FRA-MC-016 | Verify Business Function selection | Select an applicable Business Function. | The selected Business Function is retained correctly. |
| FRA-MC-017 | Verify CFCR RFO population | Select the applicable Business Function and review CFCR RFO. | Applicable CFCR RFO is populated according to the configured CRHS logic. |
| FRA-MC-018 | Verify Material Change in Process submission | Complete all required Material Change in Process information and submit the Initiative. | The assessment is created successfully and progresses to the next configured FRA stage. |

### DETAILS

| Test Case ID | Test Scenario | Test Steps | Expected Result |
|---|---|---|---|
| FRA-MC-019 | Verify Material Change in Process Details | Open a Material Change in Process assessment and open Details. | Details display Trigger Event / Driver, Process ID, Project Name, Process Description, Background of Process Change, Rationale for FRA, Accountable Executive or Key Stakeholder, Contact Point, Country Coverage, Business Function and CFCR RFO. |
| FRA-MC-020 | Verify Material Change in Process Details values | Compare the Details values with the submitted assessment. | All Material Change in Process values match the submitted assessment. |
| FRA-MC-021 | Verify Process Description Click to View | Select Click to View for Process Description. | A popup opens and displays the complete Process Description without unintended truncation. |
| FRA-MC-022 | Verify Background of Process Change Click to View | Select Click to View for Background of Process Change. | A popup opens and displays the complete Background of Process Change without unintended truncation. |
| FRA-MC-023 | Verify Rationale for FRA Click to View | Select Click to View for Rationale for FRA. | A popup opens and displays the complete Rationale for FRA without unintended truncation. |
| FRA-MC-024 | Verify assessment activity/history | Open the assessment Details/Activity section. | Assessment activity/history is displayed correctly. |

### LANDING PAGE EXPORT

| Test Case ID | Test Scenario | Test Steps | Expected Result |
|---|---|---|---|
| FRA-MC-025 | Verify Material Change in Process Landing Page Export availability | Select Material Change in Process and open Export. | Landing Page Export is available. |
| FRA-MC-026 | Verify Material Change in Process export generation | Select Export and open the downloaded file. | Export file is generated, downloaded and opened successfully. |
| FRA-MC-027 | Verify Material Change in Process exported fields | Review Trigger Event / Driver, Process ID, Project Name, Process Description, Background of Process Change, Rationale for FRA, Accountable Executive or Key Stakeholder, Contact Point, Country Coverage, Business Function and CFCR RFO. | Exported values match the Landing Page data. |
| FRA-MC-028 | Verify common exported fields | Review Status, Created By, Created Date, Last Updated Date and Completed Date. | Common exported values match the Landing Page data. |
| FRA-MC-029 | Verify long-text export | Export a case containing long Process Description, Background of Process Change and Rationale for FRA. | Complete long-text values are exported without unintended truncation. |
| FRA-MC-030 | Verify filtered Material Change in Process export | Apply a filter and export the results. | Export contains only records corresponding to the applied filter. |
| FRA-MC-031 | Verify searched Material Change in Process export | Search for a Material Change in Process case and export. | Export reflects the applicable searched records. |
| FRA-MC-032 | Verify My Cases export | Select My Cases and export the displayed records. | Export contains the applicable My Cases records. |
| FRA-MC-033 | Verify All Cases export | Select All Cases and export the displayed records. | Export contains the applicable All Cases records. |
| FRA-MC-034 | Verify Material Change in Process export accuracy | Compare exported data with the corresponding Landing Page data. | Exported data matches the Landing Page data. |

### WORKFLOW EXPORT

| Test Case ID | Test Scenario | Test Steps | Expected Result |
|---|---|---|---|
| FRA-MC-035 | Verify Material Change in Process Workflow Export availability | Open a Material Change in Process assessment and select Workflow Export. | Workflow Export is available. |
| FRA-MC-036 | Verify Material Change in Process Workflow Export generation | Select Workflow Export and open the downloaded file. | Workflow Export is generated, downloaded and opened successfully. |
| FRA-MC-037 | Verify Material Change in Process Workflow Export fields | Review Trigger Event / Driver, Process ID, Project Name, Process Description, Background of Process Change, Rationale for FRA, Accountable Executive or Key Stakeholder, Contact Point, Country Coverage, Business Function and CFCR RFO. | Exported values match the assessment data. |
| FRA-MC-038 | Verify common Workflow Export fields | Review Case ID, Initiative Category, Status, Created By, Created Date, Last Updated Date and Completed Date. | Exported common fields match the assessment. |
| FRA-MC-039 | Verify Assessment information in Workflow Export | Review the Assessment information in the Workflow Export. | Assessment information matches the corresponding assessment data. |
| FRA-MC-040 | Verify Mitigation Plan in Workflow Export | Review the Mitigation Plan information in the Workflow Export. | Exported Mitigation Plan information matches the assessment. |
| FRA-MC-041 | Verify RFO Endorsement in Workflow Export | Review CFCR RFO, RFO/Coverage status, 4LOD, RFO endorsement status and applicable RFO comments in the Workflow Export. | Exported endorsement information matches the applicable assessment data. |
| FRA-MC-042 | Verify Refer Back information in Workflow Export | Export an assessment that has been referred back and review the workflow export. | Refer Back status and applicable comments are displayed correctly. |
| FRA-MC-043 | Verify long-text values in Workflow Export | Export an assessment containing long Process Description, Background of Process Change and Rationale for FRA. | Complete long-text values are exported without unintended truncation. |
| FRA-MC-044 | Verify Material Change in Process Workflow Export accuracy | Compare assessment information with the Workflow Export. | Exported data matches the assessment data. |

# 4. CORPORATE ACTION

### LANDING PAGE

| Test Case ID | Test Scenario | Test Steps | Expected Result |
|---|---|---|---|
| FRA-CA-001 | Verify Corporate Action cases are displayed | Select Corporate Action from Initiative Category. | Corporate Action cases are displayed. |
| FRA-CA-002 | Verify Corporate Action grid fields | Review the columns displayed for a Corporate Action case. | The grid displays Trigger Event, Project Name, Transaction, Rationale, Responsible Person, Accountable Executive, MT Sponsor, Business/Function and CFCR RFOs, along with applicable common fields. |

### INITIATE RISK ASSESSMENT

| Test Case ID | Test Scenario | Test Steps | Expected Result |
|---|---|---|---|
| FRA-CA-003 | Verify Corporate Action fields are displayed | Select Corporate Action and open Initiate Risk Assessment. | Trigger Event, Project Name, Transaction, Rationale, Responsible Person, Accountable Executive, MT Sponsor, Business/Function and CFCR RFOs are displayed. |
| FRA-CA-004 | Verify Trigger Event / Driver selection | Select a valid Trigger Event / Driver. | The selected value is retained correctly. |
| FRA-CA-005 | Verify Corporate Action mandatory validation | Leave required Corporate Action fields blank and attempt to continue/submit. | Mandatory validation is displayed and progression is prevented until required information is entered. |
| FRA-CA-006 | Verify Project Name entry | Enter a valid Project Name. | Project Name is accepted and retained correctly. |
| FRA-CA-007 | Verify Transaction entry and character limit | Enter valid Transaction text. Then enter exactly 5000 characters and attempt to exceed the limit. | Valid Transaction text and a 5000-character value are accepted and retained. Entry beyond the configured 5000-character limit is prevented or appropriately validated. |
| FRA-CA-008 | Verify Rationale entry and character limit | Enter valid Rationale text. Then enter exactly 5000 characters and attempt to exceed the limit. | Valid Rationale text and a 5000-character value are accepted and retained. Entry beyond the configured 5000-character limit is prevented or appropriately validated. |
| FRA-CA-009 | Verify Responsible Person PSID population | Select the applicable Responsible Person. | The corresponding Responsible Person PSID is populated correctly. |
| FRA-CA-010 | Verify Accountable Executive PSID population | Enter/select the applicable Accountable Executive PSID. | The corresponding Accountable Executive is populated correctly. |
| FRA-CA-011 | Verify MT Sponsor PSID population | Enter/select the applicable MT Sponsor PSID. | The corresponding MT Sponsor is populated correctly. |
| FRA-CA-012 | Verify multiple Business/Function selection | Select more than one valid Business/Function. | Multiple Business/Function values can be selected and are retained correctly. |
| FRA-CA-013 | Verify CFCR RFO population | Select the required Business/Function values and review CFCR RFOs. | Applicable CFCR RFOs are populated according to the configured CRHS logic. |
| FRA-CA-014 | Verify multiple CFCR RFOs | Use a Corporate Action case with multiple applicable RFOs. | All applicable CFCR RFOs are populated/displayed correctly. |
| FRA-CA-015 | Verify Corporate Action submission | Complete all required Corporate Action information and submit the Initiative. | The Corporate Action assessment is created successfully and progresses to the next configured stage. |

### DETAILS

| Test Case ID | Test Scenario | Test Steps | Expected Result |
|---|---|---|---|
| FRA-CA-016 | Verify Corporate Action Details | Open a Corporate Action assessment and open Details. | Details display Trigger Event, Project Name, Transaction, Rationale, Responsible Person, Accountable Executive, MT Sponsor, Business/Function and CFCR RFOs. |
| FRA-CA-017 | Verify Corporate Action Details values | Compare Details values with the submitted assessment. | All Corporate Action values match the submitted assessment. |
| FRA-CA-018 | Verify Transaction Click to View | Select Click to View for Transaction in Details. | A popup opens and displays the complete Transaction text without unintended truncation. |
| FRA-CA-019 | Verify Rationale Click to View | Select Click to View for Rationale in Details. | A popup opens and displays the complete Rationale text without unintended truncation. |

### LANDING PAGE EXPORT

| Test Case ID | Test Scenario | Test Steps | Expected Result |
|---|---|---|---|
| FRA-CA-020 | Verify Corporate Action Landing Page Export availability | Select Corporate Action and open Export. | Landing Page Export is available. |
| FRA-CA-021 | Verify Corporate Action export generation | Select Export and open the downloaded file. | Export file is generated, downloaded and opened successfully. |
| FRA-CA-022 | Verify Corporate Action exported fields | Review Trigger Event, Project Name, Transaction, Rationale, Responsible Person, Accountable Executive, MT Sponsor, Business/Function and CFCR RFOs. | Exported values match Landing Page data. |
| FRA-CA-023 | Verify common exported fields | Review Status, Created By, Created Date, Last Updated Date and Completed Date. | Common exported values match Landing Page data. |
| FRA-CA-024 | Verify long Transaction and Rationale export | Export a case containing long Transaction and Rationale values. | Complete Transaction and Rationale text is exported without unintended truncation. |
| FRA-CA-025 | Verify filtered Corporate Action export | Apply a filter and export. | Export contains only records matching the applied filter. |
| FRA-CA-026 | Verify searched Corporate Action export | Search for a specific Corporate Action record and export. | Export reflects the applicable searched records. |
| FRA-CA-027 | Verify Corporate Action export accuracy | Compare exported data with the Landing Page. | Exported Corporate Action data matches the Landing Page data. |

### WORKFLOW EXPORT

| Test Case ID | Test Scenario | Test Steps | Expected Result |
|---|---|---|---|
| FRA-CA-028 | Verify Corporate Action Workflow Export availability | Open a Corporate Action assessment and select Workflow Export. | Workflow Export is available. |
| FRA-CA-029 | Verify Corporate Action Workflow Export generation | Select Workflow Export and open the downloaded file. | Workflow Export is generated and opened successfully. |
| FRA-CA-030 | Verify Corporate Action Workflow Export fields | Review Trigger Event, Project Name, Transaction, Rationale, Responsible Person, Accountable Executive, MT Sponsor, Business/Function and CFCR RFOs. | Exported values match the workflow data. |
| FRA-CA-031 | Verify common Workflow Export fields | Review Case ID, Initiative Category, Status, Created By, Created Date, Last Updated Date and Completed Date. | Exported common values match the workflow data. |
| FRA-CA-032 | Verify Transaction Workflow Export | Export a case containing long Transaction text. | Complete Transaction text is exported without unintended truncation. |
| FRA-CA-033 | Verify Rationale Workflow Export | Export a case containing long Rationale text. | Complete Rationale text is exported without unintended truncation. |
| FRA-CA-034 | Verify Corporate Action Workflow Export accuracy | Compare workflow information with the exported file. | Exported data matches the Corporate Action workflow data. |

# 5. NICRA

### LANDING PAGE

| Test Case ID | Test Scenario | Test Steps | Expected Result |
|---|---|---|---|
| FRA-NICRA-001 | Verify NICRA cases are displayed | Select NICRA from Initiative Category. | NICRA cases are displayed. |
| FRA-NICRA-002 | Verify NICRA grid fields | Review the columns displayed for a NICRA case. | The grid displays Trigger Event, New Initiative Name, New Initiative Summary, First Line, Senior Manager / Group Business Head, Country Coverage, Business/Function and CFCR RFOs, along with applicable common fields. |

### INITIATE RISK ASSESSMENT

| Test Case ID | Test Scenario | Test Steps | Expected Result |
|---|---|---|---|
| FRA-NICRA-003 | Verify NICRA fields are displayed | Select NICRA and open Initiate Risk Assessment. | Trigger Event, New Initiative Name, New Initiative Summary, First Line, Senior Manager / Group Business Head, Country Coverage, Business/Function and CFCR RFOs are displayed. |
| FRA-NICRA-004 | Verify Trigger Event / Driver selection | Select a valid Trigger Event / Driver. | The selected value is retained correctly. |
| FRA-NICRA-005 | Verify NICRA mandatory validation | Leave required NICRA fields blank and attempt to continue. | Mandatory validation is displayed and progression is prevented until the required information is entered. |
| FRA-NICRA-006 | Verify New Initiative Name entry | Enter a valid New Initiative Name. | New Initiative Name is accepted and retained correctly. |
| FRA-NICRA-007 | Verify New Initiative Summary entry and character limit | Enter valid New Initiative Summary text. Then enter exactly 5000 characters and attempt to exceed the limit. | The valid and 5000-character values are accepted and retained. Entry beyond the configured 5000-character limit is prevented or appropriately validated. |
| FRA-NICRA-008 | Verify First Line PSID population | Review the First Line value populated for the current user. | The corresponding First Line PSID is auto-populated based on the current user. |
| FRA-NICRA-009 | Verify Senior Manager / Group Business Head PSID population | Enter/select the applicable Senior Manager / Group Business Head. | The corresponding user is populated correctly. |
| FRA-NICRA-010 | Verify Country Coverage maximum | Select five countries and attempt to select a sixth country. | Five countries can be selected and selection beyond five is prevented or appropriately validated. |
| FRA-NICRA-011 | Verify multiple Business/Function selection | Select multiple Business/Function values. | Multiple Business/Function values are accepted and retained correctly. |
| FRA-NICRA-012 | Verify CFCR RFO population | Select the required Business/Function values and review CFCR RFOs. | Applicable CFCR RFOs are populated according to the configured CRHS logic. |
| FRA-NICRA-013 | Verify multiple CFCR RFOs | Use a NICRA case with multiple applicable RFOs. | All applicable CFCR RFOs are populated/displayed correctly. |
| FRA-NICRA-014 | Verify NICRA submission | Complete all mandatory NICRA fields and submit the Initiative. | The NICRA assessment is created successfully and progresses to the next configured stage. |

### DETAILS

| Test Case ID | Test Scenario | Test Steps | Expected Result |
|---|---|---|---|
| FRA-NICRA-015 | Verify NICRA Details | Open a NICRA assessment and open Details. | Details display Trigger Event, New Initiative Name, New Initiative Summary, First Line, Senior Manager / Group Business Head, Country Coverage, Business/Function and CFCR RFOs. |
| FRA-NICRA-016 | Verify NICRA Details values | Compare the Details values with the submitted assessment. | All NICRA values match the submitted assessment. |
| FRA-NICRA-017 | Verify New Initiative Summary Click to View | Select Click to View for New Initiative Summary in Details. | A popup opens and displays the complete New Initiative Summary without unintended truncation. |
| FRA-NICRA-018 | Verify common Details information | Review Case ID, Initiative Category, Status, Created By, Created Date, Last Updated Date and Completed Date. | Common Details information is displayed correctly. |

### LANDING PAGE EXPORT

| Test Case ID | Test Scenario | Test Steps | Expected Result |
|---|---|---|---|
| FRA-NICRA-019 | Verify NICRA Landing Page Export availability | Select NICRA and open Export. | Landing Page Export is available. |
| FRA-NICRA-020 | Verify NICRA export generation | Select Export and open the downloaded file. | Export file is generated, downloaded and opened successfully. |
| FRA-NICRA-021 | Verify NICRA exported fields | Review Trigger Event, New Initiative Name, New Initiative Summary, First Line, Senior Manager / Group Business Head, Country Coverage, Business/Function and CFCR RFOs. | Exported values match Landing Page data. |
| FRA-NICRA-022 | Verify common exported fields | Review Status, Created By, Created Date, Last Updated Date and Completed Date. | Common exported values match Landing Page data. |
| FRA-NICRA-023 | Verify New Initiative Summary export | Export a case containing a long New Initiative Summary. | Complete New Initiative Summary is exported without unintended truncation. |
| FRA-NICRA-024 | Verify filtered NICRA export | Apply a filter and export. | Export contains records corresponding to the applied filter. |
| FRA-NICRA-025 | Verify searched NICRA export | Search for a NICRA case and export. | Export reflects the applicable searched records. |
| FRA-NICRA-026 | Verify NICRA export accuracy | Compare exported data with the Landing Page data. | Exported NICRA data matches the Landing Page data. |

### WORKFLOW EXPORT

| Test Case ID | Test Scenario | Test Steps | Expected Result |
|---|---|---|---|
| FRA-NICRA-027 | Verify NICRA Workflow Export availability | Open a NICRA assessment and select Workflow Export. | Workflow Export is available. |
| FRA-NICRA-028 | Verify NICRA Workflow Export generation | Select Workflow Export and open the downloaded file. | Workflow Export is generated and opened successfully. |
| FRA-NICRA-029 | Verify NICRA Workflow Export fields | Review Trigger Event, New Initiative Name, New Initiative Summary, First Line, Senior Manager / Group Business Head, Country Coverage, Business/Function and CFCR RFOs. | Exported values match the workflow data. |
| FRA-NICRA-030 | Verify common Workflow Export fields | Review Case ID, Initiative Category, Status, Created By, Created Date, Last Updated Date and Completed Date. | Common exported values match the workflow data. |
| FRA-NICRA-031 | Verify New Initiative Summary Workflow Export | Export an assessment containing a long New Initiative Summary. | Complete New Initiative Summary is exported without unintended truncation. |
| FRA-NICRA-032 | Verify NICRA Workflow Export accuracy | Compare workflow information with the exported file. | Exported NICRA data matches the workflow data. |

# 6. OTHER

### LANDING PAGE

| Test Case ID | Test Scenario | Test Steps | Expected Result |
|---|---|---|---|
| FRA-OT-001 | Verify Other cases are displayed | Select Other from Initiative Category. | Other cases are displayed. |
| FRA-OT-002 | Verify Other grid fields | Review the columns displayed for an Other case. | The grid displays Trigger Event, New Initiative Name, New Initiative Summary, First Line, Approver, Country Coverage, Business/Function and CFCR RFOs, along with applicable common fields. |

### INITIATE RISK ASSESSMENT

| Test Case ID | Test Scenario | Test Steps | Expected Result |
|---|---|---|---|
| FRA-OT-003 | Verify Other fields are displayed | Select Other and open Initiate Risk Assessment. | Trigger Event, New Initiative Name, New Initiative Summary, First Line, Approver, Country Coverage, Business/Function and CFCR RFOs are displayed. |
| FRA-OT-004 | Verify Trigger Event / Driver selection | Select a valid Trigger Event / Driver. | The selected value is retained correctly. |
| FRA-OT-005 | Verify Other mandatory validation | Leave required Other fields blank and attempt to continue/submit. | Mandatory validation is displayed and progression is prevented until required information is entered. |
| FRA-OT-006 | Verify New Initiative Name entry | Enter a valid New Initiative Name. | New Initiative Name is accepted and retained correctly. |
| FRA-OT-007 | Verify New Initiative Summary entry and character limit | Enter valid New Initiative Summary text. Then enter exactly 5000 characters and attempt to exceed the limit. | Valid and 5000-character values are accepted and retained. Entry beyond the configured 5000-character limit is prevented or appropriately validated. |
| FRA-OT-008 | Verify First Line PSID population | Review the First Line populated for the current user. | The corresponding First Line PSID is auto-populated correctly. |
| FRA-OT-009 | Verify Approver PSID population | Enter/select the applicable PSID for Approver. | The corresponding Approver is populated correctly. |
| FRA-OT-010 | Verify Country Coverage selection and maximum | Select countries up to the configured maximum and attempt to select one additional country. | Allowed countries are retained correctly and selection beyond the configured maximum is prevented or appropriately validated. |
| FRA-OT-011 | Verify multiple Business/Function selection | Select multiple Business/Function values. | Multiple Business/Function values can be selected and retained correctly. |
| FRA-OT-012 | Verify CFCR RFO population | Select the required Business/Function values and review CFCR RFOs. | Applicable CFCR RFOs are populated according to the configured CRHS logic. |
| FRA-OT-013 | Verify multiple CFCR RFOs | Use an Other case with multiple applicable RFOs. | All applicable CFCR RFOs are populated/displayed correctly. |
| FRA-OT-014 | Verify Other submission | Complete all mandatory Other information and submit the Initiative. | The Other assessment is created successfully and progresses to the next configured stage. |

### DETAILS

| Test Case ID | Test Scenario | Test Steps | Expected Result |
|---|---|---|---|
| FRA-OT-015 | Verify Other Details | Open an Other assessment and open Details. | Details display Trigger Event, New Initiative Name, New Initiative Summary, First Line, Approver, Country Coverage, Business/Function and CFCR RFOs. |
| FRA-OT-016 | Verify Other Details values | Compare Details values with the submitted assessment. | All displayed Other values match the submitted assessment. |
| FRA-OT-017 | Verify New Initiative Summary in Details | Select Click to View for New Initiative Summary. | A popup opens and displays the complete New Initiative Summary without unintended truncation. |
| FRA-OT-018 | Verify common Details information | Review Case ID, Initiative Category, Status, Created By, Created Date, Last Updated Date and Completed Date. | Common Details information is displayed correctly. |

### LANDING PAGE EXPORT

| Test Case ID | Test Scenario | Test Steps | Expected Result |
|---|---|---|---|
| FRA-OT-019 | Verify Other Landing Page Export availability | Select Other and open Export. | Landing Page Export is available. |
| FRA-OT-020 | Verify Other export generation | Select Export and open the downloaded file. | Export file is generated, downloaded and opened successfully. |
| FRA-OT-021 | Verify Other exported fields | Review Trigger Event, New Initiative Name, New Initiative Summary, First Line, Approver, Country Coverage, Business/Function and CFCR RFOs. | Exported values match Landing Page data. |
| FRA-OT-022 | Verify common exported fields | Review Status, Created By, Created Date, Last Updated Date and Completed Date. | Common exported values match Landing Page data. |
| FRA-OT-023 | Verify New Initiative Summary export | Export a case containing a long New Initiative Summary. | Complete New Initiative Summary is exported without unintended truncation. |
| FRA-OT-024 | Verify filtered Other export | Apply a filter and export. | Export contains only records matching the applied filter. |
| FRA-OT-025 | Verify searched Other export | Search for an Other case and export. | Export reflects the applicable searched records. |
| FRA-OT-026 | Verify Other export accuracy | Compare exported data with Landing Page data. | Exported Other data matches the Landing Page. |

### WORKFLOW EXPORT

| Test Case ID | Test Scenario | Test Steps | Expected Result |
|---|---|---|---|
| FRA-OT-027 | Verify Other Workflow Export availability | Open an Other assessment and select Workflow Export. | Workflow Export is available. |
| FRA-OT-028 | Verify Other Workflow Export generation | Select Workflow Export and open the downloaded file. | Workflow Export is generated and opened successfully. |
| FRA-OT-029 | Verify Other Workflow Export fields | Review Trigger Event, New Initiative Name, New Initiative Summary, First Line, Approver, Country Coverage, Business/Function and CFCR RFOs. | Exported values match the workflow data. |
| FRA-OT-030 | Verify common Workflow Export fields | Review Case ID, Initiative Category, Status, Created By, Created Date, Last Updated Date and Completed Date. | Common exported values match the workflow data. |
| FRA-OT-031 | Verify New Initiative Summary Workflow Export | Export an assessment containing a long New Initiative Summary. | Complete New Initiative Summary is exported without unintended truncation. |
| FRA-OT-032 | Verify Other Workflow Export accuracy | Compare workflow information with the exported file. | Exported Other data matches the workflow data. |

This is the **same four-column structure as your screenshot**, applied to all the FRA test cases in the file. 

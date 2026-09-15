Yes. **This is the structure we should use now**:

For each category:

1. **Landing Page**
2. **Initiate Risk Assessment**
3. **Details Panel**
4. **Landing Page Export**
5. **Workflow Export**

**No separate Common Functionality sheet. No Risk Assessment / Mitigation / Endorsement workflow cases**, since your senior asked for only the relevant areas.

And I’m making the cases **UAT-user-readable** now: the tester can execute them without having to refer back to the BRD.

---

# 1. NEW PRODUCT / PRODUCT CHANGE

## A. Landing Page

| Test Case ID | Test Scenario | Test Steps | Expected Result |
|---|---|---|---|
| PM-NP-LP-001 | Verify New Product / Product Change cases are displayed | Login as PM, open the COI Landing Page, select **New Product / Product Change** from Initiative Category. | Only New Product / Product Change cases are displayed in the grid. |
| PM-NP-LP-002 | Verify New Product / Product Change grid fields | Review the columns displayed for a New Product / Product Change case. | The grid displays **Programme code, Programme Name, Product manager, Business head / Product head, Business line, CFCR RFO, Product description & scope, Applicable to – Islamic variant and Applicable to – Sustainable finance variant**. |
| PM-NP-LP-003 | Verify New Product / Product Change status display | Open cases having **In Progress, Pending Endorsement, Refer Back, Endorsement by RFO and Completed** statuses. | Each case is displayed with the status that matches its actual assessment status. |
| PM-NP-LP-004 | Verify New Product / Product Change status counts | Select each status tile and count the New Product / Product Change cases displayed in the grid. | The number of cases displayed matches the corresponding status count. |
| PM-NP-LP-005 | Verify search using Programme code | Enter an existing **Programme code** in the Landing Page search field. | The case associated with the entered Programme code is displayed. |
| PM-NP-LP-006 | Verify search with non-existing value | Enter a Programme code/value that does not exist. | No matching New Product / Product Change case is displayed. |
| PM-NP-LP-007 | Verify filtering of New Product / Product Change cases | Apply an available grid filter to the New Product / Product Change cases. | Only records matching the selected filter criteria are displayed. |
| PM-NP-LP-008 | Verify clearing of applied filter | Apply a filter and select **Clear/Reset**. | The filter is removed and all applicable New Product / Product Change records are displayed again. |
| PM-NP-LP-009 | Verify sorting of New Product / Product Change records | Sort a sortable column first in ascending order and then in descending order. | Records are displayed correctly according to the selected sort order. |
| PM-NP-LP-010 | Verify pagination | Navigate through the available pages of New Product / Product Change records. | The correct records are displayed on each page without missing or duplicated records. |
| PM-NP-LP-011 | Verify horizontal scrolling | Scroll horizontally across the New Product / Product Change grid. | All configured columns, including columns towards the right side of the grid, can be viewed. |
| PM-NP-LP-012 | Verify common case information | Review **Status, Created By, Created Date, Last Updated Date and Completed Date** for an existing case. | Each field displays the correct information for the selected case. |
| PM-NP-LP-013 | Verify Programme code display | Open a case containing a valid Programme code. | Programme code is displayed correctly in the configured **PPG-XXXXX** format. |
| PM-NP-LP-014 | Verify Product description & scope Click to View | Select **Click to View** for Product description & scope. | A popup opens showing the Product description & scope. |
| PM-NP-LP-015 | Verify complete Product description & scope | Enter/use a case containing a long Product description & scope and select **Click to View**. | The popup displays the complete Product description & scope without unintended truncation. |
| PM-NP-LP-016 | Verify Landing Page data against submitted assessment | Open a submitted New Product / Product Change case and compare the Landing Page values with the values entered during initiation. | **Programme code, Programme Name, Product manager, Business head / Product head, Business line, CFCR RFO, Product description & scope, Applicable to – Islamic variant and Applicable to – Sustainable finance variant** match the submitted values. |

## B. Initiate Risk Assessment

| Test Case ID | Test Scenario | Test Steps | Expected Result |
|---|---|---|---|
| PM-NP-INIT-001 | Verify New Product / Product Change fields are displayed | Login as PM, open COI, select **New Product / Product Change**, and open **Initiate Risk Assessment**. | The Initiative screen displays **Programme code, Programme Name, Product manager, Business head / Product head, Business line, CFCR RFO, Product description & scope, Applicable to – Islamic variant and Applicable to – Sustainable finance variant**. |
| PM-NP-INIT-002 | Verify mandatory fields prevent submission | Leave **Programme code, Programme Name, Product manager, Business head / Product head, Business line, CFCR RFO and Product description & scope** blank and attempt to continue/submit. | Mandatory validation is displayed for the required fields and the assessment cannot proceed until they are completed. |
| PM-NP-INIT-003 | Verify Programme code accepts valid format | Enter a valid Programme code such as **PPG-12345**. | The Programme code is accepted and no format validation error is displayed. |
| PM-NP-INIT-004 | Verify Programme code rejects invalid format | Enter Programme code values that do not follow the configured format, such as missing the required prefix, incorrect number of characters or invalid characters. | Invalid Programme code is rejected and an appropriate validation message is displayed. |
| PM-NP-INIT-005 | Verify Product manager PSID population | Enter/select the PSID for the Product manager according to the configured user-selection mechanism. | The corresponding Product manager is populated correctly. |
| PM-NP-INIT-006 | Verify Business head / Product head PSID population | Enter/select the PSID for Business head / Product head. | The corresponding Business head / Product head is populated correctly. |
| PM-NP-INIT-007 | Verify CFCR RFO population | Complete the applicable business information and review the CFCR RFO field. | CFCR RFO is populated according to the configured CRHS logic. |
| PM-NP-INIT-008 | Verify Business line selection | Open the Business line field and select a valid Business line. | The selected Business line is accepted and remains displayed. |
| PM-NP-INIT-009 | Verify Product description & scope mandatory behaviour | Enter Product description & scope and continue. Repeat the test without entering Product description & scope. | The entered description is accepted. When left blank, mandatory validation prevents progression. |
| PM-NP-INIT-010 | Verify Applicable to – Islamic variant | Select **Applicable to – Islamic variant**. | The Islamic variant selection is retained correctly. |
| PM-NP-INIT-011 | Verify Applicable to – Sustainable finance variant | Select **Applicable to – Sustainable finance variant**. | The Sustainable finance variant selection is retained correctly. |
| PM-NP-INIT-012 | Verify both Applicable to selections | Select both **Applicable to – Islamic variant** and **Applicable to – Sustainable finance variant**. | Both selections are retained and displayed correctly. |
| PM-NP-INIT-013 | Verify New Product / Product Change submission | Enter valid values in all mandatory fields, select applicable Applicable to values and submit the Initiative. | The assessment is created successfully and progresses to the next configured stage. |

## C. Details Panel

| Test Case ID | Test Scenario | Test Steps | Expected Result |
|---|---|---|---|
| PM-NP-DET-001 | Verify New Product / Product Change Details | Open a New Product / Product Change assessment and open the **Details** panel. | Details displays **Programme code, Programme Name, Product manager, Business head / Product head, Business line, CFCR RFO, Product description & scope, Applicable to – Islamic variant and Applicable to – Sustainable finance variant**. |
| PM-NP-DET-002 | Verify Details values against submitted information | Compare each displayed category field with the values submitted during Initiative. | All displayed values match the submitted assessment. |
| PM-NP-DET-003 | Verify Product description & scope in Details | Select **Click to View** for Product description & scope in the Details panel. | A popup opens and displays the complete Product description & scope without unintended truncation. |
| PM-NP-DET-004 | Verify common Details information | Review **Case ID, Initiative Category, Status, Created By, Created Date, Last Updated Date and Completed Date**. | All common Details information is displayed correctly. |

## D. Landing Page Export

| Test Case ID | Test Scenario | Test Steps | Expected Result |
|---|---|---|---|
| PM-NP-LPE-001 | Verify Landing Page Export is available | Select **New Product / Product Change** on the Landing Page and open the Export option. | Landing Page Export is available. |
| PM-NP-LPE-002 | Verify New Product / Product Change export generation | Select Export and open the downloaded file. | The export file is generated, downloaded and opened successfully. |
| PM-NP-LPE-003 | Verify New Product / Product Change fields in export | Review **Programme code, Programme Name, Product manager, Business head / Product head, Business line, CFCR RFO, Product description & scope, Applicable to – Islamic variant and Applicable to – Sustainable finance variant**. | All exported category fields match the Landing Page values. |
| PM-NP-LPE-004 | Verify common fields in export | Review **Status, Created By, Created Date, Last Updated Date and Completed Date** in the exported file. | Common fields match the Landing Page values. |
| PM-NP-LPE-005 | Verify long Product description & scope in export | Export a case containing a long Product description & scope. | The complete Product description & scope is present in the export without unintended truncation. |
| PM-NP-LPE-006 | Verify filtered New Product / Product Change export | Apply a filter to the Landing Page and select Export. | The exported file contains only records matching the applied filter. |
| PM-NP-LPE-007 | Verify searched New Product / Product Change export | Search for a specific Programme code/value and select Export. | The export reflects the applicable searched records. |
| PM-NP-LPE-008 | Verify Landing Page export accuracy | Compare the exported case information with the Landing Page. | Exported data matches the corresponding Landing Page data. |

## E. Workflow Export

| Test Case ID | Test Scenario | Test Steps | Expected Result |
|---|---|---|---|
| PM-NP-WFE-001 | Verify Workflow Export is available | Open a New Product / Product Change assessment and select Workflow Export. | Workflow Export option is available. |
| PM-NP-WFE-002 | Verify Workflow Export generation | Select Workflow Export and open the downloaded file. | Workflow Export is generated, downloaded and opened successfully. |
| PM-NP-WFE-003 | Verify New Product / Product Change fields in Workflow Export | Review **Programme code, Programme Name, Product manager, Business head / Product head, Business line, CFCR RFO, Product description & scope, Applicable to – Islamic variant and Applicable to – Sustainable finance variant**. | Exported values match the assessment data. |
| PM-NP-WFE-004 | Verify common fields in Workflow Export | Review **Case ID, Initiative Category, Status, Created By, Created Date, Last Updated Date and Completed Date**. | Exported common fields match the assessment. |
| PM-NP-WFE-005 | Verify long Product description & scope in Workflow Export | Export an assessment containing a long Product description & scope. | Complete Product description & scope is exported without unintended truncation. |
| PM-NP-WFE-006 | Verify Workflow Export accuracy | Compare the New Product / Product Change assessment with the exported file. | Exported data matches the corresponding assessment data. |

---

# 2. CORPORATE ACTION

## A. Landing Page

| Test Case ID | Test Scenario | Test Steps | Expected Result |
|---|---|---|---|
| PM-CA-LP-001 | Verify Corporate Action cases are displayed | Open the COI Landing Page and select **Corporate Action** from Initiative Category. | Corporate Action cases are displayed in the grid. |
| PM-CA-LP-002 | Verify Corporate Action grid fields | Review the columns displayed for a Corporate Action case. | The grid displays **Project Name, Transaction, Rationale, Responsible Person, Accountable Executive, MT Sponsor, Business/Function and CFCR RFOs**. |
| PM-CA-LP-003 | Verify Corporate Action status display | Review Corporate Action cases in **In Progress, Pending Endorsement, Refer Back, Endorsement by RFO and Completed** statuses. | Each case is displayed under its correct status. |
| PM-CA-LP-004 | Verify Corporate Action status counts | Compare the number of Corporate Action cases shown for each status with the corresponding status count. | Each status count matches the applicable Corporate Action records. |
| PM-CA-LP-005 | Verify Corporate Action search | Search using an existing Project Name or other configured searchable value. | The matching Corporate Action case is displayed. |
| PM-CA-LP-006 | Verify Corporate Action search with non-existing value | Enter a value that does not exist. | No matching Corporate Action record is displayed. |
| PM-CA-LP-007 | Verify Corporate Action filtering | Apply an available grid filter. | Only Corporate Action records matching the filter are displayed. |
| PM-CA-LP-008 | Verify clearing Corporate Action filter | Clear the applied filter. | All applicable Corporate Action records are restored. |
| PM-CA-LP-009 | Verify Corporate Action sorting | Sort a sortable column in ascending and descending order. | Records are displayed in the selected sort order. |
| PM-CA-LP-010 | Verify Corporate Action pagination and scrolling | Navigate through grid pages and scroll horizontally. | Correct records are displayed and all configured columns are accessible. |
| PM-CA-LP-011 | Verify Corporate Action common fields | Review **Status, Created By, Created Date, Last Updated Date and Completed Date**. | Common fields display the correct case information. |
| PM-CA-LP-012 | Verify multiple Business/Function values | Open a Corporate Action case created with multiple Business/Function selections. | All selected Business/Function values are displayed correctly. |
| PM-CA-LP-013 | Verify multiple CFCR RFOs | Open a Corporate Action case with multiple CFCR RFOs. | All applicable CFCR RFOs are displayed correctly. |
| PM-CA-LP-014 | Verify Transaction Click to View | Select **Click to View** for Transaction. | Transaction popup opens successfully. |
| PM-CA-LP-015 | Verify complete Transaction text | Review a Transaction containing lengthy text in the popup. | Complete Transaction text is displayed without unintended truncation. |
| PM-CA-LP-016 | Verify Rationale Click to View | Select **Click to View** for Rationale. | Rationale popup opens successfully. |
| PM-CA-LP-017 | Verify complete Rationale text | Review a Rationale containing lengthy text in the popup. | Complete Rationale text is displayed without unintended truncation. |
| PM-CA-LP-018 | Verify Corporate Action data accuracy | Compare **Project Name, Transaction, Rationale, Responsible Person, Accountable Executive, MT Sponsor, Business/Function and CFCR RFOs** with the submitted assessment. | All Corporate Action values match the submitted assessment. |

## B. Initiate Risk Assessment

| Test Case ID | Test Scenario | Test Steps | Expected Result |
|---|---|---|---|
| PM-CA-INIT-001 | Verify Corporate Action fields are displayed | Select **Corporate Action** and open Initiate Risk Assessment. | The screen displays **Project Name, Transaction, Rationale, Responsible Person, Accountable Executive, MT Sponsor, Business/Function and CFCR RFOs**. |
| PM-CA-INIT-002 | Verify Corporate Action mandatory validation | Leave required Corporate Action fields blank and attempt to continue. | Mandatory validation is displayed and progression is prevented until required information is entered. |
| PM-CA-INIT-003 | Verify Project Name entry | Enter a valid Project Name. | Project Name is accepted and retained correctly. |
| PM-CA-INIT-004 | Verify Transaction entry | Enter a valid Transaction description. | Transaction is accepted and retained correctly. |
| PM-CA-INIT-005 | Verify Rationale entry | Enter a valid Rationale. | Rationale is accepted and retained correctly. |
| PM-CA-INIT-006 | Verify Responsible Person PSID | Enter/select the PSID for Responsible Person. | The corresponding Responsible Person is populated correctly. |
| PM-CA-INIT-007 | Verify Accountable Executive PSID | Enter/select the PSID for Accountable Executive. | The corresponding Accountable Executive is populated correctly. |
| PM-CA-INIT-008 | Verify MT Sponsor PSID | Enter/select the PSID for MT Sponsor. | The corresponding MT Sponsor is populated correctly. |
| PM-CA-INIT-009 | Verify multiple Business/Function selection | Select more than one valid Business/Function. | Multiple Business/Function values can be selected and are retained correctly. |
| PM-CA-INIT-010 | Verify CFCR RFO population | Complete the applicable Business/Function selections and review CFCR RFOs. | Applicable CFCR RFOs are populated according to the configured CRHS logic. |
| PM-CA-INIT-011 | Verify multiple CFCR RFOs | Use a Corporate Action requiring multiple RFOs and review the CFCR RFO field. | All applicable CFCR RFOs are populated/displayed correctly. |
| PM-CA-INIT-012 | Verify Corporate Action submission | Complete all required Corporate Action information and submit the Initiative. | The Corporate Action assessment is created successfully and progresses to the next configured stage. |

## C. Details Panel

| Test Case ID | Test Scenario | Test Steps | Expected Result |
|---|---|---|---|
| PM-CA-DET-001 | Verify Corporate Action Details | Open a Corporate Action assessment and open Details. | Details displays **Project Name, Transaction, Rationale, Responsible Person, Accountable Executive, MT Sponsor, Business/Function and CFCR RFOs**. |
| PM-CA-DET-002 | Verify Corporate Action Details values | Compare the Details values with the submitted Initiative. | All Corporate Action values match the submitted assessment. |
| PM-CA-DET-003 | Verify Transaction in Details | Select **Click to View** for Transaction. | Transaction popup opens and displays the complete Transaction text. |
| PM-CA-DET-004 | Verify Rationale in Details | Select **Click to View** for Rationale. | Rationale popup opens and displays the complete Rationale text. |
| PM-CA-DET-005 | Verify common Details information | Review **Case ID, Initiative Category, Status, Created By, Created Date, Last Updated Date and Completed Date**. | Common Details information is displayed correctly. |

## D. Landing Page Export

| Test Case ID | Test Scenario | Test Steps | Expected Result |
|---|---|---|---|
| PM-CA-LPE-001 | Verify Corporate Action Landing Page Export | Select Corporate Action and open Export. | Landing Page Export is available. |
| PM-CA-LPE-002 | Verify Corporate Action export generation | Export the Corporate Action data and open the downloaded file. | File is generated, downloaded and opened successfully. |
| PM-CA-LPE-003 | Verify Corporate Action exported fields | Review **Project Name, Transaction, Rationale, Responsible Person, Accountable Executive, MT Sponsor, Business/Function and CFCR RFOs**. | All exported values match Landing Page data. |
| PM-CA-LPE-004 | Verify common exported fields | Review **Status, Created By, Created Date, Last Updated Date and Completed Date**. | Common exported values match Landing Page data. |
| PM-CA-LPE-005 | Verify Transaction export | Export a case containing a long Transaction. | Complete Transaction text is exported without unintended truncation. |
| PM-CA-LPE-006 | Verify Rationale export | Export a case containing a long Rationale. | Complete Rationale text is exported without unintended truncation. |
| PM-CA-LPE-007 | Verify filtered Corporate Action export | Apply a filter and export. | Export contains only records matching the applied filter. |
| PM-CA-LPE-008 | Verify searched Corporate Action export | Search for a specific Corporate Action record and export. | Export reflects the applicable searched records. |
| PM-CA-LPE-009 | Verify Corporate Action export accuracy | Compare exported data with the Landing Page. | Exported Corporate Action data matches the Landing Page. |

## E. Workflow Export

| Test Case ID | Test Scenario | Test Steps | Expected Result |
|---|---|---|---|
| PM-CA-WFE-001 | Verify Corporate Action Workflow Export | Open a Corporate Action assessment and select Workflow Export. | Workflow Export is available. |
| PM-CA-WFE-002 | Verify Corporate Action Workflow Export generation | Select Export and open the downloaded file. | Workflow Export is generated and opened successfully. |
| PM-CA-WFE-003 | Verify Corporate Action Workflow Export fields | Review **Project Name, Transaction, Rationale, Responsible Person, Accountable Executive, MT Sponsor, Business/Function and CFCR RFOs**. | Exported values match workflow data. |
| PM-CA-WFE-004 | Verify common Workflow Export fields | Review **Case ID, Initiative Category, Status, Created By, Created Date, Last Updated Date and Completed Date**. | Exported common values match workflow data. |
| PM-CA-WFE-005 | Verify Transaction Workflow Export | Export a case containing long Transaction text. | Complete Transaction text is exported without unintended truncation. |
| PM-CA-WFE-006 | Verify Rationale Workflow Export | Export a case containing long Rationale text. | Complete Rationale text is exported without unintended truncation. |
| PM-CA-WFE-007 | Verify Corporate Action Workflow Export accuracy | Compare workflow information with the exported file. | Exported data matches the Corporate Action workflow data. |

---

# 3. NICRA

## A. Landing Page

| Test Case ID | Test Scenario | Test Steps | Expected Result |
|---|---|---|---|
| PM-NICRA-LP-001 | Verify NICRA cases are displayed | Open COI Landing Page and select **NICRA**. | NICRA cases are displayed in the grid. |
| PM-NICRA-LP-002 | Verify NICRA grid fields | Review the NICRA grid columns. | The grid displays **New Initiative Name, New Initiative Summary, First Line, Senior Manager / Group Business Head, Country Coverage, Business/Function and CFCR RFOs**. |
| PM-NICRA-LP-003 | Verify NICRA status display | Review NICRA cases across **In Progress, Pending Endorsement, Refer Back, Endorsement by RFO and Completed**. | Each case is displayed under its correct status. |
| PM-NICRA-LP-004 | Verify NICRA status counts | Compare NICRA records under each status with the corresponding status count. | Each status count matches the applicable NICRA records. |
| PM-NICRA-LP-005 | Verify NICRA search | Search using an existing New Initiative Name or configured searchable value. | The matching NICRA case is displayed. |
| PM-NICRA-LP-006 | Verify NICRA search with non-existing value | Enter a value that does not exist. | No matching NICRA record is displayed. |
| PM-NICRA-LP-007 | Verify NICRA filtering | Apply an available grid filter. | Only NICRA records matching the filter are displayed. |
| PM-NICRA-LP-008 | Verify clearing NICRA filter | Clear the applied filter. | All applicable NICRA records are restored. |
| PM-NICRA-LP-009 | Verify NICRA sorting | Sort a sortable column in ascending and descending order. | Records are displayed in the selected sort order. |
| PM-NICRA-LP-010 | Verify NICRA pagination and scrolling | Navigate through pages and scroll horizontally. | Correct records are displayed and all configured columns are accessible. |
| PM-NICRA-LP-011 | Verify NICRA common fields | Review **Status, Created By, Created Date, Last Updated Date and Completed Date**. | Common fields display the correct case information. |
| PM-NICRA-LP-012 | Verify multiple Country Coverage values | Open a NICRA case containing multiple countries. | All selected Country Coverage values are displayed correctly. |
| PM-NICRA-LP-013 | Verify Country Coverage maximum | Open/create a NICRA case with the maximum permitted Country Coverage. | Up to **five countries** are accepted and displayed correctly. |
| PM-NICRA-LP-014 | Verify New Initiative Summary Click to View | Select **Click to View** for New Initiative Summary. | Popup opens and displays the New Initiative Summary. |
| PM-NICRA-LP-015 | Verify complete New Initiative Summary | Review a case containing a long New Initiative Summary. | Complete summary is displayed without unintended truncation. |
| PM-NICRA-LP-016 | Verify multiple Business/Function and CFCR RFOs | Open a NICRA case with multiple Business/Function and CFCR RFO selections. | All selected values are displayed correctly. |
| PM-NICRA-LP-017 | Verify NICRA data accuracy | Compare **New Initiative Name, New Initiative Summary, First Line, Senior Manager / Group Business Head, Country Coverage, Business/Function and CFCR RFOs** with the submitted assessment. | All NICRA values match the submitted assessment. |

## B. Initiate Risk Assessment

| Test Case ID | Test Scenario | Test Steps | Expected Result |
|---|---|---|---|
| PM-NICRA-INIT-001 | Verify NICRA fields are displayed | Select **NICRA** and open Initiate Risk Assessment. | The screen displays **New Initiative Name, New Initiative Summary, First Line, Senior Manager / Group Business Head, Country Coverage, Business/Function and CFCR RFOs**. |
| PM-NICRA-INIT-002 | Verify NICRA mandatory validation | Leave required NICRA fields blank and attempt to continue/submit. | Mandatory validation is displayed and progression is prevented until required fields are completed. |
| PM-NICRA-INIT-003 | Verify New Initiative Name entry | Enter a valid New Initiative Name. | New Initiative Name is accepted and retained correctly. |
| PM-NICRA-INIT-004 | Verify New Initiative Summary entry | Enter a valid New Initiative Summary. | New Initiative Summary is accepted and retained correctly. |
| PM-NICRA-INIT-005 | Verify First Line PSID population | Enter/select the PSID for First Line according to the configured mechanism. | The corresponding First Line value is populated correctly. |
| PM-NICRA-INIT-006 | Verify Senior Manager / Group Business Head PSID population | Enter/select the PSID for Senior Manager / Group Business Head. | The corresponding user is populated correctly. |
| PM-NICRA-INIT-007 | Verify Country Coverage selection | Select multiple countries. | Selected countries are retained correctly. |
| PM-NICRA-INIT-008 | Verify Country Coverage maximum of five | Select five countries and then attempt to select a sixth country. | Five countries can be selected. Selection beyond five is prevented or appropriately validated. |
| PM-NICRA-INIT-009 | Verify multiple Business/Function selection | Select multiple Business/Function values. | Multiple Business/Function values are accepted and retained correctly. |
| PM-NICRA-INIT-010 | Verify CFCR RFO population for Business/Function | Select the required Business/Function values and review CFCR RFOs. | Applicable CFCR RFOs are populated according to the configured CRHS logic. |
| PM-NICRA-INIT-011 | Verify multiple CFCR RFOs | Use a NICRA case with multiple applicable RFOs. | All applicable CFCR RFOs are populated/displayed correctly. |
| PM-NICRA-INIT-012 | Verify NICRA submission | Complete all mandatory NICRA fields and submit the Initiative. | NICRA assessment is created successfully and progresses to the next configured stage. |

## C. Details Panel

| Test Case ID | Test Scenario | Test Steps | Expected Result |
|---|---|---|---|
| PM-NICRA-DET-001 | Verify NICRA Details | Open a NICRA assessment and open Details. | Details displays **New Initiative Name, New Initiative Summary, First Line, Senior Manager / Group Business Head, Country Coverage, Business/Function and CFCR RFOs**. |
| PM-NICRA-DET-002 | Verify NICRA Details values | Compare Details values with the submitted Initiative. | All displayed NICRA values match the submitted assessment. |
| PM-NICRA-DET-003 | Verify New Initiative Summary in Details | Select **Click to View** for New Initiative Summary. | Popup opens and displays the complete New Initiative Summary without unintended truncation. |
| PM-NICRA-DET-004 | Verify common Details information | Review **Case ID, Initiative Category, Status, Created By, Created Date, Last Updated Date and Completed Date**. | Common Details information is displayed correctly. |

## D. Landing Page Export

| Test Case ID | Test Scenario | Test Steps | Expected Result |
|---|---|---|---|
| PM-NICRA-LPE-001 | Verify NICRA Landing Page Export | Select NICRA and open Export. | Landing Page Export is available. |
| PM-NICRA-LPE-002 | Verify NICRA export generation | Export NICRA data and open the downloaded file. | Export file is generated, downloaded and opened successfully. |
| PM-NICRA-LPE-003 | Verify NICRA exported fields | Review **New Initiative Name, New Initiative Summary, First Line, Senior Manager / Group Business Head, Country Coverage, Business/Function and CFCR RFOs**. | Exported values match Landing Page data. |
| PM-NICRA-LPE-004 | Verify NICRA common exported fields | Review **Status, Created By, Created Date, Last Updated Date and Completed Date**. | Common exported values match Landing Page data. |
| PM-NICRA-LPE-005 | Verify New Initiative Summary export | Export a case containing a long New Initiative Summary. | Complete New Initiative Summary is exported without unintended truncation. |
| PM-NICRA-LPE-006 | Verify filtered NICRA export | Apply a filter and export. | Export contains records matching the applied filter. |
| PM-NICRA-LPE-007 | Verify searched NICRA export | Search for a NICRA case and export. | Export reflects the applicable searched records. |
| PM-NICRA-LPE-008 | Verify NICRA export accuracy | Compare exported data with Landing Page data. | Exported NICRA data matches the Landing Page. |

## E. Workflow Export

| Test Case ID | Test Scenario | Test Steps | Expected Result |
|---|---|---|---|
| PM-NICRA-WFE-001 | Verify NICRA Workflow Export | Open a NICRA assessment and select Workflow Export. | Workflow Export is available. |
| PM-NICRA-WFE-002 | Verify NICRA Workflow Export generation | Select Workflow Export and open the downloaded file. | Workflow Export is generated and opened successfully. |
| PM-NICRA-WFE-003 | Verify NICRA Workflow Export fields | Review **New Initiative Name, New Initiative Summary, First Line, Senior Manager / Group Business Head, Country Coverage, Business/Function and CFCR RFOs**. | Exported values match workflow data. |
| PM-NICRA-WFE-004 | Verify common Workflow Export fields | Review **Case ID, Initiative Category, Status, Created By, Created Date, Last Updated Date and Completed Date**. | Common exported values match workflow data. |
| PM-NICRA-WFE-005 | Verify New Initiative Summary Workflow Export | Export an assessment containing a long New Initiative Summary. | Complete New Initiative Summary is exported without unintended truncation. |
| PM-NICRA-WFE-006 | Verify NICRA Workflow Export accuracy | Compare workflow information with the exported file. | Exported NICRA data matches workflow data. |

---

# 4. OTHER

## A. Landing Page

| Test Case ID | Test Scenario | Test Steps | Expected Result |
|---|---|---|---|
| PM-OTH-LP-001 | Verify Other cases are displayed | Open COI Landing Page and select **Other** from Initiative Category. | Other cases are displayed in the grid. |
| PM-OTH-LP-002 | Verify Other grid fields | Review the columns displayed for an Other case. | The grid displays **New Initiative Name, New Initiative Summary, First Line, Approver, Country Coverage, Business/Function and CFCR RFOs**. |
| PM-OTH-LP-003 | Verify Other status display | Review Other cases in **In Progress, Pending Endorsement, Refer Back, Endorsement by RFO and Completed** statuses. | Each case is displayed under its correct status. |
| PM-OTH-LP-004 | Verify Other status counts | Compare Other records for each status with the corresponding status count. | Each status count matches the applicable Other records. |
| PM-OTH-LP-005 | Verify Other search | Search using an existing New Initiative Name or configured searchable value. | Matching Other case is displayed. |
| PM-OTH-LP-006 | Verify Other search with non-existing value | Enter a value that does not exist. | No matching Other record is displayed. |
| PM-OTH-LP-007 | Verify Other filtering | Apply an available grid filter. | Only records matching the filter are displayed. |
| PM-OTH-LP-008 | Verify clearing Other filter | Clear the applied filter. | All applicable Other records are restored. |
| PM-OTH-LP-009 | Verify Other sorting | Sort a sortable column in ascending and descending order. | Records are displayed in the selected sort order. |
| PM-OTH-LP-010 | Verify Other pagination and scrolling | Navigate through grid pages and scroll horizontally. | Correct records are displayed and all configured columns are accessible. |
| PM-OTH-LP-011 | Verify Other common fields | Review **Status, Created By, Created Date, Last Updated Date and Completed Date**. | Common fields display the correct case information. |
| PM-OTH-LP-012 | Verify multiple Country Coverage values | Open an Other case containing multiple countries. | All selected Country Coverage values are displayed correctly. |
| PM-OTH-LP-013 | Verify Country Coverage maximum | Open/create an Other case with the maximum permitted Country Coverage and attempt to exceed the limit. | The configured maximum is supported and additional selections beyond the limit are prevented or validated. |
| PM-OTH-LP-014 | Verify multiple Business/Function and CFCR RFOs | Open an Other case containing multiple Business/Function and CFCR RFO values. | All selected values are displayed correctly. |
| PM-OTH-LP-015 | Verify New Initiative Summary Click to View | Select **Click to View** for New Initiative Summary. | Popup opens and displays the New Initiative Summary. |
| PM-OTH-LP-016 | Verify complete New Initiative Summary | Review a case containing a long New Initiative Summary. | Complete summary is displayed without unintended truncation. |
| PM-OTH-LP-017 | Verify Other data accuracy | Compare **New Initiative Name, New Initiative Summary, First Line, Approver, Country Coverage, Business/Function and CFCR RFOs** with the submitted assessment. | All Other values match the submitted assessment. |

## B. Initiate Risk Assessment

| Test Case ID | Test Scenario | Test Steps | Expected Result |
|---|---|---|---|
| PM-OTH-INIT-001 | Verify Other fields are displayed | Select **Other** and open Initiate Risk Assessment. | The screen displays **New Initiative Name, New Initiative Summary, First Line, Approver, Country Coverage, Business/Function and CFCR RFOs**. |
| PM-OTH-INIT-002 | Verify Other mandatory validation | Leave required Other fields blank and attempt to continue/submit. | Mandatory validation is displayed and progression is prevented until required information is entered. |
| PM-OTH-INIT-003 | Verify New Initiative Name entry | Enter a valid New Initiative Name. | New Initiative Name is accepted and retained correctly. |
| PM-OTH-INIT-004 | Verify New Initiative Summary entry | Enter a valid New Initiative Summary. | New Initiative Summary is accepted and retained correctly. |
| PM-OTH-INIT-005 | Verify First Line PSID population | Enter/select the PSID for First Line according to the configured mechanism. | The corresponding First Line is populated correctly. |
| PM-OTH-INIT-006 | Verify Approver PSID population | Enter/select the PSID for Approver. | The corresponding Approver is populated correctly. |
| PM-OTH-INIT-007 | Verify Country Coverage selection | Select multiple countries. | Selected Country Coverage values are retained correctly. |
| PM-OTH-INIT-008 | Verify Country Coverage maximum | Select countries up to the configured maximum and attempt to select one more. | The configured maximum is accepted and selection beyond the maximum is prevented or appropriately validated. |
| PM-OTH-INIT-009 | Verify multiple Business/Function selection | Select multiple Business/Function values. | Multiple Business/Function values can be selected and retained correctly. |
| PM-OTH-INIT-010 | Verify CFCR RFO population | Select the required Business/Function values and review CFCR RFOs. | Applicable CFCR RFOs are populated according to the configured CRHS logic. |
| PM-OTH-INIT-011 | Verify multiple CFCR RFOs | Use an Other case with multiple applicable RFOs. | All applicable CFCR RFOs are populated/displayed correctly. |
| PM-OTH-INIT-012 | Verify Other submission | Complete all mandatory Other information and submit the Initiative. | The Other assessment is created successfully and progresses to the next configured stage. |

## C. Details Panel

| Test Case ID | Test Scenario | Test Steps | Expected Result |
|---|---|---|---|
| PM-OTH-DET-001 | Verify Other Details | Open an Other assessment and open Details. | Details displays **New Initiative Name, New Initiative Summary, First Line, Approver, Country Coverage, Business/Function and CFCR RFOs**. |
| PM-OTH-DET-002 | Verify Other Details values | Compare Details values with the submitted Initiative. | All displayed Other values match the submitted assessment. |
| PM-OTH-DET-003 | Verify New Initiative Summary in Details | Select **Click to View** for New Initiative Summary. | Popup opens and displays the complete New Initiative Summary without unintended truncation. |
| PM-OTH-DET-004 | Verify common Details information | Review **Case ID, Initiative Category, Status, Created By, Created Date, Last Updated Date and Completed Date**. | Common Details information is displayed correctly. |

## D. Landing Page Export

| Test Case ID | Test Scenario | Test Steps | Expected Result |
|---|---|---|---|
| PM-OTH-LPE-001 | Verify Other Landing Page Export | Select Other and open Export. | Landing Page Export is available. |
| PM-OTH-LPE-002 | Verify Other export generation | Export Other data and open the downloaded file. | Export file is generated, downloaded and opened successfully. |
| PM-OTH-LPE-003 | Verify Other exported fields | Review **New Initiative Name, New Initiative Summary, First Line, Approver, Country Coverage, Business/Function and CFCR RFOs**. | Exported values match Landing Page data. |
| PM-OTH-LPE-004 | Verify Other common exported fields | Review **Status, Created By, Created Date, Last Updated Date and Completed Date**. | Common exported values match Landing Page data. |
| PM-OTH-LPE-005 | Verify New Initiative Summary export | Export a case containing a long New Initiative Summary. | Complete New Initiative Summary is exported without unintended truncation. |
| PM-OTH-LPE-006 | Verify filtered Other export | Apply a filter and export. | Export contains records corresponding to the applied filter. |
| PM-OTH-LPE-007 | Verify searched Other export | Search for an Other case and export. | Export reflects the applicable searched records. |
| PM-OTH-LPE-008 | Verify Other export accuracy | Compare exported data with Landing Page data. | Exported Other data matches the Landing Page. |

## E. Workflow Export

| Test Case ID | Test Scenario | Test Steps | Expected Result |
|---|---|---|---|
| PM-OTH-WFE-001 | Verify Other Workflow Export | Open an Other assessment and select Workflow Export. | Workflow Export is available. |
| PM-OTH-WFE-002 | Verify Other Workflow Export generation | Select Workflow Export and open the downloaded file. | Workflow Export is generated and opened successfully. |
| PM-OTH-WFE-003 | Verify Other Workflow Export fields | Review **New Initiative Name, New Initiative Summary, First Line, Approver, Country Coverage, Business/Function and CFCR RFOs**. | Exported values match workflow data. |
| PM-OTH-WFE-004 | Verify common Workflow Export fields | Review **Case ID, Initiative Category, Status, Created By, Created Date, Last Updated Date and Completed Date**. | Common exported values match workflow data. |
| PM-OTH-WFE-005 | Verify New Initiative Summary Workflow Export | Export an assessment containing a long New Initiative Summary. | Complete New Initiative Summary is exported without unintended truncation. |
| PM-OTH-WFE-006 | Verify Other Workflow Export accuracy | Compare workflow information with the exported file. | Exported Other data matches workflow data. |

### So the final workbook is simply:

**Sheet 1 — New Product - Product Change**
- Landing Page
- Initiate Risk Assessment
- Details Panel
- Landing Page Export
- Workflow Export

**Sheet 2 — Corporate Action**
- Landing Page
- Initiate Risk Assessment
- Details Panel
- Landing Page Export
- Workflow Export

**Sheet 3 — NICRA**
- Landing Page
- Initiate Risk Assessment
- Details Panel
- Landing Page Export
- Workflow Export

**Sheet 4 — Other**
- Landing Page
- Initiate Risk Assessment
- Details Panel
- Landing Page Export
- Workflow Export

This is much more appropriate for **actual UAT execution** than the previous vague version. The tester can pick a category, start at the Landing Page, then move through Initiation → Details → Exports without needing to interpret the BRD.

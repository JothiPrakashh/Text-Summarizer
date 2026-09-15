Yes. We’ll do **RFO exactly in the same category-wise structure**.

Since **RFO does not initiate the assessment**, there will be **no Initiate Risk Assessment section** for RFO.

For each category:

1. **Landing Page**
2. **Details Panel**
3. **Landing Page Export**
4. **Workflow Export**

And the cases are written for an **actual UAT user**, so they can execute them without knowing the BRD.

---

# 1. NEW PRODUCT / PRODUCT CHANGE — RFO

## A. Landing Page

| Test Case ID | Test Scenario | Test Steps | Expected Result |
|---|---|---|---|
| RFO-NP-LP-001 | Verify RFO can access New Product / Product Change cases | Login as an RFO, open COI and select **New Product / Product Change** from Initiative Category. | New Product / Product Change cases accessible to the RFO are displayed. |
| RFO-NP-LP-002 | Verify New Product / Product Change grid fields | Review a New Product / Product Change case in the Landing Page grid. | The grid displays **Programme code, Programme Name, Product manager, Business head / Product head, Business line, CFCR RFO, Product description & scope, Applicable to – Islamic variant and Applicable to – Sustainable finance variant**. |
| RFO-NP-LP-003 | Verify New Product / Product Change status display | Review New Product / Product Change cases under **In Progress, Pending Endorsement, Refer Back, Endorsement by RFO and Completed**. | Each case is displayed with the status matching its actual assessment state. |
| RFO-NP-LP-004 | Verify New Product / Product Change status counts | Compare the number of New Product / Product Change cases displayed under each status with the corresponding status count. | Each status count matches the applicable RFO-accessible cases. |
| RFO-NP-LP-005 | Verify search using Programme code | Enter an existing Programme code in the Landing Page search field. | The corresponding New Product / Product Change case is displayed. |
| RFO-NP-LP-006 | Verify search with non-existing value | Enter a Programme code or searchable value that does not exist. | No matching case is displayed. |
| RFO-NP-LP-007 | Verify filtering of New Product / Product Change cases | Apply an available grid filter. | Only records matching the selected filter are displayed. |
| RFO-NP-LP-008 | Verify clearing of filter | Clear the applied grid filter. | All applicable New Product / Product Change cases are displayed again. |
| RFO-NP-LP-009 | Verify sorting of New Product / Product Change cases | Sort a sortable column in ascending and descending order. | Records are displayed in the selected sort order. |
| RFO-NP-LP-010 | Verify pagination and horizontal scrolling | Navigate through grid pages and scroll horizontally across the grid. | Correct records are displayed on each page and all configured columns are accessible. |
| RFO-NP-LP-011 | Verify common case information | Review **Status, Created By, Created Date, Last Updated Date and Completed Date**. | Each field displays the correct information for the selected case. |
| RFO-NP-LP-012 | Verify Product description & scope Click to View | Select **Click to View** for Product description & scope. | A popup opens displaying the Product description & scope. |
| RFO-NP-LP-013 | Verify complete Product description & scope | Open a case containing a long Product description & scope and select **Click to View**. | Complete Product description & scope is displayed without unintended truncation. |
| RFO-NP-LP-014 | Verify RFO read-only access to New Product / Product Change data | Open a New Product / Product Change case and attempt to edit **Programme code, Programme Name, Product manager, Business head / Product head, Business line, CFCR RFO, Product description & scope, Applicable to – Islamic variant and Applicable to – Sustainable finance variant**. | The PM-submitted information is read-only to the RFO and cannot be modified. |
| RFO-NP-LP-015 | Verify New Product / Product Change data accuracy | Compare the displayed category-specific information with the submitted assessment. | All displayed values match the PM-submitted assessment. |

## B. Details Panel

| Test Case ID | Test Scenario | Test Steps | Expected Result |
|---|---|---|---|
| RFO-NP-DET-001 | Verify New Product / Product Change Details | Open a New Product / Product Change assessment and open the **Details** panel. | Details displays **Programme code, Programme Name, Product manager, Business head / Product head, Business line, CFCR RFO, Product description & scope, Applicable to – Islamic variant and Applicable to – Sustainable finance variant**. |
| RFO-NP-DET-002 | Verify New Product / Product Change Details values | Compare the Details values with the PM-submitted Initiative information. | All displayed values match the submitted assessment. |
| RFO-NP-DET-003 | Verify Product description & scope in Details | Select **Click to View** for Product description & scope in Details. | Popup opens and displays the complete Product description & scope without unintended truncation. |
| RFO-NP-DET-004 | Verify common Details information | Review **Case ID, Initiative Category, Status, Created By, Created Date, Last Updated Date and Completed Date**. | All common Details information is displayed correctly. |
| RFO-NP-DET-005 | Verify RFO cannot edit Details information | Attempt to modify the displayed New Product / Product Change information. | Details information remains read-only to the RFO. |

## C. Landing Page Export

| Test Case ID | Test Scenario | Test Steps | Expected Result |
|---|---|---|---|
| RFO-NP-LPE-001 | Verify New Product / Product Change Landing Page Export | Select New Product / Product Change and open the Export option. | Landing Page Export is available according to RFO permissions. |
| RFO-NP-LPE-002 | Verify New Product / Product Change export generation | Select Export and open the downloaded file. | Export file is generated, downloaded and opened successfully. |
| RFO-NP-LPE-003 | Verify New Product / Product Change exported fields | Review **Programme code, Programme Name, Product manager, Business head / Product head, Business line, CFCR RFO, Product description & scope, Applicable to – Islamic variant and Applicable to – Sustainable finance variant**. | Exported values match the RFO Landing Page data. |
| RFO-NP-LPE-004 | Verify common exported fields | Review **Status, Created By, Created Date, Last Updated Date and Completed Date**. | Common exported values match the Landing Page. |
| RFO-NP-LPE-005 | Verify Product description & scope export | Export a case containing a long Product description & scope. | Complete Product description & scope is exported without unintended truncation. |
| RFO-NP-LPE-006 | Verify filtered New Product / Product Change export | Apply a filter and export the results. | Export contains only records matching the applied filter. |
| RFO-NP-LPE-007 | Verify searched New Product / Product Change export | Search for a specific Programme code and export. | Export reflects the applicable searched records. |
| RFO-NP-LPE-008 | Verify RFO export access control | Export New Product / Product Change cases as RFO. | Export contains only cases and information accessible to the RFO. |
| RFO-NP-LPE-009 | Verify Landing Page export accuracy | Compare the exported data with the RFO Landing Page. | Exported data matches the corresponding Landing Page data. |

## D. Workflow Export

| Test Case ID | Test Scenario | Test Steps | Expected Result |
|---|---|---|---|
| RFO-NP-WFE-001 | Verify New Product / Product Change Workflow Export | Open an accessible New Product / Product Change assessment and select Workflow Export. | Workflow Export is available according to RFO permissions. |
| RFO-NP-WFE-002 | Verify Workflow Export generation | Select Workflow Export and open the downloaded file. | Workflow Export is generated, downloaded and opened successfully. |
| RFO-NP-WFE-003 | Verify New Product / Product Change Workflow Export fields | Review **Programme code, Programme Name, Product manager, Business head / Product head, Business line, CFCR RFO, Product description & scope, Applicable to – Islamic variant and Applicable to – Sustainable finance variant**. | Exported values match the assessment data. |
| RFO-NP-WFE-004 | Verify common Workflow Export fields | Review **Case ID, Initiative Category, Status, Created By, Created Date, Last Updated Date and Completed Date**. | Common exported values match the assessment. |
| RFO-NP-WFE-005 | Verify Product description & scope Workflow Export | Export an assessment containing a long Product description & scope. | Complete Product description & scope is exported without unintended truncation. |
| RFO-NP-WFE-006 | Verify RFO Workflow Export access control | Export an assessment as RFO and review the exported information. | Only information permitted for RFO access is included. |
| RFO-NP-WFE-007 | Verify Workflow Export accuracy | Compare the assessment with the exported file. | Exported data matches the corresponding assessment data. |

---

# 2. CORPORATE ACTION — RFO

## A. Landing Page

| Test Case ID | Test Scenario | Test Steps | Expected Result |
|---|---|---|---|
| RFO-CA-LP-001 | Verify RFO can access Corporate Action cases | Login as RFO, open COI and select **Corporate Action**. | Corporate Action cases accessible to the RFO are displayed. |
| RFO-CA-LP-002 | Verify Corporate Action grid fields | Review a Corporate Action case in the Landing Page grid. | The grid displays **Project Name, Transaction, Rationale, Responsible Person, Accountable Executive, MT Sponsor, Business/Function and CFCR RFOs**. |
| RFO-CA-LP-003 | Verify Corporate Action status display | Review Corporate Action cases under **In Progress, Pending Endorsement, Refer Back, Endorsement by RFO and Completed**. | Each case is displayed with its correct actual status. |
| RFO-CA-LP-004 | Verify Corporate Action status counts | Compare each status count with the Corporate Action records displayed. | Each status count matches the applicable RFO-accessible records. |
| RFO-CA-LP-005 | Verify Corporate Action search | Search using an existing Project Name or configured searchable value. | The matching Corporate Action case is displayed. |
| RFO-CA-LP-006 | Verify Corporate Action search with non-existing value | Enter a value that does not exist. | No matching Corporate Action case is displayed. |
| RFO-CA-LP-007 | Verify Corporate Action filtering | Apply an available grid filter. | Only records matching the selected filter are displayed. |
| RFO-CA-LP-008 | Verify clearing Corporate Action filter | Clear the applied filter. | All applicable Corporate Action records are restored. |
| RFO-CA-LP-009 | Verify Corporate Action sorting | Sort a sortable column in ascending and descending order. | Records are displayed in the selected sort order. |
| RFO-CA-LP-010 | Verify Corporate Action pagination and scrolling | Navigate through pages and scroll horizontally. | Correct records are displayed and all configured columns are accessible. |
| RFO-CA-LP-011 | Verify Corporate Action common fields | Review **Status, Created By, Created Date, Last Updated Date and Completed Date**. | Common fields display the correct values. |
| RFO-CA-LP-012 | Verify multiple Business/Function values | Open a Corporate Action case containing multiple Business/Function values. | All selected Business/Function values are displayed correctly. |
| RFO-CA-LP-013 | Verify multiple CFCR RFOs | Open a Corporate Action case containing multiple CFCR RFOs. | All applicable CFCR RFOs are displayed correctly. |
| RFO-CA-LP-014 | Verify Transaction Click to View | Select **Click to View** for Transaction. | Transaction popup opens successfully. |
| RFO-CA-LP-015 | Verify complete Transaction text | Review a Transaction containing lengthy text. | Complete Transaction text is displayed without unintended truncation. |
| RFO-CA-LP-016 | Verify Rationale Click to View | Select **Click to View** for Rationale. | Rationale popup opens successfully. |
| RFO-CA-LP-017 | Verify complete Rationale text | Review a Rationale containing lengthy text. | Complete Rationale text is displayed without unintended truncation. |
| RFO-CA-LP-018 | Verify RFO read-only Corporate Action data | Attempt to edit **Project Name, Transaction, Rationale, Responsible Person, Accountable Executive, MT Sponsor, Business/Function and CFCR RFOs**. | Corporate Action information submitted by PM is read-only to RFO. |
| RFO-CA-LP-019 | Verify Corporate Action data accuracy | Compare displayed information with the submitted assessment. | All Corporate Action values match the PM-submitted assessment. |

## B. Details Panel

| Test Case ID | Test Scenario | Test Steps | Expected Result |
|---|---|---|---|
| RFO-CA-DET-001 | Verify Corporate Action Details | Open a Corporate Action assessment and open Details. | Details displays **Project Name, Transaction, Rationale, Responsible Person, Accountable Executive, MT Sponsor, Business/Function and CFCR RFOs**. |
| RFO-CA-DET-002 | Verify Corporate Action Details values | Compare Details with the submitted assessment. | All Corporate Action values match the PM submission. |
| RFO-CA-DET-003 | Verify Transaction in Details | Select **Click to View** for Transaction. | Popup opens and displays complete Transaction text. |
| RFO-CA-DET-004 | Verify Rationale in Details | Select **Click to View** for Rationale. | Popup opens and displays complete Rationale text. |
| RFO-CA-DET-005 | Verify common Details information | Review **Case ID, Initiative Category, Status, Created By, Created Date, Last Updated Date and Completed Date**. | Common Details information is displayed correctly. |
| RFO-CA-DET-006 | Verify RFO cannot edit Details information | Attempt to modify Corporate Action Details. | Details information remains read-only to RFO. |

## C. Landing Page Export

| Test Case ID | Test Scenario | Test Steps | Expected Result |
|---|---|---|---|
| RFO-CA-LPE-001 | Verify Corporate Action Landing Page Export | Select Corporate Action and open Export. | Landing Page Export is available according to RFO permissions. |
| RFO-CA-LPE-002 | Verify Corporate Action export generation | Select Export and open the downloaded file. | Export is generated, downloaded and opened successfully. |
| RFO-CA-LPE-003 | Verify Corporate Action exported fields | Review **Project Name, Transaction, Rationale, Responsible Person, Accountable Executive, MT Sponsor, Business/Function and CFCR RFOs**. | Exported values match Landing Page data. |
| RFO-CA-LPE-004 | Verify common exported fields | Review **Status, Created By, Created Date, Last Updated Date and Completed Date**. | Common exported values match Landing Page data. |
| RFO-CA-LPE-005 | Verify Transaction export | Export a case containing long Transaction text. | Complete Transaction text is exported without unintended truncation. |
| RFO-CA-LPE-006 | Verify Rationale export | Export a case containing long Rationale text. | Complete Rationale text is exported without unintended truncation. |
| RFO-CA-LPE-007 | Verify filtered Corporate Action export | Apply a filter and export. | Export contains only records matching the filter. |
| RFO-CA-LPE-008 | Verify searched Corporate Action export | Search for a specific Corporate Action case and export. | Export reflects the applicable searched records. |
| RFO-CA-LPE-009 | Verify RFO export access control | Export Corporate Action cases as RFO. | Export contains only cases and information accessible to RFO. |
| RFO-CA-LPE-010 | Verify Corporate Action export accuracy | Compare exported data with the Landing Page. | Exported Corporate Action data matches the Landing Page. |

## D. Workflow Export

| Test Case ID | Test Scenario | Test Steps | Expected Result |
|---|---|---|---|
| RFO-CA-WFE-001 | Verify Corporate Action Workflow Export | Open a Corporate Action assessment and select Workflow Export. | Workflow Export is available. |
| RFO-CA-WFE-002 | Verify Workflow Export generation | Select Workflow Export and open the downloaded file. | Workflow Export is generated and opened successfully. |
| RFO-CA-WFE-003 | Verify Corporate Action Workflow Export fields | Review **Project Name, Transaction, Rationale, Responsible Person, Accountable Executive, MT Sponsor, Business/Function and CFCR RFOs**. | Exported values match workflow data. |
| RFO-CA-WFE-004 | Verify common Workflow Export fields | Review **Case ID, Initiative Category, Status, Created By, Created Date, Last Updated Date and Completed Date**. | Common exported values match workflow data. |
| RFO-CA-WFE-005 | Verify Transaction Workflow Export | Export an assessment containing long Transaction text. | Complete Transaction text is exported without unintended truncation. |
| RFO-CA-WFE-006 | Verify Rationale Workflow Export | Export an assessment containing long Rationale text. | Complete Rationale text is exported without unintended truncation. |
| RFO-CA-WFE-007 | Verify RFO Workflow Export access control | Export the assessment as RFO and review the file. | Only information permitted for RFO access is included. |
| RFO-CA-WFE-008 | Verify Corporate Action Workflow Export accuracy | Compare workflow information with the exported file. | Exported data matches the corresponding workflow data. |

---

# 3. NICRA — RFO

## A. Landing Page

| Test Case ID | Test Scenario | Test Steps | Expected Result |
|---|---|---|---|
| RFO-NICRA-LP-001 | Verify RFO can access NICRA cases | Login as RFO, open COI and select **NICRA**. | NICRA cases accessible to the RFO are displayed. |
| RFO-NICRA-LP-002 | Verify NICRA grid fields | Review a NICRA case in the Landing Page grid. | The grid displays **New Initiative Name, New Initiative Summary, First Line, Senior Manager / Group Business Head, Country Coverage, Business/Function and CFCR RFOs**. |
| RFO-NICRA-LP-003 | Verify NICRA status display | Review NICRA cases under **In Progress, Pending Endorsement, Refer Back, Endorsement by RFO and Completed**. | Each case is displayed with its correct actual status. |
| RFO-NICRA-LP-004 | Verify NICRA status counts | Compare NICRA records displayed under each status with the corresponding status count. | Each status count matches the applicable RFO-accessible records. |
| RFO-NICRA-LP-005 | Verify NICRA search | Search using an existing New Initiative Name or configured searchable value. | The matching NICRA case is displayed. |
| RFO-NICRA-LP-006 | Verify NICRA search with non-existing value | Enter a value that does not exist. | No matching NICRA case is displayed. |
| RFO-NICRA-LP-007 | Verify NICRA filtering | Apply an available grid filter. | Only records matching the selected filter are displayed. |
| RFO-NICRA-LP-008 | Verify clearing NICRA filter | Clear the applied filter. | All applicable NICRA records are restored. |
| RFO-NICRA-LP-009 | Verify NICRA sorting | Sort a sortable column in ascending and descending order. | Records are displayed in the selected sort order. |
| RFO-NICRA-LP-010 | Verify NICRA pagination and scrolling | Navigate through pages and scroll horizontally. | Correct records are displayed and all configured columns are accessible. |
| RFO-NICRA-LP-011 | Verify NICRA common fields | Review **Status, Created By, Created Date, Last Updated Date and Completed Date**. | Common fields display the correct values. |
| RFO-NICRA-LP-012 | Verify multiple Country Coverage values | Open a NICRA case containing multiple countries. | All selected Country Coverage values are displayed correctly. |
| RFO-NICRA-LP-013 | Verify Country Coverage maximum | Review a NICRA case containing the maximum permitted countries. | Up to **five countries** are displayed correctly. |
| RFO-NICRA-LP-014 | Verify multiple Business/Function and CFCR RFOs | Open a NICRA case containing multiple Business/Function and CFCR RFO values. | All selected values are displayed correctly. |
| RFO-NICRA-LP-015 | Verify New Initiative Summary Click to View | Select **Click to View** for New Initiative Summary. | Popup opens and displays the New Initiative Summary. |
| RFO-NICRA-LP-016 | Verify complete New Initiative Summary | Review a case containing a long New Initiative Summary. | Complete summary is displayed without unintended truncation. |
| RFO-NICRA-LP-017 | Verify RFO read-only NICRA data | Attempt to edit **New Initiative Name, New Initiative Summary, First Line, Senior Manager / Group Business Head, Country Coverage, Business/Function and CFCR RFOs**. | NICRA information submitted by PM is read-only to RFO. |
| RFO-NICRA-LP-018 | Verify NICRA data accuracy | Compare displayed information with the submitted assessment. | All NICRA values match the PM-submitted assessment. |

## B. Details Panel

| Test Case ID | Test Scenario | Test Steps | Expected Result |
|---|---|---|---|
| RFO-NICRA-DET-001 | Verify NICRA Details | Open a NICRA assessment and open Details. | Details displays **New Initiative Name, New Initiative Summary, First Line, Senior Manager / Group Business Head, Country Coverage, Business/Function and CFCR RFOs**. |
| RFO-NICRA-DET-002 | Verify NICRA Details values | Compare Details values with the submitted assessment. | All displayed NICRA values match the PM submission. |
| RFO-NICRA-DET-003 | Verify New Initiative Summary in Details | Select **Click to View** for New Initiative Summary. | Popup opens and displays the complete summary without unintended truncation. |
| RFO-NICRA-DET-004 | Verify common Details information | Review **Case ID, Initiative Category, Status, Created By, Created Date, Last Updated Date and Completed Date**. | Common Details information is displayed correctly. |
| RFO-NICRA-DET-005 | Verify RFO cannot edit NICRA Details | Attempt to modify NICRA Details information. | NICRA Details remain read-only to RFO. |

## C. Landing Page Export

| Test Case ID | Test Scenario | Test Steps | Expected Result |
|---|---|---|---|
| RFO-NICRA-LPE-001 | Verify NICRA Landing Page Export | Select NICRA and open Export. | Landing Page Export is available according to RFO permissions. |
| RFO-NICRA-LPE-002 | Verify NICRA export generation | Select Export and open the downloaded file. | Export is generated, downloaded and opened successfully. |
| RFO-NICRA-LPE-003 | Verify NICRA exported fields | Review **New Initiative Name, New Initiative Summary, First Line, Senior Manager / Group Business Head, Country Coverage, Business/Function and CFCR RFOs**. | Exported values match Landing Page data. |
| RFO-NICRA-LPE-004 | Verify common exported fields | Review **Status, Created By, Created Date, Last Updated Date and Completed Date**. | Common exported values match Landing Page data. |
| RFO-NICRA-LPE-005 | Verify New Initiative Summary export | Export a case containing a long New Initiative Summary. | Complete New Initiative Summary is exported without unintended truncation. |
| RFO-NICRA-LPE-006 | Verify filtered NICRA export | Apply a filter and export. | Export contains records corresponding to the applied filter. |
| RFO-NICRA-LPE-007 | Verify searched NICRA export | Search for a NICRA case and export. | Export reflects the applicable searched records. |
| RFO-NICRA-LPE-008 | Verify RFO export access control | Export NICRA cases as RFO. | Export contains only cases and information accessible to RFO. |
| RFO-NICRA-LPE-009 | Verify NICRA export accuracy | Compare exported data with the Landing Page. | Exported NICRA data matches the Landing Page. |

## D. Workflow Export

| Test Case ID | Test Scenario | Test Steps | Expected Result |
|---|---|---|---|
| RFO-NICRA-WFE-001 | Verify NICRA Workflow Export | Open a NICRA assessment and select Workflow Export. | Workflow Export is available. |
| RFO-NICRA-WFE-002 | Verify NICRA Workflow Export generation | Select Workflow Export and open the downloaded file. | Workflow Export is generated and opened successfully. |
| RFO-NICRA-WFE-003 | Verify NICRA Workflow Export fields | Review **New Initiative Name, New Initiative Summary, First Line, Senior Manager / Group Business Head, Country Coverage, Business/Function and CFCR RFOs**. | Exported values match workflow data. |
| RFO-NICRA-WFE-004 | Verify common Workflow Export fields | Review **Case ID, Initiative Category, Status, Created By, Created Date, Last Updated Date and Completed Date**. | Common exported values match workflow data. |
| RFO-NICRA-WFE-005 | Verify New Initiative Summary Workflow Export | Export an assessment containing a long New Initiative Summary. | Complete New Initiative Summary is exported without unintended truncation. |
| RFO-NICRA-WFE-006 | Verify RFO Workflow Export access control | Export an assessment as RFO and review the file. | Only information permitted for RFO access is included. |
| RFO-NICRA-WFE-007 | Verify NICRA Workflow Export accuracy | Compare workflow information with the exported file. | Exported data matches the corresponding workflow data. |

---

# 4. OTHER — RFO

## A. Landing Page

| Test Case ID | Test Scenario | Test Steps | Expected Result |
|---|---|---|---|
| RFO-OTH-LP-001 | Verify RFO can access Other cases | Login as RFO, open COI and select **Other**. | Other cases accessible to the RFO are displayed. |
| RFO-OTH-LP-002 | Verify Other grid fields | Review an Other case in the Landing Page grid. | The grid displays **New Initiative Name, New Initiative Summary, First Line, Approver, Country Coverage, Business/Function and CFCR RFOs**. |
| RFO-OTH-LP-003 | Verify Other status display | Review Other cases under **In Progress, Pending Endorsement, Refer Back, Endorsement by RFO and Completed**. | Each case is displayed with its correct actual status. |
| RFO-OTH-LP-004 | Verify Other status counts | Compare Other records displayed under each status with the corresponding status count. | Each status count matches the applicable RFO-accessible records. |
| RFO-OTH-LP-005 | Verify Other search | Search using an existing New Initiative Name or configured searchable value. | The matching Other case is displayed. |
| RFO-OTH-LP-006 | Verify Other search with non-existing value | Enter a value that does not exist. | No matching Other case is displayed. |
| RFO-OTH-LP-007 | Verify Other filtering | Apply an available grid filter. | Only records matching the selected filter are displayed. |
| RFO-OTH-LP-008 | Verify clearing Other filter | Clear the applied filter. | All applicable Other records are restored. |
| RFO-OTH-LP-009 | Verify Other sorting | Sort a sortable column in ascending and descending order. | Records are displayed in the selected sort order. |
| RFO-OTH-LP-010 | Verify Other pagination and scrolling | Navigate through pages and scroll horizontally. | Correct records are displayed and all configured columns are accessible. |
| RFO-OTH-LP-011 | Verify Other common fields | Review **Status, Created By, Created Date, Last Updated Date and Completed Date**. | Common fields display the correct values. |
| RFO-OTH-LP-012 | Verify multiple Country Coverage values | Open an Other case containing multiple countries. | All selected Country Coverage values are displayed correctly. |
| RFO-OTH-LP-013 | Verify Country Coverage maximum | Review an Other case containing the maximum permitted Country Coverage. | The configured maximum number of countries is displayed correctly. |
| RFO-OTH-LP-014 | Verify multiple Business/Function and CFCR RFOs | Open an Other case containing multiple Business/Function and CFCR RFO values. | All selected values are displayed correctly. |
| RFO-OTH-LP-015 | Verify New Initiative Summary Click to View | Select **Click to View** for New Initiative Summary. | Popup opens and displays the New Initiative Summary. |
| RFO-OTH-LP-016 | Verify complete New Initiative Summary | Review a case containing a long New Initiative Summary. | Complete summary is displayed without unintended truncation. |
| RFO-OTH-LP-017 | Verify RFO read-only Other data | Attempt to edit **New Initiative Name, New Initiative Summary, First Line, Approver, Country Coverage, Business/Function and CFCR RFOs**. | Other information submitted by PM is read-only to RFO. |
| RFO-OTH-LP-018 | Verify Other data accuracy | Compare displayed information with the submitted assessment. | All Other values match the PM-submitted assessment. |

## B. Details Panel

| Test Case ID | Test Scenario | Test Steps | Expected Result |
|---|---|---|---|
| RFO-OTH-DET-001 | Verify Other Details | Open an Other assessment and open Details. | Details displays **New Initiative Name, New Initiative Summary, First Line, Approver, Country Coverage, Business/Function and CFCR RFOs**. |
| RFO-OTH-DET-002 | Verify Other Details values | Compare Details values with the submitted assessment. | All displayed Other values match the PM submission. |
| RFO-OTH-DET-003 | Verify New Initiative Summary in Details | Select **Click to View** for New Initiative Summary. | Popup opens and displays the complete summary without unintended truncation. |
| RFO-OTH-DET-004 | Verify common Details information | Review **Case ID, Initiative Category, Status, Created By, Created Date, Last Updated Date and Completed Date**. | Common Details information is displayed correctly. |
| RFO-OTH-DET-005 | Verify RFO cannot edit Other Details | Attempt to modify Other Details information. | Other Details remain read-only to RFO. |

## C. Landing Page Export

| Test Case ID | Test Scenario | Test Steps | Expected Result |
|---|---|---|---|
| RFO-OTH-LPE-001 | Verify Other Landing Page Export | Select Other and open Export. | Landing Page Export is available according to RFO permissions. |
| RFO-OTH-LPE-002 | Verify Other export generation | Select Export and open the downloaded file. | Export is generated, downloaded and opened successfully. |
| RFO-OTH-LPE-003 | Verify Other exported fields | Review **New Initiative Name, New Initiative Summary, First Line, Approver, Country Coverage, Business/Function and CFCR RFOs**. | Exported values match Landing Page data. |
| RFO-OTH-LPE-004 | Verify common exported fields | Review **Status, Created By, Created Date, Last Updated Date and Completed Date**. | Common exported values match Landing Page data. |
| RFO-OTH-LPE-005 | Verify New Initiative Summary export | Export a case containing a long New Initiative Summary. | Complete New Initiative Summary is exported without unintended truncation. |
| RFO-OTH-LPE-006 | Verify filtered Other export | Apply a filter and export. | Export contains records corresponding to the applied filter. |
| RFO-OTH-LPE-007 | Verify searched Other export | Search for an Other case and export. | Export reflects the applicable searched records. |
| RFO-OTH-LPE-008 | Verify RFO export access control | Export Other cases as RFO. | Export contains only cases and information accessible to RFO. |
| RFO-OTH-LPE-009 | Verify Other export accuracy | Compare exported data with the Landing Page. | Exported Other data matches the Landing Page. |

## D. Workflow Export

| Test Case ID | Test Scenario | Test Steps | Expected Result |
|---|---|---|---|
| RFO-OTH-WFE-001 | Verify Other Workflow Export | Open an Other assessment and select Workflow Export. | Workflow Export is available. |
| RFO-OTH-WFE-002 | Verify Other Workflow Export generation | Select Workflow Export and open the downloaded file. | Workflow Export is generated and opened successfully. |
| RFO-OTH-WFE-003 | Verify Other Workflow Export fields | Review **New Initiative Name, New Initiative Summary, First Line, Approver, Country Coverage, Business/Function and CFCR RFOs**. | Exported values match workflow data. |
| RFO-OTH-WFE-004 | Verify common Workflow Export fields | Review **Case ID, Initiative Category, Status, Created By, Created Date, Last Updated Date and Completed Date**. | Common exported values match workflow data. |
| RFO-OTH-WFE-005 | Verify New Initiative Summary Workflow Export | Export an assessment containing a long New Initiative Summary. | Complete New Initiative Summary is exported without unintended truncation. |
| RFO-OTH-WFE-006 | Verify RFO Workflow Export access control | Export an assessment as RFO and review the file. | Only information permitted for RFO access is included. |
| RFO-OTH-WFE-007 | Verify Other Workflow Export accuracy | Compare workflow information with the exported file. | Exported data matches the corresponding workflow data. |

### Final RFO workbook

**Sheet 1 — New Product - Product Change**
- Landing Page
- Details Panel
- Landing Page Export
- Workflow Export

**Sheet 2 — Corporate Action**
- Landing Page
- Details Panel
- Landing Page Export
- Workflow Export

**Sheet 3 — NICRA**
- Landing Page
- Details Panel
- Landing Page Export
- Workflow Export

**Sheet 4 — Other**
- Landing Page
- Details Panel
- Landing Page Export
- Workflow Export

**No Initiative sheet for RFO.** RFO is the reviewer, not the maker, so the initiation test cases belong only in the PM workbook.

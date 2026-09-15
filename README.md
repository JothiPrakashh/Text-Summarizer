You're right. I misunderstood the structure again.

For **FRA**, you are testing only **one category: Material Change in Process**.

So:

### FRA — PM workbook
**ONE sheet:** `Material Change in Process`

Inside that single sheet, the order should be:

1. **Landing Page**
2. **Initiate Risk Assessment**
3. **Details Panel**
4. **Landing Page Export**
5. **Workflow Export**

### FRA — RFO workbook
**ONE sheet:** `Material Change in Process`

Inside that single sheet, the order should be:

1. **Landing Page**
2. **Details Panel**
3. **Landing Page Export**
4. **Workflow Export**

No separate sheets for these. No generic Common Functionality sheet. And **RFO does not have Initiate Risk Assessment**.

Also, I'll give it in the same normal format as before, with **Test Case ID | Test Scenario | Test Steps | Expected Result**, so you can manually enter each row.

## FRA — RFO — MATERIAL CHANGE IN PROCESS

### A. LANDING PAGE

| Test Case ID | Test Scenario | Test Steps | Expected Result |
|---|---|---|---|
| RFO-FRA-LP-001 | Verify FRA Landing Page access | Login as an RFO and navigate to Fraud Risk Assessment (FRA). | FRA Landing Page is displayed successfully and the RFO can access the applicable cases. |
| RFO-FRA-LP-002 | Verify My Cases view | Select My Cases on the FRA Landing Page. | Cases assigned or applicable to the logged-in RFO are displayed. |
| RFO-FRA-LP-003 | Verify All Cases view | Select All Cases, where available. | Only FRA cases that the RFO is authorised to access are displayed. |
| RFO-FRA-LP-004 | Verify Material Change in Process category | Select Material Change in Process from the Initiative Category filter/dropdown. | Material Change in Process cases are displayed in the data grid. |
| RFO-FRA-LP-005 | Verify Material Change in Process data grid | Review the Material Change in Process data grid. | Process Id, Project name, Process description, Background of process change, Rationale for FRA, Accountable executive or Key stakeholder, Contact point, Country coverage, Business function and CFCR RFO are displayed with the correct case values. |
| RFO-FRA-LP-006 | Verify Material Change in Process status display | Review cases under In Progress, Pending Endorsement, Refer Back, Endorsement by RFO and Completed statuses. | Each case is displayed under the correct status and the status matches the actual assessment state. |
| RFO-FRA-LP-007 | Verify Material Change in Process status counts | Compare the records displayed for each status with the corresponding status tile count. | Each status count matches the applicable RFO-accessible records. |
| RFO-FRA-LP-008 | Verify Material Change in Process grid search | Search using a valid Process Id and then enter a non-existing Process Id. | Matching Material Change in Process record is displayed for the valid Process Id and no matching record is displayed for the non-existing value. |
| RFO-FRA-LP-009 | Verify Material Change in Process grid filtering | Apply an available filter and then clear the filter. | Filtered records are displayed and all applicable records are restored after clearing the filter. |
| RFO-FRA-LP-010 | Verify Material Change in Process grid sorting | Sort a sortable column in ascending and descending order. | Records are displayed in the selected sort order. |
| RFO-FRA-LP-011 | Verify Material Change in Process pagination | Navigate through the available pages of the data grid. | Correct records are displayed on each page without duplication or omission. |
| RFO-FRA-LP-012 | Verify Material Change in Process horizontal scrolling | Scroll horizontally across the data grid. | All configured Material Change in Process columns are accessible. |
| RFO-FRA-LP-013 | Verify common case fields | Review Status, Created By, Created Date, Last Updated Date and Completed Date. | Each field displays the correct value for the selected assessment. |
| RFO-FRA-LP-014 | Verify Process Id display | Review the Process Id of a Material Change in Process case. | The correct Process Id associated with the assessment is displayed. |
| RFO-FRA-LP-015 | Verify Process description full text | Select Click to View for Process description, where available. | Popup opens and displays the complete Process description without unintended truncation. |
| RFO-FRA-LP-016 | Verify Background of process change full text | Select Click to View for Background of process change, where available. | Popup opens and displays the complete Background of process change without unintended truncation. |
| RFO-FRA-LP-017 | Verify Rationale for FRA full text | Select Click to View for Rationale for FRA, where available. | Popup opens and displays the complete Rationale for FRA without unintended truncation. |
| RFO-FRA-LP-018 | Verify Material Change in Process data accuracy | Compare Process Id, Project name, Process description, Background of process change, Rationale for FRA, Accountable executive or Key stakeholder, Contact point, Country coverage, Business function and CFCR RFO with the submitted assessment. | All Material Change in Process values displayed on the Landing Page match the submitted assessment. |
| RFO-FRA-LP-019 | Verify RFO read-only access | Attempt to edit Process Id, Project name, Process description, Background of process change, Rationale for FRA, Accountable executive or Key stakeholder, Contact point, Country coverage, Business function and CFCR RFO. | RFO cannot modify the PM-submitted Material Change in Process information. |

---

### B. DETAILS PANEL

| Test Case ID | Test Scenario | Test Steps | Expected Result |
|---|---|---|---|
| RFO-FRA-DET-001 | Verify Material Change in Process Details panel | Open a Material Change in Process assessment and open the Details panel. | Details panel opens successfully and displays the assessment information. |
| RFO-FRA-DET-002 | Verify Material Change in Process Details | Review Initiative Category, Process Id, Project name, Process description, Background of process change, Rationale for FRA, Accountable executive or Key stakeholder, Contact point, Country coverage, Business function and CFCR RFO. | All Material Change in Process information is displayed with the correct values submitted by the PM. |
| RFO-FRA-DET-003 | Verify common Details information | Review Case ID, Initiative Category, Status, Created By, Created Date, Last Updated Date and Completed Date. | All common Details information is displayed with the correct values. |
| RFO-FRA-DET-004 | Verify Process description in Details | Select Click to View for Process description in the Details panel. | Popup opens and displays the complete Process description without unintended truncation. |
| RFO-FRA-DET-005 | Verify Background of process change in Details | Select Click to View for Background of process change in the Details panel. | Popup opens and displays the complete Background of process change without unintended truncation. |
| RFO-FRA-DET-006 | Verify Rationale for FRA in Details | Select Click to View for Rationale for FRA in the Details panel. | Popup opens and displays the complete Rationale for FRA without unintended truncation. |
| RFO-FRA-DET-007 | Verify Material Change in Process Details read-only access | Attempt to modify the Material Change in Process information displayed in the Details panel. | RFO cannot modify the PM-submitted assessment information. |
| RFO-FRA-DET-008 | Verify Info tab | Select the Info tab. | Assessment information is displayed correctly. |
| RFO-FRA-DET-009 | Verify History tab | Select the History tab. | Assessment activity and history are displayed correctly. |

---

### C. LANDING PAGE EXPORT

| Test Case ID | Test Scenario | Test Steps | Expected Result |
|---|---|---|---|
| RFO-FRA-LPE-001 | Verify Landing Page Export availability | Open the FRA Landing Page as an RFO and select Material Change in Process. | Landing Page Export option is available according to RFO permissions. |
| RFO-FRA-LPE-002 | Verify Material Change in Process export generation | Select Export and open the downloaded file. | Export file is generated, downloaded and opened successfully. |
| RFO-FRA-LPE-003 | Verify Material Change in Process exported fields | Review Initiative Category, Process Id, Project name, Process description, Background of process change, Rationale for FRA, Accountable executive or Key stakeholder, Contact point, Country coverage, Business function and CFCR RFO in the export. | All exported Material Change in Process fields match the Landing Page data. |
| RFO-FRA-LPE-004 | Verify common exported fields | Review Status, Created By, Created Date, Last Updated Date and Completed Date in the export. | Common exported fields match the Landing Page data. |
| RFO-FRA-LPE-005 | Verify long-text export | Export a case containing long Process description, Background of process change and Rationale for FRA values. | Complete applicable long-text values are exported without unintended truncation. |
| RFO-FRA-LPE-006 | Verify filtered export | Apply a filter on the Material Change in Process Landing Page and export the results. | Export contains the records corresponding to the applied filter. |
| RFO-FRA-LPE-007 | Verify searched export | Search for a Material Change in Process case and export the results. | Export reflects the applicable searched records. |
| RFO-FRA-LPE-008 | Verify My Cases export | Select My Cases and export the Material Change in Process records. | Export contains only the Material Change in Process records available under My Cases. |
| RFO-FRA-LPE-009 | Verify All Cases export | Select All Cases, where available, and export the Material Change in Process records. | Export contains only the Material Change in Process records accessible to the RFO. |
| RFO-FRA-LPE-010 | Verify RFO export access control | Generate the Landing Page Export as an RFO. | Export contains only cases and information the RFO is authorised to access. |
| RFO-FRA-LPE-011 | Verify Landing Page export accuracy | Compare the exported Material Change in Process records with the Landing Page. | Exported data matches the corresponding Landing Page data. |

---

### D. WORKFLOW EXPORT

| Test Case ID | Test Scenario | Test Steps | Expected Result |
|---|---|---|---|
| RFO-FRA-WFE-001 | Verify Workflow Export availability | Open a Material Change in Process assessment as an RFO. | Workflow Export option is available according to RFO permissions. |
| RFO-FRA-WFE-002 | Verify Workflow Export generation | Select Workflow Export and open the downloaded file. | Workflow Export is generated, downloaded and opened successfully. |
| RFO-FRA-WFE-003 | Verify Material Change in Process Workflow Export fields | Review Initiative Category, Process Id, Project name, Process description, Background of process change, Rationale for FRA, Accountable executive or Key stakeholder, Contact point, Country coverage, Business function and CFCR RFO in the export. | Exported Material Change in Process values match the assessment. |
| RFO-FRA-WFE-004 | Verify common Workflow Export fields | Review Case ID, Initiative Category, Status, Created By, Created Date, Last Updated Date and Completed Date. | Exported common fields match the corresponding assessment information. |
| RFO-FRA-WFE-005 | Verify Risk Assessment information in Workflow Export | Review the Risk Assessment information available in the exported assessment. | Exported Risk Assessment information matches the information displayed to the RFO. |
| RFO-FRA-WFE-006 | Verify Mitigation Plan information in Workflow Export | Review the Mitigation Plan information available in the exported assessment. | Exported Mitigation Plan information matches the information displayed to the RFO. |
| RFO-FRA-WFE-007 | Verify RFO endorsement information in Workflow Export | Review CFCR RFO, RFO/Coverage status - 1LOD, RFO endorsement status and applicable RFO comments in the export. | Exported RFO endorsement information matches the assessment. |
| RFO-FRA-WFE-008 | Verify Refer Back information in Workflow Export | Export a Material Change in Process assessment that has been referred back. | Refer Back status and applicable comments are reflected correctly in the export. |
| RFO-FRA-WFE-009 | Verify long-text Workflow Export | Export an assessment containing long Process description, Background of process change and Rationale for FRA values. | Complete applicable long-text values are exported without unintended truncation. |
| RFO-FRA-WFE-010 | Verify RFO Workflow Export access control | Generate Workflow Export as an RFO. | Export contains only information that the RFO is authorised to view. |
| RFO-FRA-WFE-011 | Verify Workflow Export accuracy | Compare the Material Change in Process assessment with the exported file. | Exported data matches the corresponding assessment data. |

**This is the structure you should use now:** one `Material Change in Process` sheet for RFO, with these four sections in order. PM will have the same single sheet, but with **Initiate Risk Assessment placed second after Landing Page**.

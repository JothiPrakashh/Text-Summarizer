Yes. For **FRA → Material Change in Process**, keep **one sheet for PM** and **one sheet for RFO**.

For PM: **Landing Page → Initiate Risk Assessment → Details Panel → Landing Page Export → Workflow Export**

For RFO: **Landing Page → Details Panel → Risk Assessment Review → Mitigation Plan Review → Endorsement → Offline/Final → Landing Page Export → Workflow Export**

No separate common sheet and no unnecessary workflow cases.

---

# FRA — PM / MAKER — MATERIAL CHANGE IN PROCESS

## LANDING PAGE

| Test Case ID | Test Scenario | Test Steps | Expected Result |
|---|---|---|---|
| PM-FRA-LP-001 | Verify FRA Landing Page access | Login as a PM and navigate to FRA. | FRA Landing Page is displayed successfully. |
| PM-FRA-LP-002 | Verify My Cases view | Select My Cases. | Cases created/owned by the logged-in PM are displayed. |
| PM-FRA-LP-003 | Verify All Cases view | Select All Cases. | All FRA cases accessible to the PM are displayed. |
| PM-FRA-LP-004 | Verify Material Change in Process category | Select Material Change in Process from the Initiative Category filter. | Material Change in Process cases are displayed. |
| PM-FRA-LP-005 | Verify Material Change in Process data grid | Review the data grid for a Material Change in Process case. | Trigger event / driver, Process Id, Project name, Process description, Background of process change, Rationale for FRA, Accountable executive or Key stakeholder, Contact point, Country coverage, Business function and CFCR RFO are displayed with the correct values. |
| PM-FRA-LP-006 | Verify status display | Review Material Change in Process cases in In Progress, Pending Endorsement, Refer Back, Endorsement by RFO and Completed statuses. | Cases are displayed under the correct status. |
| PM-FRA-LP-007 | Verify status counts | Compare the status tile counts with the corresponding grid records. | Each status count matches the applicable records. |
| PM-FRA-LP-008 | Verify grid search | Search using a valid Process Id and then a non-existing Process Id. | Matching record is displayed for the valid value and no record is displayed for the non-existing value. |
| PM-FRA-LP-009 | Verify grid filtering | Apply an available filter and then clear it. | Filtered records are displayed and all applicable records are restored after clearing. |
| PM-FRA-LP-010 | Verify grid sorting | Sort a sortable column in ascending and descending order. | Records are displayed in the selected sort order. |
| PM-FRA-LP-011 | Verify pagination | Navigate through the available grid pages. | Correct records are displayed on each page without duplication or omission. |
| PM-FRA-LP-012 | Verify horizontal scrolling | Scroll horizontally across the grid. | All configured columns are accessible. |
| PM-FRA-LP-013 | Verify common case fields | Review Status, Created By, Created Date, Last Updated Date and Completed Date. | Each field displays the correct value. |
| PM-FRA-LP-014 | Verify Process description full text | Select Click to View for Process description. | Popup opens and displays the complete Process description without unintended truncation. |
| PM-FRA-LP-015 | Verify Background of process change full text | Select Click to View for Background of process change. | Popup opens and displays the complete Background of process change without unintended truncation. |
| PM-FRA-LP-016 | Verify Rationale for FRA full text | Select Click to View for Rationale for FRA. | Popup opens and displays the complete Rationale for FRA without unintended truncation. |
| PM-FRA-LP-017 | Verify Material Change in Process data accuracy | Compare the Landing Page values with the submitted assessment. | All displayed Material Change in Process values match the submitted assessment. |

## INITIATE RISK ASSESSMENT

| Test Case ID | Test Scenario | Test Steps | Expected Result |
|---|---|---|---|
| PM-FRA-INIT-001 | Verify Material Change in Process fields | Select Material Change in Process and review Trigger event / driver, Process Id, Project name, Process description, Background of process change, Rationale for FRA, Accountable executive or Key stakeholder, Contact point, Country coverage, Business function and CFCR RFO. | All configured Material Change in Process fields are displayed correctly. |
| PM-FRA-INIT-002 | Verify Trigger event / driver | Open Trigger event / driver and select an applicable value. | Available values are displayed and the selected value is retained. |
| PM-FRA-INIT-003 | Verify Process Id | Enter a valid Process Id. | Process Id is accepted and retained correctly. |
| PM-FRA-INIT-004 | Verify Process Id mandatory validation | Leave Process Id blank and attempt to proceed. | Mandatory validation is displayed and progression is prevented. |
| PM-FRA-INIT-005 | Verify Project name | Enter a valid Project name. | Project name is accepted and retained correctly. |
| PM-FRA-INIT-006 | Verify Process description mandatory validation | Leave Process description blank and attempt to proceed. | Mandatory validation is displayed and progression is prevented. |
| PM-FRA-INIT-007 | Verify Background of process change mandatory validation | Leave Background of process change blank and attempt to proceed. | Mandatory validation is displayed and progression is prevented. |
| PM-FRA-INIT-008 | Verify Rationale for FRA mandatory validation | Leave Rationale for FRA blank and attempt to proceed. | Mandatory validation is displayed and progression is prevented. |
| PM-FRA-INIT-009 | Verify Accountable executive or Key stakeholder | Search and select an Accountable executive or Key stakeholder using the employee/bank ID field. | Selected user is accepted and retained correctly. |
| PM-FRA-INIT-010 | Verify Contact point | Review the Contact point field after entering the applicable user information. | Contact point is populated according to configured logic. |
| PM-FRA-INIT-011 | Verify Country coverage | Select an applicable Country coverage value. | Selected Country coverage is retained correctly. |
| PM-FRA-INIT-012 | Verify Business function | Select an applicable Business function. | Selected Business function is retained correctly. |
| PM-FRA-INIT-013 | Verify CFCR RFO population | Select the applicable Business function and review CFCR RFO. | Applicable CFCR RFO is populated according to configured CRHS logic. |
| PM-FRA-INIT-014 | Verify mandatory validation | Leave required Material Change in Process fields blank and attempt to proceed. | Mandatory validation is displayed for the required fields and progression is prevented. |
| PM-FRA-INIT-015 | Verify Initiative data persistence | Enter the required information, save/navigate away and return to the assessment. | Previously entered values are retained correctly. |
| PM-FRA-INIT-016 | Verify Initiative submission | Complete all required fields and submit the Initiative. | Assessment is created successfully and progresses to the next configured FRA stage. |

## DETAILS PANEL

| Test Case ID | Test Scenario | Test Steps | Expected Result |
|---|---|---|---|
| PM-FRA-DET-001 | Verify Details panel | Open a Material Change in Process assessment and open Details. | Details panel opens successfully. |
| PM-FRA-DET-002 | Verify Material Change in Process Details | Review Trigger event / driver, Process Id, Project name, Process description, Background of process change, Rationale for FRA, Accountable executive or Key stakeholder, Contact point, Country coverage, Business function and CFCR RFO. | All Details display the submitted values correctly. |
| PM-FRA-DET-003 | Verify common Details | Review Case ID, Initiative Category, Status, Created By, Created Date, Last Updated Date and Completed Date. | All common Details display the correct values. |
| PM-FRA-DET-004 | Verify Process description in Details | Select Click to View for Process description. | Complete Process description is displayed without unintended truncation. |
| PM-FRA-DET-005 | Verify Background of process change in Details | Select Click to View for Background of process change. | Complete Background of process change is displayed without unintended truncation. |
| PM-FRA-DET-006 | Verify Rationale for FRA in Details | Select Click to View for Rationale for FRA. | Complete Rationale for FRA is displayed without unintended truncation. |
| PM-FRA-DET-007 | Verify Info tab | Select Info. | Assessment information is displayed correctly. |
| PM-FRA-DET-008 | Verify History tab | Select History. | Assessment activity/history is displayed correctly. |

## LANDING PAGE EXPORT

| Test Case ID | Test Scenario | Test Steps | Expected Result |
|---|---|---|---|
| PM-FRA-LPE-001 | Verify Landing Page Export availability | Select Material Change in Process and open Export. | Landing Page Export is available. |
| PM-FRA-LPE-002 | Verify export generation | Select Export and open the downloaded file. | Export file is generated, downloaded and opened successfully. |
| PM-FRA-LPE-003 | Verify exported Material Change in Process fields | Review Trigger event / driver, Process Id, Project name, Process description, Background of process change, Rationale for FRA, Accountable executive or Key stakeholder, Contact point, Country coverage, Business function and CFCR RFO. | Exported values match the Landing Page. |
| PM-FRA-LPE-004 | Verify common exported fields | Review Status, Created By, Created Date, Last Updated Date and Completed Date. | Common exported fields match the Landing Page. |
| PM-FRA-LPE-005 | Verify long-text export | Export a case containing long Process description, Background of process change and Rationale for FRA. | Complete long-text values are exported without unintended truncation. |
| PM-FRA-LPE-006 | Verify filtered export | Apply a filter and export the results. | Export contains the records corresponding to the applied filter. |
| PM-FRA-LPE-007 | Verify searched export | Search for a Material Change in Process case and export. | Export reflects the searched records. |
| PM-FRA-LPE-008 | Verify My Cases export | Select My Cases and export. | Export contains applicable My Cases records. |
| PM-FRA-LPE-009 | Verify All Cases export | Select All Cases and export. | Export contains applicable All Cases records. |
| PM-FRA-LPE-010 | Verify Landing Page export accuracy | Compare exported data with the Landing Page. | Exported data matches the corresponding Landing Page data. |

## WORKFLOW EXPORT

| Test Case ID | Test Scenario | Test Steps | Expected Result |
|---|---|---|---|
| PM-FRA-WFE-001 | Verify Workflow Export availability | Open a Material Change in Process assessment and select Workflow Export. | Workflow Export is available. |
| PM-FRA-WFE-002 | Verify Workflow Export generation | Select Workflow Export and open the downloaded file. | Workflow Export is generated, downloaded and opened successfully. |
| PM-FRA-WFE-003 | Verify Material Change in Process Workflow Export fields | Review Trigger event / driver, Process Id, Project name, Process description, Background of process change, Rationale for FRA, Accountable executive or Key stakeholder, Contact point, Country coverage, Business function and CFCR RFO. | Exported values match the assessment. |
| PM-FRA-WFE-004 | Verify common Workflow Export fields | Review Case ID, Initiative Category, Status, Created By, Created Date, Last Updated Date and Completed Date. | Exported common fields match the assessment. |
| PM-FRA-WFE-005 | Verify Risk Assessment export | Review the Risk Assessment information in the Workflow Export. | Exported Risk Assessment information matches the assessment. |
| PM-FRA-WFE-006 | Verify Mitigation Plan export | Review the Mitigation Plan information in the Workflow Export. | Exported Mitigation Plan information matches the assessment. |
| PM-FRA-WFE-007 | Verify RFO endorsement export | Review CFCR RFO, RFO/Coverage status - 1LOD, RFO endorsement status and applicable RFO comments. | Exported endorsement information matches the assessment. |
| PM-FRA-WFE-008 | Verify Refer Back export | Export an assessment that has been referred back. | Refer Back status and applicable comments are displayed correctly. |
| PM-FRA-WFE-009 | Verify long-text Workflow Export | Export an assessment containing long Process description, Background of process change and Rationale for FRA. | Complete long-text values are exported without unintended truncation. |
| PM-FRA-WFE-010 | Verify Workflow Export accuracy | Compare assessment data with the Workflow Export. | Exported data matches the assessment. |

---

# FRA — RFO / REVIEWER — MATERIAL CHANGE IN PROCESS

## LANDING PAGE

| Test Case ID | Test Scenario | Test Steps | Expected Result |
|---|---|---|---|
| RFO-FRA-LP-001 | Verify FRA Landing Page access | Login as an RFO and navigate to FRA. | FRA Landing Page is displayed successfully. |
| RFO-FRA-LP-002 | Verify My Cases view | Select My Cases. | FRA cases assigned/relevant to the logged-in RFO are displayed. |
| RFO-FRA-LP-003 | Verify All Cases view | Select All Cases where available. | All FRA cases accessible to the RFO are displayed. |
| RFO-FRA-LP-004 | Verify Material Change in Process category | Select Material Change in Process from the Initiative Category filter. | Material Change in Process cases accessible to the RFO are displayed. |
| RFO-FRA-LP-005 | Verify Material Change in Process data grid | Review the data grid for a Material Change in Process case. | Trigger event / driver, Process Id, Project name, Process description, Background of process change, Rationale for FRA, Accountable executive or Key stakeholder, Contact point, Country coverage, Business function and CFCR RFO are displayed with the correct values. |
| RFO-FRA-LP-006 | Verify status display | Review Material Change in Process cases in In Progress, Pending Endorsement, Refer Back, Endorsement by RFO and Completed statuses. | Cases are displayed under the correct status. |
| RFO-FRA-LP-007 | Verify status counts | Compare status tile counts with the corresponding grid records. | Each status count matches the applicable records. |
| RFO-FRA-LP-008 | Verify grid search | Search using a valid Process Id and then a non-existing Process Id. | Matching record is displayed for the valid value and no record is displayed for the non-existing value. |
| RFO-FRA-LP-009 | Verify grid filtering | Apply an available filter and then clear it. | Filtered records are displayed and applicable records are restored after clearing. |
| RFO-FRA-LP-010 | Verify grid sorting | Sort a sortable column in ascending and descending order. | Records are displayed in the selected sort order. |
| RFO-FRA-LP-011 | Verify pagination and horizontal scrolling | Navigate through grid pages and scroll horizontally. | Correct records are displayed and all configured columns are accessible. |
| RFO-FRA-LP-012 | Verify common case fields | Review Status, Created By, Created Date, Last Updated Date and Completed Date. | Each field displays the correct value. |
| RFO-FRA-LP-013 | Verify Process description full text | Select Click to View for Process description. | Complete Process description is displayed without unintended truncation. |
| RFO-FRA-LP-014 | Verify Background of process change full text | Select Click to View for Background of process change. | Complete Background of process change is displayed without unintended truncation. |
| RFO-FRA-LP-015 | Verify Rationale for FRA full text | Select Click to View for Rationale for FRA. | Complete Rationale for FRA is displayed without unintended truncation. |
| RFO-FRA-LP-016 | Verify RFO Landing Page data accuracy | Compare displayed Material Change in Process values with the assessment. | Displayed values match the assessment. |

## DETAILS PANEL

| Test Case ID | Test Scenario | Test Steps | Expected Result |
|---|---|---|---|
| RFO-FRA-DET-001 | Verify Details panel | Open an assigned Material Change in Process assessment and open Details. | Details panel opens successfully. |
| RFO-FRA-DET-002 | Verify Material Change in Process Details | Review Trigger event / driver, Process Id, Project name, Process description, Background of process change, Rationale for FRA, Accountable executive or Key stakeholder, Contact point, Country coverage, Business function and CFCR RFO. | All Details display the correct submitted values. |
| RFO-FRA-DET-003 | Verify common Details | Review Case ID, Initiative Category, Status, Created By, Created Date, Last Updated Date and Completed Date. | All common Details display the correct values. |
| RFO-FRA-DET-004 | Verify long-text Details | Select Click to View for Process description, Background of process change and Rationale for FRA. | Each popup opens and displays the complete underlying text without unintended truncation. |
| RFO-FRA-DET-005 | Verify Info tab | Select Info. | Assessment information is displayed correctly. |
| RFO-FRA-DET-006 | Verify History tab | Select History. | Assessment activity/history is displayed correctly. |
| RFO-FRA-DET-007 | Verify RFO read-only access | Attempt to edit Material Change in Process Initiative information as an RFO. | RFO cannot modify the PM-entered Initiative information. |

## RISK ASSESSMENT REVIEW

| Test Case ID | Test Scenario | Test Steps | Expected Result |
|---|---|---|---|
| RFO-FRA-RA-001 | Verify Risk Assessment stage | Open an assigned assessment that has reached Risk Assessment. | Risk Assessment stage is displayed. |
| RFO-FRA-RA-002 | Verify Initiative information carry-forward | Review the Material Change in Process information carried forward from Initiative. | Submitted Initiative information is displayed correctly. |
| RFO-FRA-RA-003 | Verify Risk Assessment responses | Review the Risk Assessment responses entered by the PM. | Risk Assessment responses are displayed correctly. |
| RFO-FRA-RA-004 | Verify RFO read-only Risk Assessment | Attempt to modify Risk Assessment responses. | RFO cannot modify the PM-entered Risk Assessment responses. |
| RFO-FRA-RA-005 | Verify Risk Assessment data accuracy | Compare displayed Risk Assessment information with the submitted assessment. | Risk Assessment information matches the assessment. |

## MITIGATION PLAN REVIEW

| Test Case ID | Test Scenario | Test Steps | Expected Result |
|---|---|---|---|
| RFO-FRA-MP-001 | Verify Mitigation Plan information | Review Target, Action Owner, Status, Supporting Document and mitigation-to-question mapping. | Mitigation Plan information is displayed correctly. |
| RFO-FRA-MP-002 | Verify Action Owner | Review the selected Action Owner. | PM or RFO selection is displayed correctly. |
| RFO-FRA-MP-003 | Verify Supporting Document | Open the Supporting Document associated with the Mitigation Plan. | Supporting Document is accessible and associated with the correct assessment. |
| RFO-FRA-MP-004 | Verify mitigation plan mapping | Review the questions mapped to the Mitigation Plan. | Configured mitigation-to-question mapping is displayed correctly. |
| RFO-FRA-MP-005 | Verify RFO read-only Mitigation Plan | Attempt to modify Mitigation Plan information. | RFO cannot modify the PM-entered Mitigation Plan information. |

## ENDORSEMENT

| Test Case ID | Test Scenario | Test Steps | Expected Result |
|---|---|---|---|
| RFO-FRA-END-001 | Verify RFO/Coverage status - 1LOD | Open the endorsement section and review RFO/Coverage status - 1LOD. | Correct RFO/Coverage status is displayed. |
| RFO-FRA-END-002 | Verify RFO endorsement information | Review RFO endorsement status and applicable RFO information. | Current endorsement information is displayed correctly. |
| RFO-FRA-END-003 | Verify Endorse action | Select Endorse for the assigned assessment. | Endorse action is available and can be selected. |
| RFO-FRA-END-004 | Verify endorsement comments | Enter endorsement comments where applicable and submit. | Comments are saved and associated with the endorsement. |
| RFO-FRA-END-005 | Verify endorsement without optional comments | Select Endorse without entering optional comments and submit. | Endorsement is submitted successfully when comments are optional. |
| RFO-FRA-END-006 | Verify endorsement submission | Complete the required endorsement action and submit. | RFO endorsement is recorded successfully. |
| RFO-FRA-END-007 | Verify endorsement status update | Return to the assessment after endorsing. | RFO endorsement status is updated correctly. |
| RFO-FRA-END-008 | Verify Refer Back validation | Select Refer Back without entering comments and attempt to submit. | Mandatory validation is displayed and Refer Back submission is prevented. |
| RFO-FRA-END-009 | Verify Refer Back submission | Select Refer Back, enter the required comments and submit. | Assessment moves to Refer Back and the comments are recorded. |
| RFO-FRA-END-010 | Verify multiple RFO endorsement tracking | Use an assessment with multiple assigned RFOs and complete one RFO endorsement. | Completed RFO endorsement is recorded while remaining RFO endorsements remain pending. |
| RFO-FRA-END-011 | Verify all RFO endorsements | Complete all required RFO endorsements. | All required RFO endorsements are recorded and the assessment progresses according to the configured workflow. |
| RFO-FRA-END-012 | Verify PM visibility of endorsement outcome | Complete an endorsement and review the assessment from the PM side. | PM can see the updated RFO endorsement outcome. |

## OFFLINE / FINAL

| Test Case ID | Test Scenario | Test Steps | Expected Result |
|---|---|---|---|
| RFO-FRA-FIN-001 | Verify Offline Endorsement | Open an assessment requiring Offline Endorsement. | Offline Endorsement functionality is available where applicable. |
| RFO-FRA-FIN-002 | Verify Offline Endorsement evidence | Review the uploaded Offline Endorsement evidence. | Evidence is accessible and associated with the correct assessment. |
| RFO-FRA-FIN-003 | Verify final endorsed assessment | Complete the required endorsement activities. | Assessment reaches the configured final endorsed stage. |
| RFO-FRA-FIN-004 | Verify final assessment information | Review the final assessment information after endorsement. | Final assessment information is displayed correctly. |
| RFO-FRA-FIN-005 | Verify completion | Complete all required final activities. | Assessment reaches Completed status according to the configured workflow. |
| RFO-FRA-FIN-006 | Verify Completed Date | Open the completed assessment. | Completed Date is populated correctly. |
| RFO-FRA-FIN-007 | Verify completion History | Open History for the completed assessment. | Final endorsement, submission and completion activities are recorded. |

## LANDING PAGE EXPORT

| Test Case ID | Test Scenario | Test Steps | Expected Result |
|---|---|---|---|
| RFO-FRA-LPE-001 | Verify Landing Page Export availability | Select Material Change in Process and open Export. | Landing Page Export is available to the RFO. |
| RFO-FRA-LPE-002 | Verify export generation | Select Export and open the downloaded file. | Export file is generated, downloaded and opened successfully. |
| RFO-FRA-LPE-003 | Verify exported Material Change in Process fields | Review Trigger event / driver, Process Id, Project name, Process description, Background of process change, Rationale for FRA, Accountable executive or Key stakeholder, Contact point, Country coverage, Business function and CFCR RFO. | Exported values match the Landing Page data. |
| RFO-FRA-LPE-004 | Verify common exported fields | Review Status, Created By, Created Date, Last Updated Date and Completed Date. | Common exported fields match the Landing Page data. |
| RFO-FRA-LPE-005 | Verify long-text export | Export a case containing long Process description, Background of process change and Rationale for FRA. | Complete long-text values are exported without unintended truncation. |
| RFO-FRA-LPE-006 | Verify filtered export | Apply a filter and export the results. | Export contains the applicable filtered records. |
| RFO-FRA-LPE-007 | Verify searched export | Search for a Material Change in Process case and export. | Export reflects the searched records. |
| RFO-FRA-LPE-008 | Verify RFO access control for export | Attempt to export records outside the RFO's permitted access. | RFO can export only records permitted by the configured access controls. |
| RFO-FRA-LPE-009 | Verify Landing Page export accuracy | Compare exported data with the Landing Page. | Exported data matches the corresponding Landing Page data. |

## WORKFLOW EXPORT

| Test Case ID | Test Scenario | Test Steps | Expected Result |
|---|---|---|---|
| RFO-FRA-WFE-001 | Verify Workflow Export availability | Open an assigned Material Change in Process assessment and select Workflow Export. | Workflow Export is available. |
| RFO-FRA-WFE-002 | Verify Workflow Export generation | Select Workflow Export and open the downloaded file. | Workflow Export is generated, downloaded and opened successfully. |
| RFO-FRA-WFE-003 | Verify Material Change in Process Workflow Export fields | Review Trigger event / driver, Process Id, Project name, Process description, Background of process change, Rationale for FRA, Accountable executive or Key stakeholder, Contact point, Country coverage, Business function and CFCR RFO. | Exported values match the assessment. |
| RFO-FRA-WFE-004 | Verify common Workflow Export fields | Review Case ID, Initiative Category, Status, Created By, Created Date, Last Updated Date and Completed Date. | Exported common fields match the assessment. |
| RFO-FRA-WFE-005 | Verify Risk Assessment Workflow Export | Review the Risk Assessment information in the export. | Exported Risk Assessment information matches the assessment. |
| RFO-FRA-WFE-006 | Verify Mitigation Plan Workflow Export | Review Target, Action Owner, Status, Supporting Document and mitigation-to-question mapping. | Exported Mitigation Plan information matches the assessment. |
| RFO-FRA-WFE-007 | Verify RFO endorsement Workflow Export | Review CFCR RFO, RFO/Coverage status - 1LOD, RFO endorsement status and applicable comments. | Exported endorsement information matches the assessment. |
| RFO-FRA-WFE-008 | Verify Refer Back Workflow Export | Export an assessment that has been referred back. | Refer Back status and applicable comments are reflected correctly. |
| RFO-FRA-WFE-009 | Verify long-text Workflow Export | Export an assessment containing long Process description, Background of process change and Rationale for FRA. | Complete long-text values are exported without unintended truncation. |
| RFO-FRA-WFE-010 | Verify RFO Workflow Export access control | Attempt to export an assessment outside the RFO's permitted access. | RFO can export only permitted assessment data. |
| RFO-FRA-WFE-011 | Verify Workflow Export accuracy | Compare the assessment with the exported file. | Exported data matches the corresponding assessment data. |

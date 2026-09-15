Yes. Let’s restructure the PM workbook category-wise now. I would not repeat the common workflow test cases under all four categories—that would unnecessarily inflate the workbook.

Final PM workbook structure

1. Common Functionality
2. New Product - Product Change
3. Corporate Action
4. NICRA
5. Other

Columns:

Test Case ID | Test Scenario | Test Steps | Expected Result

The category sheets contain everything specific to that category. The common sheet contains functionality applicable across all categories.

⸻

SHEET 1 — COMMON FUNCTIONALITY

A. Landing Page — Common

Test Case ID	Test Scenario	Test Steps	Expected Result
PM-LP-001	Verify COI Landing Page access	Login as PM and navigate to COI.	COI Landing Page is displayed successfully.
PM-LP-002	Verify My Cases and All Cases views	Select My Cases and then All Cases.	My Cases displays PM-created/owned applicable cases and All Cases displays all cases accessible to the PM.
PM-LP-003	Verify switching between My Cases and All Cases	Switch between My Cases and All Cases.	Grid refreshes correctly based on the selected view.
PM-LP-004	Verify Initiative Category selection	Open the Initiative Category dropdown.	New Product / Product Change, Corporate Action, NICRA and Other categories are displayed.
PM-LP-005	Verify category selection and grid refresh	Select New Product / Product Change, Corporate Action, NICRA and Other individually.	Applicable records and category-specific columns are displayed for the selected category.
PM-LP-006	Verify status tiles	Select In Progress, Pending Endorsement, Refer Back, Endorsement by RFO and Completed individually.	Cases corresponding to the selected status are displayed.
PM-LP-007	Verify status tile counts	Compare the counts on In Progress, Pending Endorsement, Refer Back, Endorsement by RFO and Completed with the corresponding grid records.	Each status tile count matches the applicable records.
PM-LP-008	Verify search functionality	Enter a valid searchable value and then a non-existing value.	Matching records are displayed for a valid value and no matching records are displayed for a non-existing value.
PM-LP-009	Verify grid filtering	Apply an applicable filter and then clear the filter.	Matching records are displayed after filtering and applicable records are restored after clearing the filter.
PM-LP-010	Verify grid sorting	Sort a sortable column in ascending and descending order.	Records are displayed in the selected sort order.
PM-LP-011	Verify pagination	Navigate through the available grid pages.	Correct records are displayed on each page without duplication or omission.
PM-LP-012	Verify horizontal scrolling	Scroll horizontally across the grid.	All configured grid columns are accessible.

⸻

B. Workflow / Details — Common

Test Case ID	Test Scenario	Test Steps	Expected Result
PM-WF-001	Verify assessment opening	Select a COI case from the Landing Page.	Selected assessment opens successfully.
PM-WF-002	Verify workflow stages and current stage	Review the workflow progress indicator.	Configured COI workflow stages are displayed and the current stage is highlighted.
PM-WF-003	Verify current status and available actions	Review the assessment status and available actions.	Current Status and applicable PM actions are displayed according to the assessment state.
PM-WF-004	Verify Details panel	Open the Details panel.	Details panel opens and displays assessment information.
PM-WF-005	Verify common Details information	Review Case ID, Initiative Category, Status, Created By, Created Date, Last Updated Date and Completed Date.	All common Details information is displayed with the correct values.
PM-WF-012	Verify Info tab	Select Info.	Assessment information is displayed correctly.
PM-WF-013	Verify History tab	Select History.	Assessment activity/history is displayed correctly.

⸻

C. Risk Assessment — Common

Test Case ID	Test Scenario	Test Steps	Expected Result
PM-RA-001	Verify Risk Assessment stage	Open an assessment that has progressed from Initiative.	Risk Assessment stage is displayed.
PM-RA-002	Verify Initiative information carry-forward	Review information carried forward from the Initiative stage.	Relevant submitted Initiative information is retained correctly.
PM-RA-003	Verify Potential COI Risk response	Review Potential COI Risk and select Yes/No in applicable test scenarios.	Potential COI Risk response is saved correctly.
PM-RA-004	Verify Potential COI Risk dependent validation	Select Potential COI Risk = Yes and attempt to proceed without required dependent information.	Required COI risk information must be completed before progression.
PM-RA-005	Verify Potential COI Risk = No behaviour	Select Potential COI Risk = No and proceed.	Dependent COI risk information is not required and assessment can proceed.
PM-RA-006	Verify Risk Assessment response persistence	Enter responses, save/navigate away and reopen the assessment.	Previously entered Risk Assessment responses are retained.
PM-RA-007	Verify Risk Assessment submission	Complete required Risk Assessment information and submit.	Assessment progresses to the Mitigation Plan stage.

⸻

D. Mitigation Plan — Common

Test Case ID	Test Scenario	Test Steps	Expected Result
PM-MP-001	Verify Mitigation Plan fields and behaviour	Open Mitigation Plan and review Target, Action Owner, Status and Supporting Document.	Configured Mitigation Plan fields are displayed and behave correctly.
PM-MP-002	Verify Action Owner selection	Select PM and RFO as Action Owner in applicable scenarios.	Selected Action Owner is saved and displayed correctly.
PM-MP-003	Verify Mitigation Plan Status	Select each applicable Mitigation Plan Status.	Selected Status is saved correctly.
PM-MP-004	Verify Supporting Document	Upload a supporting document and review the saved assessment.	Supporting document uploads successfully and is associated with the assessment.
PM-MP-005	Verify optional Supporting Document	Leave Supporting Document blank where it is optional and proceed.	Assessment can proceed without Supporting Document where permitted.
PM-MP-006	Verify mitigation plan mapping	Map a mitigation plan to one and then multiple applicable questions.	A mitigation plan can be mapped to the permitted question(s), including multiple applicable questions where configured.
PM-MP-007	Verify Mitigation Plan persistence	Save and reopen the Mitigation Plan.	Target, Action Owner, Status, Supporting Document and mapping information are retained.
PM-MP-008	Verify Mitigation Plan submission	Complete required Mitigation Plan information and submit.	Assessment progresses to Pending Endorsement.

⸻

E. Pending Endorsement / Final — Common

Test Case ID	Test Scenario	Test Steps	Expected Result
PM-PE-001	Verify Pending Endorsement stage	Submit the completed assessment for endorsement.	Assessment moves to Pending Endorsement.
PM-PE-002	Verify RFO assignment and endorsement information	Review CFCR RFOs, RFO/Coverage status - 1LOD and RFO endorsement status.	Applicable RFOs and their current endorsement/coverage statuses are displayed correctly.
PM-PE-003	Verify RFO coverage comments	Review RFO coverage comments for an assessment where comments are provided.	RFO coverage comments are displayed correctly.
PM-PE-004	Verify endorsement completion	Complete required RFO endorsements.	Individual endorsement statuses are updated and completion is recognised once all required endorsements are completed.
PM-PE-005	Verify multiple RFO endorsement tracking	Use an assessment with multiple assigned RFOs and complete one endorsement.	Completed RFO endorsement is recorded while remaining required RFO endorsements remain pending.
PM-PE-006	Verify Refer Back	Have an RFO refer the assessment back with comments.	Assessment moves to Refer Back and the RFO comments are displayed to PM.
PM-PE-007	Verify PM update after Refer Back	Update permitted assessment information and resubmit.	PM can update permitted information and resubmit the assessment for RFO review.
PM-FIN-001	Verify Offline Endorsement	Open an assessment requiring Offline Endorsement.	Offline Endorsement functionality is available where applicable.
PM-FIN-002	Verify Offline Endorsement evidence	Upload the required Offline Endorsement evidence and reopen the assessment.	Evidence is uploaded successfully and associated with the correct assessment.
PM-FIN-003	Verify final endorsement status	Complete all required endorsement activities.	Assessment reaches the configured final endorsed stage.
PM-FIN-004	Verify final submission	Complete the required final action and submit.	Assessment is submitted successfully.
PM-FIN-005	Verify Completed status and date	Return to the Landing Page and open the completed assessment.	Assessment displays Completed status and the Completed Date is populated correctly.
PM-FIN-006	Verify completion history	Open the History tab of the completed assessment.	Final submission, endorsement and completion activities are recorded in History.

⸻

F. Export — Common

Test Case ID	Test Scenario	Test Steps	Expected Result
PM-LPE-001	Verify Landing Page Export availability	Open the COI Landing Page.	Export option is available to PM.
PM-LPE-002	Verify category-wise export	Select each category and select Export.	Data for the selected category is exported successfully.
PM-LPE-003	Verify export download and file opening	Select Export and open the downloaded file.	Export file downloads and opens successfully.
PM-LPE-008	Verify common exported fields	Review Status, Created By, Created Date, Last Updated Date and Completed Date in the export.	Common fields match the Landing Page data.
PM-LPE-010	Verify My Cases export	Select My Cases and export.	Export contains records applicable to My Cases.
PM-LPE-011	Verify All Cases export	Select All Cases and export.	Export contains records applicable to All Cases.
PM-LPE-012	Verify filtered export	Apply a grid filter and select Export.	Export contains data corresponding to the applied filter.
PM-LPE-013	Verify searched export	Apply a search and select Export.	Export reflects the applicable search results.
PM-LPE-014	Verify Landing Page export accuracy	Compare exported records and fields with the Landing Page.	Exported data matches the corresponding Landing Page data.
PM-WFE-001	Verify Workflow Export availability	Open a COI workflow as PM.	Workflow Export option is available.
PM-WFE-002	Verify Workflow Export generation	Select Workflow Export.	Workflow export is generated and downloaded successfully.
PM-WFE-003	Verify common Workflow Export fields	Review Case ID, Initiative Category, Status, Created By, Created Date, Last Updated Date and Completed Date.	Exported common fields match the workflow.
PM-WFE-012	Verify Workflow Export accuracy	Compare the complete workflow with the exported file.	Exported data matches the corresponding workflow data.

⸻

SHEET 2 — NEW PRODUCT - PRODUCT CHANGE

A. Initiative

ID	Test Scenario	Test Steps	Expected Result
PM-INIT-001	Verify New Product / Product Change Initiative fields and behaviour	Select New Product / Product Change and review Programme code, Programme Name, Product manager, Business head / Product head, Business line, CFCR RFO, Product description & scope, Applicable to – Islamic variant and Applicable to – Sustainable finance variant.	All configured fields are displayed and behave according to the BRD.
PM-INIT-002	Verify New Product / Product Change mandatory validation	Leave mandatory fields blank and attempt to proceed.	Mandatory validation prevents progression until required fields are completed.
PM-INIT-003	Verify Programme code validation	Enter valid and invalid Programme code values.	Valid Programme code is accepted and invalid format/character values are rejected according to configured rules.
PM-INIT-004	Verify PSID and RFO population	Review Product manager, Business head / Product head and CFCR RFO population.	Product manager/Business head or Product head are populated through configured PSID logic and CFCR RFO is populated according to CRHS logic.
PM-INIT-005	Verify Business line selection	Select a Business line.	Valid Business line can be selected and retained.
PM-INIT-006	Verify Product description & scope	Enter Product description & scope and attempt to proceed without it.	Product description & scope is accepted when provided and mandatory validation is applied when required.
PM-INIT-007	Verify Applicable to selections	Select Islamic variant and/or Sustainable finance variant as applicable.	Selected Applicable to values are saved correctly.
PM-INIT-021	Verify Initiative submission	Complete all mandatory fields and submit.	Assessment is created successfully and progresses to Risk Assessment.

B. Landing Page

ID	Test Scenario	Test Steps	Expected Result
PM-NP-LP-001	Verify New Product / Product Change category fields	Select New Product / Product Change and review the grid.	Programme code, Programme Name, Product manager, Business head / Product head, Business line, CFCR RFO, Product description & scope, Applicable to – Islamic variant and Applicable to – Sustainable finance variant display with correct case values.
PM-NP-LP-002	Verify New Product / Product Change common fields	Review Status, Created By, Created Date, Last Updated Date and Completed Date.	Common fields display correct values.
PM-NP-LP-003	Verify Programme code display and format	Review Programme code for a valid case.	Programme code is displayed in configured PPG-XXXXX format and follows defined character rules.
PM-NP-LP-004	Verify Product description & scope full text	Select Click to View for Product description & scope.	Popup opens and displays the complete Product description & scope without unintended truncation.
PM-NP-LP-005	Verify New Product / Product Change field data accuracy	Compare category-specific fields with submitted assessment data.	All displayed New Product / Product Change field values match the submitted assessment data.

C. Details Panel

ID	Test Scenario	Test Steps	Expected Result
PM-WF-006	Verify New Product / Product Change Details	Review Programme code, Programme Name, Product manager, Business head / Product head, Business line, CFCR RFO, Product description & scope, Applicable to – Islamic variant and Applicable to – Sustainable finance variant.	All applicable New Product / Product Change Details match the submitted assessment.
PM-WF-010	Verify Product description & scope in Details	Select Click to View for Product description & scope in Details.	Popup opens and displays the complete underlying text.

D. Landing Page Export

ID	Test Scenario	Test Steps	Expected Result
PM-LPE-004	Verify New Product / Product Change exported fields	Export New Product / Product Change and review Programme code, Programme Name, Product manager, Business head / Product head, Business line, CFCR RFO, Product description & scope, Applicable to – Islamic variant and Applicable to – Sustainable finance variant.	Exported fields match the Landing Page data.
PM-LPE-009	Verify New Product long-text export	Export a case containing long Product description & scope.	Complete Product description & scope is exported without unintended truncation.

E. Workflow Export

ID	Test Scenario	Test Steps	Expected Result
PM-WFE-004	Verify New Product / Product Change Workflow Export fields	Review Programme code, Programme Name, Product manager, Business head / Product head, Business line, CFCR RFO, Product description & scope, Applicable to – Islamic variant and Applicable to – Sustainable finance variant.	Exported fields match workflow data.
PM-WFE-011	Verify New Product long-text Workflow Export	Export an assessment containing long Product description & scope.	Complete Product description & scope is exported without unintended truncation.

⸻

SHEET 3 — CORPORATE ACTION

A. Initiative

ID	Test Scenario	Test Steps	Expected Result
PM-INIT-008	Verify Corporate Action Initiative fields and behaviour	Select Corporate Action and review Project Name, Transaction, Rationale, Responsible Person, Accountable Executive, MT Sponsor, Business/Function and CFCR RFOs.	All configured Corporate Action fields are displayed and behave according to the BRD.
PM-INIT-009	Verify Corporate Action mandatory validation	Leave mandatory Corporate Action fields blank and attempt to proceed.	Mandatory validation prevents progression until required fields are completed.
PM-INIT-010	Verify Corporate Action PSID fields	Select/review Responsible Person, Accountable Executive and MT Sponsor using PSID.	Correct users are populated through configured PSID logic.
PM-INIT-011	Verify Corporate Action Business/Function and CFCR RFOs	Select multiple Business/Function values and review CFCR RFOs.	Multiple Business/Function values can be selected and applicable CFCR RFOs are populated according to CRHS logic.
PM-INIT-021	Verify Initiative submission	Complete all mandatory fields and submit.	Assessment is created successfully and progresses to Risk Assessment.

B. Landing Page

ID	Test Scenario	Test Steps	Expected Result
PM-CA-LP-001	Verify Corporate Action category fields	Select Corporate Action and review the grid.	Project Name, Transaction, Rationale, Responsible Person, Accountable Executive, MT Sponsor, Business/Function and CFCR RFOs display correct values.
PM-CA-LP-002	Verify Corporate Action common fields	Review Status, Created By, Created Date, Last Updated Date and Completed Date.	Common fields display correct values.
PM-CA-LP-003	Verify multiple Business/Function and CFCR RFOs	Open a Corporate Action case with multiple selections.	All selected Business/Function and CFCR RFOs values are displayed correctly.
PM-CA-LP-004	Verify Transaction Click to View	Select Click to View for Transaction.	Transaction popup opens successfully.
PM-CA-LP-005	Verify Transaction popup content	Review the Transaction popup.	Complete Transaction description is displayed without unintended truncation.
PM-CA-LP-006	Verify Rationale Click to View	Select Click to View for Rationale.	Rationale popup opens successfully.
PM-CA-LP-007	Verify Rationale popup content	Review the Rationale popup.	Complete Rationale description is displayed without unintended truncation.
PM-CA-LP-008	Verify Corporate Action field data accuracy	Compare Project Name, Transaction, Rationale, Responsible Person, Accountable Executive, MT Sponsor, Business/Function and CFCR RFOs with submitted data.	All Corporate Action field values match submitted assessment data.

C. Details

ID	Test Scenario	Test Steps	Expected Result
PM-WF-007	Verify Corporate Action Details	Review Project Name, Transaction, Rationale, Responsible Person, Accountable Executive, MT Sponsor, Business/Function and CFCR RFOs.	All applicable Corporate Action Details match submitted assessment.
PM-WF-010	Verify Transaction Click to View in Details	Select Click to View for Transaction.	Transaction popup opens and displays complete Transaction description.
PM-WF-011	Verify Rationale Click to View in Details	Select Click to View for Rationale.	Rationale popup opens and displays complete Rationale description.

D. Exports

ID	Test Scenario	Test Steps	Expected Result
PM-LPE-005	Verify Corporate Action exported fields	Export Corporate Action and review Project Name, Transaction, Rationale, Responsible Person, Accountable Executive, MT Sponsor, Business/Function and CFCR RFOs.	Exported fields match Landing Page data.
PM-LPE-009	Verify Corporate Action long-text export	Export a case containing long Transaction and Rationale values.	Complete applicable long-text values are exported without unintended truncation.
PM-WFE-005	Verify Corporate Action Workflow Export fields	Review Project Name, Transaction, Rationale, Responsible Person, Accountable Executive, MT Sponsor, Business/Function and CFCR RFOs.	Exported fields match workflow data.
PM-WFE-011	Verify Corporate Action long-text Workflow Export	Export an assessment containing long Transaction and Rationale.	Complete applicable long-text values are exported without unintended truncation.

⸻

SHEET 4 — NICRA

A. Initiative

ID	Test Scenario	Test Steps	Expected Result
PM-INIT-012	Verify NICRA Initiative fields and behaviour	Select NICRA and review New Initiative Name, New Initiative Summary, First Line, Senior Manager / Group Business Head, Country Coverage, Business/Function and CFCR RFOs.	All configured NICRA fields are displayed and behave according to the BRD.
PM-INIT-013	Verify NICRA mandatory validation	Leave required NICRA fields blank and attempt to proceed.	Mandatory validation prevents progression until required fields are completed.
PM-INIT-014	Verify NICRA PSID population	Review First Line and Senior Manager / Group Business Head.	First Line and Senior Manager / Group Business Head follow configured PSID population logic.
PM-INIT-015	Verify NICRA Country Coverage	Select multiple countries up to and beyond the permitted limit.	Multiple countries can be selected up to a maximum of five; selection beyond the configured limit is prevented.
PM-INIT-016	Verify NICRA Business/Function and CFCR RFOs	Select multiple Business/Function values and review CFCR RFOs.	Multiple Business/Function values can be selected and CFCR RFOs are populated according to CRHS logic.
PM-INIT-021	Verify Initiative submission	Complete all mandatory fields and submit.	Assessment is created successfully and progresses to Risk Assessment.

B. Landing Page

ID	Test Scenario	Test Steps	Expected Result
PM-NICRA-LP-001	Verify NICRA category fields	Select NICRA and review the grid.	New Initiative Name, New Initiative Summary, First Line, Senior Manager / Group Business Head, Country Coverage, Business/Function and CFCR RFOs display correct values.
PM-NICRA-LP-002	Verify NICRA common fields	Review Status, Created By, Created Date, Last Updated Date and Completed Date.	Common fields display correct values.
PM-NICRA-LP-003	Verify multiple Country Coverage, Business/Function and CFCR RFOs	Open a NICRA case containing multiple selections.	All selected Country Coverage, Business/Function and CFCR RFOs values are displayed correctly.
PM-NICRA-LP-004	Verify Country Coverage limit	Review/create a NICRA case containing the maximum permitted country selections.	Up to five countries can be selected and displayed.
PM-NICRA-LP-005	Verify New Initiative Summary full text	Select Click to View for New Initiative Summary.	Popup opens and displays complete New Initiative Summary without unintended truncation.
PM-NICRA-LP-006	Verify NICRA field data accuracy	Compare New Initiative Name, New Initiative Summary, First Line, Senior Manager / Group Business Head, Country Coverage, Business/Function and CFCR RFOs with submitted data.	All NICRA field values match submitted assessment data.

C. Details

ID	Test Scenario	Test Steps	Expected Result
PM-WF-008	Verify NICRA Details	Review New Initiative Name, New Initiative Summary, First Line, Senior Manager / Group Business Head, Country Coverage, Business/Function and CFCR RFOs.	All applicable NICRA Details match submitted assessment.
PM-WF-011	Verify New Initiative Summary Click to View in Details	Select Click to View for New Initiative Summary.	Popup opens and displays complete underlying text.

D. Exports

ID	Test Scenario	Test Steps	Expected Result
PM-LPE-006	Verify NICRA exported fields	Export NICRA and review New Initiative Name, New Initiative Summary, First Line, Senior Manager / Group Business Head, Country Coverage, Business/Function and CFCR RFOs.	Exported fields match Landing Page data.
PM-LPE-009	Verify NICRA long-text export	Export a case containing long New Initiative Summary.	Complete New Initiative Summary is exported without unintended truncation.
PM-WFE-006	Verify NICRA Workflow Export fields	Review New Initiative Name, New Initiative Summary, First Line, Senior Manager / Group Business Head, Country Coverage, Business/Function and CFCR RFOs.	Exported fields match workflow data.
PM-WFE-011	Verify NICRA long-text Workflow Export	Export an assessment containing long New Initiative Summary.	Complete New Initiative Summary is exported without unintended truncation.

⸻

SHEET 5 — OTHER

A. Initiative

ID	Test Scenario	Test Steps	Expected Result
PM-INIT-017	Verify Other Initiative fields and behaviour	Select Other and review New Initiative Name, New Initiative Summary, First Line, Approver, Country Coverage, Business/Function and CFCR RFOs.	All configured Other fields are displayed and behave according to the BRD.
PM-INIT-018	Verify Other mandatory validation	Leave required Other fields blank and attempt to proceed.	Mandatory validation prevents progression until required fields are completed.
PM-INIT-019	Verify Other PSID population	Review First Line and Approver.	First Line and Approver follow configured PSID population logic.
PM-INIT-020	Verify Other Country Coverage, Business/Function and CFCR RFOs	Select multiple Country Coverage and Business/Function values and review CFCR RFOs.	Multiple permitted selections are retained and CFCR RFOs are populated according to CRHS logic.
PM-INIT-021	Verify Initiative submission	Complete all mandatory fields and submit.	Assessment is created successfully and progresses to Risk Assessment.

B. Landing Page

ID	Test Scenario	Test Steps	Expected Result
PM-OTH-LP-001	Verify Other category fields	Select Other and review the grid.	New Initiative Name, New Initiative Summary, First Line, Approver, Country Coverage, Business/Function and CFCR RFOs display correct values.
PM-OTH-LP-002	Verify Other common fields	Review Status, Created By, Created Date, Last Updated Date and Completed Date.	Common fields display correct values.
PM-OTH-LP-003	Verify multiple Country Coverage, Business/Function and CFCR RFOs	Open an Other case containing multiple selections.	All selected Country Coverage, Business/Function and CFCR RFOs values are displayed correctly.
PM-OTH-LP-004	Verify Country Coverage limit	Review/create an Other case with multiple countries.	Country Coverage supports the configured maximum and displays selected countries correctly.
PM-OTH-LP-005	Verify New Initiative Summary full text	Select Click to View for New Initiative Summary.	Popup opens and displays complete New Initiative Summary without unintended truncation.
PM-OTH-LP-006	Verify Other field data accuracy	Compare New Initiative Name, New Initiative Summary, First Line, Approver, Country Coverage, Business/Function and CFCR RFOs with submitted data.	All Other category field values match submitted assessment data.

C. Details

ID	Test Scenario	Test Steps	Expected Result
PM-WF-009	Verify Other Details	Review New Initiative Name, New Initiative Summary, First Line, Approver, Country Coverage, Business/Function and CFCR RFOs.	All applicable Other Details match submitted assessment.
PM-WF-011	Verify New Initiative Summary Click to View in Details	Select Click to View for New Initiative Summary.	Popup opens and displays complete underlying text.

D. Exports

ID	Test Scenario	Test Steps	Expected Result
PM-LPE-007	Verify Other exported fields	Export Other and review New Initiative Name, New Initiative Summary, First Line, Approver, Country Coverage, Business/Function and CFCR RFOs.	Exported fields match Landing Page data.
PM-LPE-009	Verify Other long-text export	Export a case containing long New Initiative Summary.	Complete New Initiative Summary is exported without unintended truncation.
PM-WFE-007	Verify Other Workflow Export fields	Review New Initiative Name, New Initiative Summary, First Line, Approver, Country Coverage, Business/Function and CFCR RFOs.	Exported fields match workflow data.
PM-WFE-011	Verify Other long-text Workflow Export	Export an assessment containing long New Initiative Summary.	Complete New Initiative Summary is exported without unintended truncation.

⸻

One correction to the earlier structure

I wouldn’t put PM-WF-006/007/008/009 etc. into a generic Workflow sheet anymore. Those are category-specific, so they belong in their respective category sheets.

The same applies to:

* category-specific Landing Page cases
* category-specific Landing Page Export cases
* category-specific Details cases
* category-specific Workflow Export cases

The common sheet only contains functionality that genuinely applies across all four categories.

That gives you a much cleaner UAT workbook:

Common Functionality → New Product → Corporate Action → NICRA → Other

And when your senior asks, “Show me the NICRA UAT cases,” you can literally open one sheet and everything specific to NICRA is there.

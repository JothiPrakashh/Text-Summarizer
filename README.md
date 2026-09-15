Yes. Now we have the actual BRD field names from the screenshots, so we can do this properly from scratch.

I’m treating the COI categories as:

1. New Product / Product Change
2. Corporate Action
3. NICRA – New Initiatives / Change Risk Assessment
4. Other

And the UAT granularity is locked:

ONE test case = ONE validation = ONE row.
No “validate all fields” or “select each category” summary cases.

For every applicable category, I’m also including the common landing-page fields:

Status, Created By, Created Date, Last Updated Date, Completed Date

For long-text fields such as Transaction and Rationale, I’m separately testing:

* the Click to View hyperlink
* the popup
* the complete underlying text

Below is the full manual version you can put directly into Excel.

⸻

COI — PM / MAKER TEST CASES

1. PM — LANDING PAGE — COMMON FUNCTIONALITY

ID	Test Scenario	Test Steps	Expected Result
PM-LP-001	Verify COI landing page access	Login as PM and navigate to COI.	COI landing page is displayed.
PM-LP-002	Verify My Cases view	Select My Cases.	PM’s applicable COI cases are displayed.
PM-LP-003	Verify All Cases view	Select All Cases.	All COI cases accessible to PM are displayed.
PM-LP-004	Switch My Cases to All Cases	Select My Cases, then select All Cases.	Grid refreshes to display All Cases.
PM-LP-005	Switch All Cases to My Cases	Select All Cases, then select My Cases.	Grid refreshes to display My Cases.
PM-LP-006	Verify Initiative Category dropdown	Open the Initiative Category dropdown.	All configured COI categories are displayed.
PM-LP-007	Verify New Product / Product Change category	Select New Product / Product Change.	Applicable New Product / Product Change records are displayed.
PM-LP-008	Verify Corporate Action category	Select Corporate Action.	Applicable Corporate Action records are displayed.
PM-LP-009	Verify NICRA category	Select NICRA.	Applicable NICRA records are displayed.
PM-LP-010	Verify Other category	Select Other.	Applicable Other records are displayed.
PM-LP-011	Verify category-specific grid refresh	Switch between COI categories.	Category-specific records and columns refresh correctly.
PM-LP-012	Verify In Progress tile	Select In Progress.	In-progress COI cases are displayed.
PM-LP-013	Verify Pending Endorsement tile	Select Pending Endorsement.	Pending Endorsement cases are displayed.
PM-LP-014	Verify Refer Back tile	Select Refer Back.	Referred-back cases are displayed.
PM-LP-015	Verify Endorsement by RFO tile	Select Endorsement by RFO.	Applicable RFO endorsement cases are displayed.
PM-LP-016	Verify Completed tile	Select Completed.	Completed COI cases are displayed.
PM-LP-017	Verify status count	Compare status tile count with corresponding records.	Status count matches the applicable records.
PM-LP-018	Verify search with valid value	Enter a valid searchable value.	Matching records are displayed.
PM-LP-019	Verify search with invalid value	Enter a non-existing value.	No matching records are displayed.
PM-LP-020	Verify filter	Apply a valid grid filter.	Only matching records are displayed.
PM-LP-021	Verify clear filter	Apply a filter and select Clear.	All applicable records are restored.
PM-LP-022	Verify ascending sort	Sort a sortable column in ascending order.	Records are sorted in ascending order.
PM-LP-023	Verify descending sort	Sort a sortable column in descending order.	Records are sorted in descending order.
PM-LP-024	Verify pagination	Navigate between grid pages.	Correct records are displayed on each page.
PM-LP-025	Verify horizontal scrolling	Scroll horizontally across the grid.	All configured columns are accessible.

⸻

2. PM — LANDING PAGE — NEW PRODUCT / PRODUCT CHANGE

BRD fields

The BRD screenshot gives us:

* Programme code*
* Programme Name*
* Product manager*
* Business head / Product head*
* Business line*
* CFCR RFO*
* Product description & scope*
* Applicable to:
    * Islamic variant?
    * Sustainable finance variant?

Individual UAT cases

ID	Test Scenario	Test Steps	Expected Result
PM-NP-LP-001	Verify Programme code	Open New Product / Product Change records and review Programme code.	Programme code is displayed correctly.
PM-NP-LP-002	Verify Programme code format	Review a valid Programme code.	Programme code follows the configured PPG-XXXXX format and character rules.
PM-NP-LP-003	Verify Programme Name	Review Programme Name.	Programme Name is displayed correctly.
PM-NP-LP-004	Verify Product manager	Review Product manager.	Product manager displays the correct user.
PM-NP-LP-005	Verify Business head / Product head	Review Business head / Product head.	Business head / Product head displays the correct user.
PM-NP-LP-006	Verify Business line	Review Business line.	Business line displays the correct value.
PM-NP-LP-007	Verify CFCR RFO	Review CFCR RFO.	CFCR RFO displays the applicable RFO.
PM-NP-LP-008	Verify Product description & scope	Review Product description & scope.	Product description & scope displays the correct value.
PM-NP-LP-009	Verify Product description & scope full text	Open the long-text value where Click to View is available.	Full Product description & scope is displayed.
PM-NP-LP-010	Verify Applicable to — Islamic variant	Review Applicable to: Islamic variant?.	Islamic variant selection is displayed correctly.
PM-NP-LP-011	Verify Applicable to — Sustainable finance variant	Review Applicable to: Sustainable finance variant?.	Sustainable finance variant selection is displayed correctly.
PM-NP-LP-012	Verify Status	Review Status.	Status displays the current case status.
PM-NP-LP-013	Verify Created By	Review Created By.	Created By displays the correct creator.
PM-NP-LP-014	Verify Created Date	Review Created Date.	Created Date displays the correct creation date.
PM-NP-LP-015	Verify Last Updated Date	Review Last Updated Date.	Last Updated Date displays the latest update date.
PM-NP-LP-016	Verify Completed Date	Review Completed Date for a completed case.	Completed Date displays the correct completion date.
PM-NP-LP-017	Verify Completed Date for incomplete case	Review an incomplete case.	Completed Date is blank/not applicable.

⸻

3. PM — LANDING PAGE — CORPORATE ACTION

BRD fields

Exact fields from your screenshot:

* Project Name*
* Transaction*
* Rationale*
* Responsible Person*
* Accountable Executive*
* MT Sponsor*
* Business/Function*
* CFCR RFOs*

Plus common fields.

ID	Test Scenario	Test Steps	Expected Result
PM-CA-LP-001	Verify Project Name	Review Project Name.	Project Name displays the correct value.
PM-CA-LP-002	Verify Transaction	Review Transaction.	Transaction displays Click to View.
PM-CA-LP-003	Verify Rationale	Review Rationale.	Rationale displays Click to View.
PM-CA-LP-004	Verify Responsible Person	Review Responsible Person.	Responsible Person displays the correct user.
PM-CA-LP-005	Verify Accountable Executive	Review Accountable Executive.	Accountable Executive displays the correct user.
PM-CA-LP-006	Verify MT Sponsor	Review MT Sponsor.	MT Sponsor displays the correct user.
PM-CA-LP-007	Verify Business/Function	Review Business/Function.	Business/Function displays the correct value(s).
PM-CA-LP-008	Verify multiple Business/Function values	Open a case with multiple Business/Function selections.	All selected Business/Function values are displayed.
PM-CA-LP-009	Verify CFCR RFOs	Review CFCR RFOs.	Applicable CFCR RFOs are displayed.
PM-CA-LP-010	Verify multiple CFCR RFOs	Open a case with multiple RFOs.	All selected CFCR RFOs are displayed.
PM-CA-LP-011	Verify Status	Review Status.	Status displays the current case status.
PM-CA-LP-012	Verify Created By	Review Created By.	Created By displays the correct creator.
PM-CA-LP-013	Verify Created Date	Review Created Date.	Created Date displays the correct date.
PM-CA-LP-014	Verify Last Updated Date	Review Last Updated Date.	Last Updated Date displays the latest update date.
PM-CA-LP-015	Verify Completed Date	Review Completed Date.	Completed Date displays the completion date for completed cases.
PM-CA-LP-016	Verify Transaction hyperlink	Click Transaction / Click to View.	Transaction popup opens.
PM-CA-LP-017	Verify Transaction popup content	Review the popup.	Complete Transaction text is displayed.
PM-CA-LP-018	Verify Transaction text accuracy	Compare popup value with source/workflow value.	Complete Transaction text matches the stored value.
PM-CA-LP-019	Verify Rationale hyperlink	Click Rationale / Click to View.	Rationale popup opens.
PM-CA-LP-020	Verify Rationale popup content	Review the popup.	Complete Rationale text is displayed.
PM-CA-LP-021	Verify Rationale text accuracy	Compare popup value with source/workflow value.	Complete Rationale text matches the stored value.

⸻

4. PM — LANDING PAGE — NICRA

Exact BRD fields from your screenshot

* New Initiative Name*
* New Initiative Summary*
* First Line*
* Senior Manager / Group Business Head*
* Country Coverage*
* Business/Function*
* CFCR RFOs*

Important BRD behaviour:

* First Line → logged-in User PSID / same IFC logic
* Senior Manager / Group Business Head → PSID
* Country Coverage → maximum 5 countries; multiple countries can be selected
* Business/Function → multiple can be selected
* CFCR RFOs → pre-populated from CRHS; multiple RFOs can be selected

ID	Test Scenario	Test Steps	Expected Result
PM-NICRA-LP-001	Verify New Initiative Name	Select NICRA and review New Initiative Name.	New Initiative Name displays the correct value.
PM-NICRA-LP-002	Verify New Initiative Summary	Review New Initiative Summary.	New Initiative Summary displays the correct value.
PM-NICRA-LP-003	Verify First Line	Review First Line.	First Line displays the correct user/value.
PM-NICRA-LP-004	Verify Senior Manager / Group Business Head	Review Senior Manager / Group Business Head.	Correct user is displayed.
PM-NICRA-LP-005	Verify Country Coverage	Review Country Coverage.	Selected country/group coverage is displayed correctly.
PM-NICRA-LP-006	Verify multiple Country Coverage values	Open a case with multiple countries.	All selected Country Coverage values are displayed.
PM-NICRA-LP-007	Verify maximum Country Coverage	Create/select a case with five countries.	Maximum of five countries can be selected.
PM-NICRA-LP-008	Verify Business/Function	Review Business/Function.	Selected Business/Function values are displayed correctly.
PM-NICRA-LP-009	Verify multiple Business/Function values	Open a case with multiple selections.	All selected Business/Function values are displayed.
PM-NICRA-LP-010	Verify CFCR RFOs	Review CFCR RFOs.	Applicable CFCR RFOs are displayed.
PM-NICRA-LP-011	Verify multiple CFCR RFOs	Open a case with multiple RFOs.	All selected CFCR RFOs are displayed.
PM-NICRA-LP-012	Verify Status	Review Status.	Status displays the current case status.
PM-NICRA-LP-013	Verify Created By	Review Created By.	Created By displays the correct creator.
PM-NICRA-LP-014	Verify Created Date	Review Created Date.	Created Date displays the correct date.
PM-NICRA-LP-015	Verify Last Updated Date	Review Last Updated Date.	Last Updated Date displays the latest update date.
PM-NICRA-LP-016	Verify Completed Date	Review Completed Date.	Completed Date displays the completion date where applicable.
PM-NICRA-LP-017	Verify New Initiative Summary full text	Open the long-text value using Click to View where available.	Full New Initiative Summary is displayed.

⸻

5. PM — LANDING PAGE — OTHER

Exact BRD fields from your screenshot

* New Initiative Name*
* New Initiative Summary*
* First Line*
* Approver*
* Country Coverage*
* Business/Function*
* CFCR RFOs*

ID	Test Scenario	Test Steps	Expected Result
PM-OTH-LP-001	Verify New Initiative Name	Select Other and review New Initiative Name.	New Initiative Name displays the correct value.
PM-OTH-LP-002	Verify New Initiative Summary	Review New Initiative Summary.	New Initiative Summary displays the correct value.
PM-OTH-LP-003	Verify First Line	Review First Line.	First Line displays the correct user/value.
PM-OTH-LP-004	Verify Approver	Review Approver.	Approver displays the correct user.
PM-OTH-LP-005	Verify Country Coverage	Review Country Coverage.	Selected Country Coverage is displayed correctly.
PM-OTH-LP-006	Verify multiple Country Coverage values	Open a case with multiple countries.	All selected Country Coverage values are displayed.
PM-OTH-LP-007	Verify Business/Function	Review Business/Function.	Selected Business/Function values are displayed.
PM-OTH-LP-008	Verify multiple Business/Function values	Open a case with multiple selections.	All selected Business/Function values are displayed.
PM-OTH-LP-009	Verify CFCR RFOs	Review CFCR RFOs.	Applicable CFCR RFOs are displayed.
PM-OTH-LP-010	Verify multiple CFCR RFOs	Open a case with multiple RFOs.	All selected CFCR RFOs are displayed.
PM-OTH-LP-011	Verify Status	Review Status.	Status displays the current case status.
PM-OTH-LP-012	Verify Created By	Review Created By.	Created By displays the correct creator.
PM-OTH-LP-013	Verify Created Date	Review Created Date.	Created Date displays the correct date.
PM-OTH-LP-014	Verify Last Updated Date	Review Last Updated Date.	Last Updated Date displays the latest update date.
PM-OTH-LP-015	Verify Completed Date	Review Completed Date.	Completed Date displays the completion date where applicable.
PM-OTH-LP-016	Verify New Initiative Summary full text	Open the long-text value.	Full New Initiative Summary is displayed.

⸻

6. PM — LANDING PAGE EXPORT

The export needs to be tested for every category, not just “verify export”.

ID	Test Scenario	Test Steps	Expected Result
PM-LPE-001	Verify Export option	Open COI landing page.	Export option is available.
PM-LPE-002	Verify New Product / Product Change export	Select New Product / Product Change and export.	New Product / Product Change data is exported.
PM-LPE-003	Verify Corporate Action export	Select Corporate Action and export.	Corporate Action data is exported.
PM-LPE-004	Verify NICRA export	Select NICRA and export.	NICRA data is exported.
PM-LPE-005	Verify Other export	Select Other and export.	Other data is exported.
PM-LPE-006	Verify export download	Select Export.	Export file downloads successfully.
PM-LPE-007	Verify export file	Open downloaded file.	Export file opens successfully.
PM-LPE-008	Verify New Product / Product Change exported Programme code	Export New Product / Product Change and review Programme code.	Programme code matches landing page.
PM-LPE-009	Verify exported Programme Name	Review Programme Name.	Programme Name matches landing page.
PM-LPE-010	Verify exported Product manager	Review Product manager.	Product manager matches landing page.
PM-LPE-011	Verify exported Business head / Product head	Review Business head / Product head.	Value matches landing page.
PM-LPE-012	Verify exported Business line	Review Business line.	Value matches landing page.
PM-LPE-013	Verify exported CFCR RFO	Review CFCR RFO.	Value matches landing page.
PM-LPE-014	Verify exported Product description & scope	Review Product description & scope.	Value matches landing page.
PM-LPE-015	Verify exported Applicable to	Review Applicable to values.	Islamic/Sustainable finance selections match landing page.
PM-LPE-016	Verify exported Corporate Action fields	Export Corporate Action and review all CA fields.	Project Name, Transaction, Rationale, Responsible Person, Accountable Executive, MT Sponsor, Business/Function and CFCR RFOs match landing page.
PM-LPE-017	Verify exported NICRA fields	Export NICRA and review all NICRA fields.	New Initiative Name, New Initiative Summary, First Line, Senior Manager / Group Business Head, Country Coverage, Business/Function and CFCR RFOs match landing page.
PM-LPE-018	Verify exported Other fields	Export Other and review all Other fields.	New Initiative Name, New Initiative Summary, First Line, Approver, Country Coverage, Business/Function and CFCR RFOs match landing page.
PM-LPE-019	Verify exported Status	Review Status in export.	Status matches landing page.
PM-LPE-020	Verify exported Created By	Review Created By.	Created By matches landing page.
PM-LPE-021	Verify exported Created Date	Review Created Date.	Created Date matches landing page.
PM-LPE-022	Verify exported Last Updated Date	Review Last Updated Date.	Last Updated Date matches landing page.
PM-LPE-023	Verify exported Completed Date	Review Completed Date.	Completed Date matches landing page.
PM-LPE-024	Verify Transaction export	Export Corporate Action containing long Transaction.	Complete Transaction is exported.
PM-LPE-025	Verify Rationale export	Export Corporate Action containing long Rationale.	Complete Rationale is exported.
PM-LPE-026	Verify My Cases export	Select My Cases and export.	Export contains My Cases records.
PM-LPE-027	Verify All Cases export	Select All Cases and export.	Export contains All Cases records.
PM-LPE-028	Verify filtered export	Apply a filter and export.	Export reflects the applied filter.
PM-LPE-029	Verify searched export	Apply search and export.	Export reflects the search results.
PM-LPE-030	Verify exported data accuracy	Compare exported data against landing page.	Exported data matches landing-page data.

⸻

7. PM — WORKFLOW / DETAILS PANEL

ID	Test Scenario	Test Steps	Expected Result
PM-WF-001	Open assessment from landing page	Select a COI case.	Selected assessment opens successfully.
PM-WF-002	Verify workflow stages	Review workflow progress indicator.	Configured COI workflow stages are displayed.
PM-WF-003	Verify current stage	Open an in-progress assessment.	Current stage is highlighted.
PM-WF-004	Verify current status	Review assessment status.	Current Status is displayed correctly.
PM-WF-005	Verify Details panel	Open Details.	Details panel is displayed.
PM-WF-006	Verify Info tab	Select Info.	Assessment information is displayed.
PM-WF-007	Verify History tab	Select History.	Assessment history is displayed.
PM-WF-008	Verify Case ID	Review Case ID in Details.	Case ID matches the assessment.
PM-WF-009	Verify Initiative Category	Review Initiative Category.	Initiative Category matches the selected category.
PM-WF-010	Verify Responsible Person	Review Responsible Person.	Correct Responsible Person is displayed.
PM-WF-011	Verify category-specific details	Open each category assessment.	Category-specific fields match submitted values.
PM-WF-012	Verify Transaction	Review Transaction.	Transaction is available through Click to View.
PM-WF-013	Verify Transaction popup	Click Transaction / Click to View.	Full Transaction description opens in popup.
PM-WF-014	Verify Rationale	Review Rationale.	Rationale is available through Click to View.
PM-WF-015	Verify Rationale popup	Click Rationale / Click to View.	Full Rationale description opens in popup.
PM-WF-016	Verify Accountable Executive	Review Accountable Executive.	Correct Accountable Executive is displayed.
PM-WF-017	Verify MT Sponsor	Review MT Sponsor.	Correct MT Sponsor is displayed.
PM-WF-018	Verify Business/Function	Review Business/Function.	Correct selected Business/Function values are displayed.
PM-WF-019	Verify CFCR RFOs	Review CFCR RFOs.	Correct assigned CFCR RFOs are displayed.
PM-WF-020	Verify Created By	Review Created By.	Correct creator is displayed.
PM-WF-021	Verify Created Date	Review Created Date.	Correct creation date is displayed.
PM-WF-022	Verify Last Updated Date	Review Last Updated Date.	Latest update date is displayed.
PM-WF-023	Verify Completed Date	Review completed assessment.	Correct Completed Date is displayed.

⸻

8. PM — INITIATIVE STAGE

This is PM-only because RFO does not initiate the assessment.

ID	Test Scenario	Test Steps	Expected Result
PM-INIT-001	Verify Initiative stage	Open a new COI assessment.	Initiate Risk Assessment stage is displayed.
PM-INIT-002	Verify Initiative Category	Review the category selected for the assessment.	Correct Initiative Category is displayed.
PM-INIT-003	Verify category-specific fields	Select each category and review the Initiative stage.	Applicable category-specific fields are displayed.
PM-INIT-004	Verify Programme code	Enter valid Programme code for New Product / Product Change.	Programme code accepts valid value.
PM-INIT-005	Verify Programme code format	Enter invalid Programme code format.	Invalid Programme code is rejected.
PM-INIT-006	Verify Programme Name	Enter Programme Name.	Programme Name is accepted.
PM-INIT-007	Verify Product manager population	Open the assessment as PM.	Product manager is populated with logged-in user’s PSID where applicable.
PM-INIT-008	Verify Business head / Product head population	Select Business head / Product head.	Value is populated through PSID selection.
PM-INIT-009	Verify Business line selection	Select Business line.	Valid Business line can be selected.
PM-INIT-010	Verify CFCR RFO population	Enter/select applicable risk information.	CFCR RFO is pre-populated according to CRHS logic.
PM-INIT-011	Verify Product description & scope	Enter valid description.	Product description & scope is accepted.
PM-INIT-012	Verify Product description & scope mandatory	Leave field blank and proceed.	User cannot proceed without Product description & scope.
PM-INIT-013	Verify Applicable to — Islamic variant	Select Islamic variant.	Islamic variant selection is saved.
PM-INIT-014	Verify Applicable to — Sustainable finance variant	Select Sustainable finance variant.	Sustainable finance variant selection is saved.
PM-INIT-015	Verify blank Applicable to	Leave both Applicable to boxes unselected where permitted.	Assessment can proceed where applicable.
PM-INIT-016	Verify Corporate Action Project Name	Enter Project Name.	Project Name is accepted.
PM-INIT-017	Verify Corporate Action Transaction	Enter Transaction.	Transaction is accepted.
PM-INIT-018	Verify Corporate Action Rationale	Enter Rationale.	Rationale is accepted.
PM-INIT-019	Verify Responsible Person	Review Responsible Person.	Responsible Person is populated through PSID.
PM-INIT-020	Verify Accountable Executive	Select Accountable Executive using PSID.	Correct user is populated.
PM-INIT-021	Verify MT Sponsor	Select MT Sponsor using PSID.	Correct user is populated.
PM-INIT-022	Verify Corporate Action Business/Function	Select one or more Business/Function values.	Multiple Business/Function values can be selected.
PM-INIT-023	Verify Corporate Action CFCR RFOs	Review CFCR RFOs.	Applicable RFOs are pre-populated from CRHS.
PM-INIT-024	Verify NICRA New Initiative Name	Enter New Initiative Name.	New Initiative Name is accepted.
PM-INIT-025	Verify NICRA New Initiative Summary	Enter New Initiative Summary.	New Initiative Summary is accepted.
PM-INIT-026	Verify NICRA First Line	Review First Line.	First Line is populated according to configured logic.
PM-INIT-027	Verify NICRA Senior Manager / Group Business Head	Select using PSID.	Correct Senior Manager / Group Business Head is populated.
PM-INIT-028	Verify NICRA Country Coverage	Select countries.	Multiple countries can be selected up to configured maximum of five.
PM-INIT-029	Verify NICRA Business/Function	Select Business/Function values.	Multiple Business/Function values can be selected.
PM-INIT-030	Verify NICRA CFCR RFOs	Review RFO values.	CFCR RFOs are pre-populated from CRHS.
PM-INIT-031	Verify Other New Initiative Name	Enter New Initiative Name.	New Initiative Name is accepted.
PM-INIT-032	Verify Other New Initiative Summary	Enter New Initiative Summary.	New Initiative Summary is accepted.
PM-INIT-033	Verify Other First Line	Review First Line.	First Line follows configured logic.
PM-INIT-034	Verify Other Approver	Select Approver using PSID.	Correct Approver is populated.
PM-INIT-035	Verify Other Country Coverage	Select countries.	Multiple Country Coverage values can be selected within configured limit.
PM-INIT-036	Verify Other Business/Function	Select Business/Function.	Multiple Business/Function values can be selected.
PM-INIT-037	Verify Other CFCR RFOs	Review CFCR RFOs.	RFOs are pre-populated from CRHS.
PM-INIT-038	Verify mandatory-field validation	Leave a mandatory field blank and attempt to proceed.	User cannot proceed and mandatory field validation is displayed.
PM-INIT-039	Verify successful Initiative submission	Complete all mandatory Initiative fields and submit.	Assessment is created successfully and proceeds to Risk Assessment.

⸻

9. PM — RISK ASSESSMENT

ID	Test Scenario	Test Steps	Expected Result
PM-RA-001	Verify Risk Assessment stage	Open a submitted COI assessment.	Risk Assessment stage is displayed.
PM-RA-002	Verify Initiative information carry-forward	Review information from Initiative stage.	Applicable Initiative information is retained.
PM-RA-003	Verify Potential COI Risk question	Review the question.	Potential COI Risk is displayed.
PM-RA-004	Select Potential COI Risk = No	Select No.	Assessment proceeds without requiring COI risk details.
PM-RA-005	Select Potential COI Risk = Yes	Select Yes.	Applicable COI risk details become required.
PM-RA-006	Verify Potential COI Risk mandatory logic	Select Yes and attempt to proceed without required details.	User cannot proceed until required COI risk information is provided.
PM-RA-007	Verify Risk Assessment response persistence	Enter responses and navigate away/back.	Entered responses are retained.
PM-RA-008	Verify Risk Assessment submission	Complete required Risk Assessment information.	Assessment can proceed to Mitigation Plan.

⸻

10. PM — MITIGATION PLAN

ID	Test Scenario	Test Steps	Expected Result
PM-MP-001	Verify Mitigation Plan stage	Navigate to Mitigation Plan.	Mitigation Plan stage is displayed.
PM-MP-002	Verify mitigation target	Enter mitigation target information.	Target information is retained.
PM-MP-003	Verify Action Owner	Select Action Owner.	Valid Action Owner can be selected.
PM-MP-004	Verify Action Owner PM	Select PM as Action Owner where applicable.	PM is displayed as Action Owner.
PM-MP-005	Verify Action Owner RFO	Select RFO as Action Owner where applicable.	RFO is displayed as Action Owner.
PM-MP-006	Verify Mitigation Plan status	Select configured mitigation Status.	Selected status is saved correctly.
PM-MP-007	Verify supporting document	Upload supporting document.	Supporting document uploads successfully.
PM-MP-008	Verify supporting document optional	Leave supporting document blank where optional.	User can proceed without the supporting document.
PM-MP-009	Verify mitigation plan mapping	Map a mitigation plan to a question.	Mitigation plan is mapped correctly.
PM-MP-010	Verify multiple-question mapping	Map one mitigation plan to multiple permitted questions.	One mitigation plan can be mapped to multiple applicable questions.
PM-MP-011	Verify Mitigation Plan data persistence	Save and revisit the stage.	Saved mitigation information is retained.
PM-MP-012	Verify Mitigation Plan submission	Complete required information and proceed.	Assessment progresses to Pending Endorsement.

⸻

11. PM — PENDING ENDORSEMENT

ID	Test Scenario	Test Steps	Expected Result
PM-PE-001	Verify Pending Endorsement stage	Submit completed assessment for endorsement.	Assessment moves to Pending Endorsement.
PM-PE-002	Verify assigned CFCR RFOs	Review assigned RFOs.	Applicable CFCR RFOs are displayed.
PM-PE-003	Verify RFO coverage status	Review RFO/Coverage status - 1LOD.	RFO coverage information is displayed.
PM-PE-004	Verify RFO endorsement status	Review endorsement status.	Current RFO endorsement status is displayed.
PM-PE-005	Verify RFO coverage comments	Review RFO coverage comments.	RFO coverage comments are displayed where provided.
PM-PE-006	Verify optional RFO coverage comments	Complete endorsement without optional coverage comments.	Assessment can proceed without optional comments.
PM-PE-007	Verify endorsed status	RFO completes endorsement.	Corresponding RFO endorsement status is updated.
PM-PE-008	Verify multiple RFO endorsements	Assign multiple RFOs and complete required endorsements.	Each RFO endorsement status is tracked separately.
PM-PE-009	Verify completion after all endorsements	Complete all required RFO endorsements.	Assessment becomes eligible for final completion.
PM-PE-010	Verify Refer Back	RFO refers assessment back.	Assessment moves to Refer Back.
PM-PE-011	Verify Refer Back comments	Open referred-back assessment.	RFO’s Refer Back comments are displayed.
PM-PE-012	Verify PM update after Refer Back	Update the required information.	PM can update permitted fields.
PM-PE-013	Verify resubmission after Refer Back	Resubmit corrected assessment.	Assessment returns to RFO endorsement.

⸻

12. PM — OFFLINE ENDORSEMENT / FINAL SUBMISSION

ID	Test Scenario	Test Steps	Expected Result
PM-FIN-001	Verify Offline Endorsement option	Open applicable assessment.	Offline Endorsement option is available where applicable.
PM-FIN-002	Verify offline endorsement evidence upload	Upload endorsement evidence.	Evidence uploads successfully.
PM-FIN-003	Verify offline endorsement evidence association	Open the assessment after upload.	Evidence is associated with the correct assessment.
PM-FIN-004	Verify final endorsed risk assessment	Complete required endorsements.	Assessment reaches Final endorsed risk assessment stage.
PM-FIN-005	Verify final assessment information	Review final assessment.	Final assessment information is displayed correctly.
PM-FIN-006	Verify final submission	Complete required final action and submit.	Assessment is submitted successfully.
PM-FIN-007	Verify Completed status	Return to landing page.	Assessment appears under Completed.
PM-FIN-008	Verify Completed Date	Open completed assessment.	Completed Date is populated.
PM-FIN-009	Verify completion history	Open History.	Final submission and completion activity are recorded.

⸻

13. PM — WORKFLOW EXPORT

ID	Test Scenario	Test Steps	Expected Result
PM-WFE-001	Verify Workflow Export option	Open COI workflow.	Workflow Export option is available.
PM-WFE-002	Verify Workflow Export download	Select Export.	Workflow export downloads successfully.
PM-WFE-003	Verify Case ID in export	Review Case ID.	Exported Case ID matches workflow.
PM-WFE-004	Verify Initiative Category in export	Review Initiative Category.	Exported Initiative Category matches workflow.
PM-WFE-005	Verify category-specific fields	Review applicable category fields.	Exported category-specific fields match workflow.
PM-WFE-006	Verify Transaction in export	Review Transaction.	Complete Transaction is exported.
PM-WFE-007	Verify Rationale in export	Review Rationale.	Complete Rationale is exported.
PM-WFE-008	Verify Risk Assessment data	Review exported Risk Assessment information.	Risk Assessment data matches workflow.
PM-WFE-009	Verify Mitigation Plan data	Review exported Mitigation Plan information.	Mitigation Plan data matches workflow.
PM-WFE-010	Verify Action Owner	Review exported Action Owner.	Action Owner matches workflow.
PM-WFE-011	Verify mitigation Status	Review mitigation Status.	Status matches workflow.
PM-WFE-012	Verify supporting document information	Review applicable supporting document information.	Export reflects configured document information.
PM-WFE-013	Verify RFO/Coverage status - 1LOD	Review exported RFO coverage status.	Export matches workflow.
PM-WFE-014	Verify RFO comments	Review exported RFO comments.	Export matches workflow.
PM-WFE-015	Verify endorsement information	Review endorsement information.	Exported endorsement information matches workflow.
PM-WFE-016	Verify Status	Review Status.	Exported Status matches workflow.
PM-WFE-017	Verify Created By	Review Created By.	Exported Created By matches workflow.
PM-WFE-018	Verify Created Date	Review Created Date.	Exported Created Date matches workflow.
PM-WFE-019	Verify Last Updated Date	Review Last Updated Date.	Exported Last Updated Date matches workflow.
PM-WFE-020	Verify Completed Date	Review Completed Date.	Exported Completed Date matches workflow.
PM-WFE-021	Verify long Transaction export	Export assessment with long Transaction.	Complete Transaction is exported without unintended truncation.
PM-WFE-022	Verify long Rationale export	Export assessment with long Rationale.	Complete Rationale is exported without unintended truncation.
PM-WFE-023	Verify Workflow Export accuracy	Compare workflow with exported data.	Exported data matches workflow data.

⸻

COI — RFO / REVIEWER TEST CASES

RFO does not have the Initiative sheet/stage because RFO doesn’t initiate the assessment.

RFO covers:

Landing Page → Landing Page Export → Workflow → Risk Assessment Review → Mitigation Plan Review → Endorsement → Offline/Final → Workflow Export

⸻

14. RFO — LANDING PAGE COMMON

ID	Test Scenario	Test Steps	Expected Result
RFO-LP-001	Verify RFO landing page access	Login as RFO and navigate to COI.	COI landing page is displayed.
RFO-LP-002	Verify My Cases	Select My Cases.	RFO-accessible cases are displayed.
RFO-LP-003	Verify All Cases	Select All Cases, where permitted.	Only permitted cases are displayed.
RFO-LP-004	Verify category dropdown	Open Initiative Category.	All configured categories are displayed.
RFO-LP-005	Verify New Product / Product Change	Select category.	Applicable New Product / Product Change records are displayed.
RFO-LP-006	Verify Corporate Action	Select category.	Applicable Corporate Action records are displayed.
RFO-LP-007	Verify NICRA	Select category.	Applicable NICRA records are displayed.
RFO-LP-008	Verify Other	Select category.	Applicable Other records are displayed.
RFO-LP-009	Verify category switching	Switch between categories.	Grid refreshes correctly.
RFO-LP-010	Verify In Progress tile	Select In Progress.	Applicable in-progress cases are displayed.
RFO-LP-011	Verify Pending Endorsement tile	Select Pending Endorsement.	Applicable pending cases are displayed.
RFO-LP-012	Verify Refer Back tile	Select Refer Back.	Applicable referred-back cases are displayed.
RFO-LP-013	Verify Endorsement by RFO tile	Select Endorsement by RFO.	Applicable endorsement cases are displayed.
RFO-LP-014	Verify Completed tile	Select Completed.	Applicable completed cases are displayed.
RFO-LP-015	Verify status counts	Compare tile count with records.	Status count matches displayed records.
RFO-LP-016	Verify search	Enter valid searchable value.	Matching accessible records are displayed.
RFO-LP-017	Verify invalid search	Enter non-existing value.	No matching records are displayed.
RFO-LP-018	Verify filter	Apply a filter.	Matching records are displayed.
RFO-LP-019	Verify clear filter	Clear filter.	Applicable records are restored.
RFO-LP-020	Verify ascending sort	Sort a column ascending.	Records are sorted ascending.
RFO-LP-021	Verify descending sort	Sort a column descending.	Records are sorted descending.
RFO-LP-022	Verify pagination	Navigate pages.	Correct records are displayed.
RFO-LP-023	Verify horizontal scroll	Scroll horizontally.	All configured columns are accessible.

⸻

15. RFO — LANDING PAGE — NEW PRODUCT / PRODUCT CHANGE

ID	Test Scenario	Test Steps	Expected Result
RFO-NP-LP-001	Verify Programme code	Review Programme code.	Programme code displays the correct value.
RFO-NP-LP-002	Verify Programme Name	Review Programme Name.	Programme Name displays the correct value.
RFO-NP-LP-003	Verify Product manager	Review Product manager.	Product manager displays the correct user.
RFO-NP-LP-004	Verify Business head / Product head	Review Business head / Product head.	Correct user is displayed.
RFO-NP-LP-005	Verify Business line	Review Business line.	Correct Business line is displayed.
RFO-NP-LP-006	Verify CFCR RFO	Review CFCR RFO.	Correct CFCR RFO is displayed.
RFO-NP-LP-007	Verify Product description & scope	Review field.	Correct Product description & scope is displayed.
RFO-NP-LP-008	Verify Applicable to — Islamic variant	Review field.	Islamic variant selection is displayed correctly.
RFO-NP-LP-009	Verify Applicable to — Sustainable finance variant	Review field.	Sustainable finance variant selection is displayed correctly.
RFO-NP-LP-010	Verify Status	Review Status.	Current Status is displayed.
RFO-NP-LP-011	Verify Created By	Review Created By.	Correct creator is displayed.
RFO-NP-LP-012	Verify Created Date	Review Created Date.	Correct creation date is displayed.
RFO-NP-LP-013	Verify Last Updated Date	Review Last Updated Date.	Latest update date is displayed.
RFO-NP-LP-014	Verify Completed Date	Review Completed Date.	Completion date is displayed for completed cases.
RFO-NP-LP-015	Verify Product description & scope full text	Open Click to View where applicable.	Full Product description & scope is displayed.

⸻

16. RFO — LANDING PAGE — CORPORATE ACTION

ID	Test Scenario	Test Steps	Expected Result
RFO-CA-LP-001	Verify Project Name	Review Project Name.	Correct Project Name is displayed.
RFO-CA-LP-002	Verify Transaction	Review Transaction.	Transaction displays Click to View.
RFO-CA-LP-003	Verify Rationale	Review Rationale.	Rationale displays Click to View.
RFO-CA-LP-004	Verify Responsible Person	Review Responsible Person.	Correct Responsible Person is displayed.
RFO-CA-LP-005	Verify Accountable Executive	Review Accountable Executive.	Correct Accountable Executive is displayed.
RFO-CA-LP-006	Verify MT Sponsor	Review MT Sponsor.	Correct MT Sponsor is displayed.
RFO-CA-LP-007	Verify Business/Function	Review Business/Function.	Correct selected values are displayed.
RFO-CA-LP-008	Verify multiple Business/Function	Review a multi-selection case.	All selected values are displayed.
RFO-CA-LP-009	Verify CFCR RFOs	Review CFCR RFOs.	Applicable RFOs are displayed.
RFO-CA-LP-010	Verify multiple CFCR RFOs	Review multiple-RFO case.	All assigned RFOs are displayed.
RFO-CA-LP-011	Verify Status	Review Status.	Current Status is displayed.
RFO-CA-LP-012	Verify Created By	Review Created By.	Correct creator is displayed.
RFO-CA-LP-013	Verify Created Date	Review Created Date.	Correct date is displayed.
RFO-CA-LP-014	Verify Last Updated Date	Review Last Updated Date.	Latest update date is displayed.
RFO-CA-LP-015	Verify Completed Date	Review Completed Date.	Completion date is displayed where applicable.
RFO-CA-LP-016	Verify Transaction popup	Click Transaction / Click to View.	Full Transaction description opens.
RFO-CA-LP-017	Verify Rationale popup	Click Rationale / Click to View.	Full Rationale description opens.
RFO-CA-LP-018	Verify Transaction accuracy	Compare popup against workflow.	Full Transaction text matches workflow.
RFO-CA-LP-019	Verify Rationale accuracy	Compare popup against workflow.	Full Rationale text matches workflow.

⸻

17. RFO — LANDING PAGE — NICRA

ID	Test Scenario	Test Steps	Expected Result
RFO-NICRA-LP-001	Verify New Initiative Name	Review New Initiative Name.	Correct value is displayed.
RFO-NICRA-LP-002	Verify New Initiative Summary	Review New Initiative Summary.	Correct value is displayed.
RFO-NICRA-LP-003	Verify First Line	Review First Line.	Correct value is displayed.
RFO-NICRA-LP-004	Verify Senior Manager / Group Business Head	Review field.	Correct user is displayed.
RFO-NICRA-LP-005	Verify Country Coverage	Review Country Coverage.	Correct selected coverage is displayed.
RFO-NICRA-LP-006	Verify multiple Country Coverage	Review multi-country case.	All selected countries are displayed.
RFO-NICRA-LP-007	Verify Business/Function	Review field.	Correct selected values are displayed.
RFO-NICRA-LP-008	Verify multiple Business/Function	Review multi-selection case.	All selected values are displayed.
RFO-NICRA-LP-009	Verify CFCR RFOs	Review field.	Correct applicable RFOs are displayed.
RFO-NICRA-LP-010	Verify multiple CFCR RFOs	Review multi-RFO case.	All assigned RFOs are displayed.
RFO-NICRA-LP-011	Verify Status	Review Status.	Current Status is displayed.
RFO-NICRA-LP-012	Verify Created By	Review Created By.	Correct creator is displayed.
RFO-NICRA-LP-013	Verify Created Date	Review Created Date.	Correct creation date is displayed.
RFO-NICRA-LP-014	Verify Last Updated Date	Review Last Updated Date.	Latest update date is displayed.
RFO-NICRA-LP-015	Verify Completed Date	Review Completed Date.	Completion date is displayed where applicable.
RFO-NICRA-LP-016	Verify New Initiative Summary full text	Open Click to View where applicable.	Full New Initiative Summary is displayed.

⸻

18. RFO — LANDING PAGE — OTHER

ID	Test Scenario	Test Steps	Expected Result
RFO-OTH-LP-001	Verify New Initiative Name	Review New Initiative Name.	Correct value is displayed.
RFO-OTH-LP-002	Verify New Initiative Summary	Review New Initiative Summary.	Correct value is displayed.
RFO-OTH-LP-003	Verify First Line	Review First Line.	Correct value is displayed.
RFO-OTH-LP-004	Verify Approver	Review Approver.	Correct Approver is displayed.
RFO-OTH-LP-005	Verify Country Coverage	Review Country Coverage.	Correct selected coverage is displayed.
RFO-OTH-LP-006	Verify multiple Country Coverage	Review multi-country case.	All selected countries are displayed.
RFO-OTH-LP-007	Verify Business/Function	Review Business/Function.	Correct selected values are displayed.
RFO-OTH-LP-008	Verify multiple Business/Function	Review multi-selection case.	All selected values are displayed.
RFO-OTH-LP-009	Verify CFCR RFOs	Review CFCR RFOs.	Applicable RFOs are displayed.
RFO-OTH-LP-010	Verify multiple CFCR RFOs	Review multi-RFO case.	All assigned RFOs are displayed.
RFO-OTH-LP-011	Verify Status	Review Status.	Current Status is displayed.
RFO-OTH-LP-012	Verify Created By	Review Created By.	Correct creator is displayed.
RFO-OTH-LP-013	Verify Created Date	Review Created Date.	Correct creation date is displayed.
RFO-OTH-LP-014	Verify Last Updated Date	Review Last Updated Date.	Latest update date is displayed.
RFO-OTH-LP-015	Verify Completed Date	Review Completed Date.	Completion date is displayed where applicable.
RFO-OTH-LP-016	Verify New Initiative Summary full text	Open Click to View where applicable.	Full New Initiative Summary is displayed.

⸻

19. RFO — LANDING PAGE EXPORT

ID	Test Scenario	Test Steps	Expected Result
RFO-LPE-001	Verify Export option	Open RFO landing page.	Export option is available according to RFO permissions.
RFO-LPE-002	Verify New Product / Product Change export	Select category and export.	New Product / Product Change data is exported.
RFO-LPE-003	Verify Corporate Action export	Select category and export.	Corporate Action data is exported.
RFO-LPE-004	Verify NICRA export	Select category and export.	NICRA data is exported.
RFO-LPE-005	Verify Other export	Select category and export.	Other data is exported.
RFO-LPE-006	Verify export download	Select Export.	File downloads successfully.
RFO-LPE-007	Verify exported Programme code	Review Programme code.	Exported Programme code matches landing page.
RFO-LPE-008	Verify exported Programme Name	Review Programme Name.	Exported Programme Name matches landing page.
RFO-LPE-009	Verify exported Product manager	Review Product manager.	Exported Product manager matches landing page.
RFO-LPE-010	Verify exported Business head / Product head	Review field.	Exported value matches landing page.
RFO-LPE-011	Verify exported Business line	Review Business line.	Exported value matches landing page.
RFO-LPE-012	Verify exported Product description & scope	Review field.	Exported value matches landing page.
RFO-LPE-013	Verify exported Corporate Action fields	Review all CA fields.	Project Name, Transaction, Rationale, Responsible Person, Accountable Executive, MT Sponsor, Business/Function and CFCR RFOs match landing page.
RFO-LPE-014	Verify exported NICRA fields	Review all NICRA fields.	New Initiative Name, New Initiative Summary, First Line, Senior Manager / Group Business Head, Country Coverage, Business/Function and CFCR RFOs match landing page.
RFO-LPE-015	Verify exported Other fields	Review all Other fields.	New Initiative Name, New Initiative Summary, First Line, Approver, Country Coverage, Business/Function and CFCR RFOs match landing page.
RFO-LPE-016	Verify exported Status	Review Status.	Exported Status matches landing page.
RFO-LPE-017	Verify exported Created By	Review Created By.	Exported Created By matches landing page.
RFO-LPE-018	Verify exported Created Date	Review Created Date.	Exported Created Date matches landing page.
RFO-LPE-019	Verify exported Last Updated Date	Review Last Updated Date.	Exported Last Updated Date matches landing page.
RFO-LPE-020	Verify exported Completed Date	Review Completed Date.	Exported Completed Date matches landing page.
RFO-LPE-021	Verify Transaction export	Export Corporate Action.	Complete Transaction is exported.
RFO-LPE-022	Verify Rationale export	Export Corporate Action.	Complete Rationale is exported.
RFO-LPE-023	Verify filtered export	Apply filter and export.	Export reflects the applied filter.
RFO-LPE-024	Verify searched export	Search and export.	Export reflects search results.
RFO-LPE-025	Verify RFO-accessible data	Export as RFO.	Export contains only RFO-accessible data.
RFO-LPE-026	Verify export accuracy	Compare export with landing page.	Exported data matches landing page.

⸻

20. RFO — WORKFLOW / DETAILS PANEL

ID	Test Scenario	Test Steps	Expected Result
RFO-WF-001	Open assigned assessment	Select an assigned COI case.	Assessment opens successfully.
RFO-WF-002	Verify workflow stages	Review workflow progress.	Configured COI workflow stages are displayed.
RFO-WF-003	Verify current stage	Open assessment.	Current stage is highlighted.
RFO-WF-004	Verify current status	Review status.	Current Status is displayed correctly.
RFO-WF-005	Verify Details panel	Open Details.	Details panel is displayed.
RFO-WF-006	Verify Info tab	Select Info.	Assessment information is displayed.
RFO-WF-007	Verify History tab	Select History.	Assessment history is displayed.
RFO-WF-008	Verify Case ID	Review Case ID.	Case ID matches the assessment.
RFO-WF-009	Verify Initiative Category	Review Initiative Category.	Correct category is displayed.
RFO-WF-010	Verify Responsible Person	Review Responsible Person.	Correct user is displayed.
RFO-WF-011	Verify Accountable Executive	Review Accountable Executive.	Correct user is displayed.
RFO-WF-012	Verify MT Sponsor	Review MT Sponsor.	Correct user is displayed.
RFO-WF-013	Verify Business/Function	Review Business/Function.	Correct selected values are displayed.
RFO-WF-014	Verify CFCR RFOs	Review CFCR RFOs.	Correct RFO assignment is displayed.
RFO-WF-015	Verify Transaction hyperlink	Click Transaction / Click to View.	Transaction popup opens.
RFO-WF-016	Verify Transaction popup	Review popup.	Complete Transaction description is displayed.
RFO-WF-017	Verify Rationale hyperlink	Click Rationale / Click to View.	Rationale popup opens.
RFO-WF-018	Verify Rationale popup	Review popup.	Complete Rationale description is displayed.
RFO-WF-019	Verify category-specific details	Open each category.	Category-specific fields match PM-submitted data.
RFO-WF-020	Verify RFO read-only access	Attempt to edit PM-entered assessment information.	PM-entered information is read-only to RFO.

⸻

21. RFO — RISK ASSESSMENT REVIEW

ID	Test Scenario	Test Steps	Expected Result
RFO-RA-001	Verify Risk Assessment stage	Navigate to Risk Assessment.	Risk Assessment information is displayed.
RFO-RA-002	Verify Initiative information	Review carried-forward information.	Initiative information matches PM submission.
RFO-RA-003	Verify Potential COI Risk	Review Potential COI Risk.	PM response is displayed correctly.
RFO-RA-004	Verify Potential COI Risk = No	Review a No-response assessment.	Potential COI Risk displays No.
RFO-RA-005	Verify Potential COI Risk = Yes	Review a Yes-response assessment.	Potential COI Risk displays Yes.
RFO-RA-006	Verify dependent risk details	Review applicable details where Yes was selected.	Required COI risk details are displayed.
RFO-RA-007	Verify RFO read-only Risk Assessment	Attempt to edit Risk Assessment responses.	Risk Assessment responses are read-only to RFO.
RFO-RA-008	Verify Risk Assessment data accuracy	Compare assessment against PM-entered data.	RFO sees the same submitted Risk Assessment data.

⸻

22. RFO — MITIGATION PLAN REVIEW

ID	Test Scenario	Test Steps	Expected Result
RFO-MP-001	Verify Mitigation Plan stage	Navigate to Mitigation Plan.	Mitigation Plan stage is displayed.
RFO-MP-002	Verify mitigation target	Review mitigation target.	Correct target information is displayed.
RFO-MP-003	Verify Action Owner	Review Action Owner.	Correct Action Owner is displayed.
RFO-MP-004	Verify Mitigation Plan status	Review mitigation Status.	Correct status is displayed.
RFO-MP-005	Verify supporting document	Open supporting document.	Supporting document is accessible where permitted.
RFO-MP-006	Verify mitigation mapping	Review mitigation-to-question mapping.	Mapping is displayed correctly.
RFO-MP-007	Verify multiple-question mapping	Review a multi-question mapping.	One mitigation plan is correctly mapped to permitted questions.
RFO-MP-008	Verify RFO read-only access	Attempt to modify mitigation information.	PM-entered mitigation information remains read-only.

⸻

23. RFO — ENDORSEMENT

ID	Test Scenario	Test Steps	Expected Result
RFO-END-001	Verify RFO/Coverage status - 1LOD	Open RFO coverage section.	RFO/Coverage status - 1LOD is displayed.
RFO-END-002	Verify applicable endorsement action	Review available actions.	Applicable RFO endorsement actions are displayed.
RFO-END-003	Verify Endorse action	Select Endorse.	Endorsement action is available.
RFO-END-004	Verify endorsement submission	Complete required endorsement information and submit.	RFO endorsement is submitted successfully.
RFO-END-005	Verify endorsement comments	Enter applicable endorsement comments.	Endorsement comments are saved.
RFO-END-006	Verify optional endorsement comments	Submit endorsement without optional comments.	Endorsement is submitted successfully where comments are optional.
RFO-END-007	Verify endorsement status	Complete endorsement and review status.	RFO endorsement status is updated.
RFO-END-008	Verify PM receives endorsement status	Open assessment as PM.	Updated RFO endorsement status is visible to PM.
RFO-END-009	Verify Refer Back action	Select Refer Back.	Refer Back action is available.
RFO-END-010	Verify Refer Back comments mandatory	Select Refer Back without comments.	Refer Back cannot be submitted without required comments.
RFO-END-011	Verify Refer Back with comments	Enter comments and submit.	Assessment is referred back with the comments.
RFO-END-012	Verify PM receives Refer Back	Open assessment as PM.	PM can view RFO Refer Back comments.
RFO-END-013	Verify multiple RFO endorsement tracking	Complete endorsement for one of multiple RFOs.	Individual RFO endorsement status is updated correctly.
RFO-END-014	Verify remaining RFO endorsement requirement	Complete one RFO endorsement while another remains pending.	Remaining required RFO endorsement remains pending.
RFO-END-015	Verify all RFO endorsements completed	Complete all required RFO endorsements.	All required endorsements are recorded.

⸻

24. RFO — OFFLINE / FINAL

ID	Test Scenario	Test Steps	Expected Result
RFO-FIN-001	Verify Offline Endorsement	Open applicable assessment.	Offline Endorsement process is available where applicable.
RFO-FIN-002	Verify offline endorsement evidence	Review uploaded evidence.	Offline endorsement evidence is available.
RFO-FIN-003	Verify evidence association	Open evidence from assessment.	Correct evidence is associated with the assessment.
RFO-FIN-004	Verify Final endorsed risk assessment	Complete required RFO endorsement activities.	Assessment reaches Final endorsed risk assessment.
RFO-FIN-005	Verify final assessment	Review final assessment information.	Final endorsed assessment is displayed correctly.
RFO-FIN-006	Verify completion status	Complete configured final process.	Assessment moves to Completed.
RFO-FIN-007	Verify Completed Date	Review completed assessment.	Completed Date is populated correctly.
RFO-FIN-008	Verify History after completion	Open History.	RFO endorsement and completion activities are recorded.

⸻

25. RFO — WORKFLOW EXPORT

ID	Test Scenario	Test Steps	Expected Result
RFO-WFE-001	Verify Workflow Export option	Open RFO workflow.	Workflow Export is available according to permissions.
RFO-WFE-002	Verify export download	Select Export.	Workflow export downloads successfully.
RFO-WFE-003	Verify Case ID	Review Case ID.	Exported Case ID matches workflow.
RFO-WFE-004	Verify Initiative Category	Review Initiative Category.	Exported category matches workflow.
RFO-WFE-005	Verify category-specific fields	Review all applicable category fields.	Exported category-specific fields match workflow.
RFO-WFE-006	Verify Transaction	Review Transaction.	Complete Transaction is exported.
RFO-WFE-007	Verify Rationale	Review Rationale.	Complete Rationale is exported.
RFO-WFE-008	Verify Risk Assessment	Review Risk Assessment data.	Exported Risk Assessment data matches workflow.
RFO-WFE-009	Verify Mitigation Plan	Review Mitigation Plan data.	Exported Mitigation Plan data matches workflow.
RFO-WFE-010	Verify Action Owner	Review Action Owner.	Exported Action Owner matches workflow.
RFO-WFE-011	Verify mitigation Status	Review mitigation Status.	Exported status matches workflow.
RFO-WFE-012	Verify RFO/Coverage status - 1LOD	Review exported RFO coverage status.	Exported value matches workflow.
RFO-WFE-013	Verify RFO endorsement information	Review endorsement data.	Exported endorsement information matches workflow.
RFO-WFE-014	Verify RFO comments	Review RFO comments.	Exported RFO comments match workflow.
RFO-WFE-015	Verify Refer Back information	Export a referred-back assessment.	Refer Back information is exported correctly.
RFO-WFE-016	Verify Status	Review Status.	Exported Status matches workflow.
RFO-WFE-017	Verify Created By	Review Created By.	Exported Created By matches workflow.
RFO-WFE-018	Verify Created Date	Review Created Date.	Exported Created Date matches workflow.
RFO-WFE-019	Verify Last Updated Date	Review Last Updated Date.	Exported Last Updated Date matches workflow.
RFO-WFE-020	Verify Completed Date	Review Completed Date.	Exported Completed Date matches workflow.
RFO-WFE-021	Verify long Transaction	Export long Transaction data.	Complete Transaction is exported without unintended truncation.
RFO-WFE-022	Verify long Rationale	Export long Rationale data.	Complete Rationale is exported without unintended truncation.
RFO-WFE-023	Verify Workflow Export accuracy	Compare workflow with export.	Exported data matches workflow data.
RFO-WFE-024	Verify RFO access control	Export assessment as RFO.	Only permitted assessment data is exported.

⸻

FINAL WORKBOOK STRUCTURE

So when you manually create the Excel, do not make 5 summary rows like Copilot did.

Make the sheets like this:

COI PM

1. Initiative
2. Landing Page
3. Landing Page Export
4. Workflow
5. Workflow Export

COI RFO

1. Landing Page
2. Landing Page Export
3. Workflow
4. Workflow Export

And your Excel columns should simply be:

Test Case ID	Test Scenario	Test Steps	Expected Result

If your existing workbook also requires execution columns, append:

Preconditions | Test Data | Status | Actual Result | Evidence

⸻

Most important correction

The Landing Page is not just:

“Verify category selection.”

It is:

Category → every category-specific field → every common field → every interaction with those fields.

For example, NICRA is:

New Initiative Name → New Initiative Summary → First Line → Senior Manager / Group Business Head → Country Coverage → Business/Function → CFCR RFOs → Status → Created By → Created Date → Last Updated Date → Completed Date

And Corporate Action is:

Project Name → Transaction → Rationale → Responsible Person → Accountable Executive → MT Sponsor → Business/Function → CFCR RFOs → Status → Created By → Created Date → Last Updated Date → Completed Date

Then Transaction and Rationale get their own Click-to-View/popup test cases.

That is the level of granularity your senior is expecting — one validation per row, not a module summary.

Yes. Forget the Copilot workbook. We’ll do the actual cases manually here, based on the COI flow we’ve already worked through.

I’ll keep it exactly to:

Test Scenario | Test Steps | Expected Result

No Preconditions, no Test Data, no Status, no Evidence columns.

I’m also separating PM and RFO, and I’m treating Status / Created By / Created Date / Last Updated Date / Completed Date as common columns for the landing page/export.

⸻

COI — PM / Maker

1. Initiative

Test Scenario	Test Steps	Expected Result
Verify PM can access the COI Initiate Risk Assessment page	1. Login as COI PM/Maker. 2. Navigate to Change Risk Assessment. 3. Select COI. 4. Click Initiate Risk Assessment.	COI Initiate Risk Assessment page is displayed successfully.
Verify Initiative Category field	1. Open Initiate Risk Assessment. 2. Click Initiative Category.	Initiative Category field is displayed and selectable.
Verify COI category options	1. Open Initiative Category dropdown. 2. Review available options.	All COI-configured initiative categories are displayed.
Verify category selection	1. Select a COI category.	The selected category is displayed and the relevant fields are loaded.
Verify category switching	1. Select one category. 2. Change the selection to another category.	The page refreshes to display the fields applicable to the newly selected category.
Verify mandatory-field validation	1. Leave mandatory fields blank. 2. Click Submit.	Submission is prevented and validation is displayed for the mandatory fields.
Verify Project/Initiative Name field	1. Enter a valid value in the applicable name field.	The value is accepted and retained.
Verify Initiative Summary / description field	1. Enter valid text in the applicable summary/description field.	The entered text is accepted and retained.
Verify Responsible Person	1. Select/search for a Responsible Person where applicable.	The selected Responsible Person is displayed correctly.
Verify Transaction field	1. Enter transaction details.	Transaction details are accepted and retained.
Verify Rationale field	1. Enter rationale details.	Rationale details are accepted and retained.
Verify Accountable Executive / Key Stakeholder	1. Select the applicable person.	The selected person is displayed correctly.
Verify MT Sponsor	1. Select the applicable MT Sponsor.	The selected MT Sponsor is displayed correctly.
Verify Business Function	1. Open Business Function. 2. Select the applicable function.	The selected Business Function is displayed correctly.
Verify CFCR RFO population	1. Select the applicable Business Function.	The corresponding CFCR RFO is populated/displayed according to the configured mapping.
Verify Country Coverage	1. Select the applicable country coverage.	The selected country coverage is accepted and displayed.
Verify Approver field where applicable	1. Search/select the required Approver.	The selected Approver is displayed correctly.
Verify data retention before submission	1. Enter valid information in the initiation fields. 2. Navigate through the page without submitting.	Entered information remains available and is not unexpectedly cleared.
Verify successful initiation	1. Complete all mandatory fields with valid information. 2. Click Submit.	COI assessment is successfully created and the user is taken to the appropriate workflow stage/landing page.
Verify submission with incomplete information	1. Complete only some mandatory fields. 2. Click Submit.	Assessment is not submitted and the relevant missing mandatory fields are highlighted.
Verify created Case ID	1. Successfully submit a COI assessment. 2. Open the created assessment.	A unique Case ID is generated and associated with the assessment.
Verify initiated data appears in workflow	1. Submit a COI assessment. 2. Open the assessment workflow.	Information entered during initiation is displayed correctly in the workflow.

⸻

2. PM — Landing Page

Access and views

Test Scenario	Test Steps	Expected Result
Verify PM can access COI landing page	1. Login as PM. 2. Navigate to COI.	COI landing page is displayed.
Verify My Cases view	1. Select My Cases.	Only cases associated with the PM’s access/ownership are displayed.
Verify All Cases view	1. Select All Cases.	All COI cases accessible to the PM are displayed.
Verify switching from My Cases to All Cases	1. Open My Cases. 2. Select All Cases.	Grid refreshes and displays the records applicable to All Cases.
Verify switching from All Cases to My Cases	1. Open All Cases. 2. Select My Cases.	Grid refreshes and displays the records applicable to My Cases.

Category

Test Scenario	Test Steps	Expected Result
Verify Initiative Category dropdown on landing page	1. Open COI landing page. 2. Click Initiative Category dropdown.	Available COI categories are displayed.
Verify New Product / Product Change category	1. Select New Product / Product Change.	Grid displays the records belonging to the selected category and its applicable columns.
Verify Corporate Action category	1. Select Corporate Action.	Grid displays Corporate Action records and applicable Corporate Action columns.
Verify NICRA category	1. Select NICRA.	Grid displays NICRA records and applicable NICRA columns.
Verify Other category	1. Select Other.	Grid displays Other records and applicable Other columns.
Verify category switching	1. Select one category. 2. Select another category.	Grid refreshes correctly and displays the selected category’s records/columns.

Status tiles

Test Scenario	Test Steps	Expected Result
Verify In Progress tile	1. Select In Progress.	Cases currently in progress are displayed.
Verify Pending Endorsement tile	1. Select Pending Endorsement.	Cases pending RFO endorsement are displayed.
Verify Refer Back tile	1. Select Refer Back.	Cases referred back to the PM are displayed.
Verify Endorsement by RFO tile	1. Select Endorsement by RFO.	Cases for which RFO endorsement activity is applicable/ongoing are displayed.
Verify Completed tile	1. Select Completed.	Completed COI assessments are displayed.
Verify status count	1. Note the count displayed on a status tile. 2. Open the tile. 3. Count/verify displayed records.	The status count corresponds to the applicable records.
Verify status count updates	1. Complete an action that changes case status. 2. Return to landing page.	Relevant status count is updated accordingly.

Grid functions

Test Scenario	Test Steps	Expected Result
Verify Search	1. Enter a valid searchable value.	Matching records are displayed.
Verify invalid Search	1. Enter a value that does not match any record.	No matching records are displayed.
Verify clearing Search	1. Enter a search value. 2. Clear the search.	Full applicable record list is restored.
Verify Filter	1. Open filter. 2. Select a valid filter value.	Grid displays only records matching the filter.
Verify Clear Filter	1. Apply a filter. 2. Clear the filter.	All applicable records are restored.
Verify ascending sort	1. Select a sortable column. 2. Apply ascending sort.	Records are arranged in ascending order.
Verify descending sort	1. Select a sortable column. 2. Apply descending sort.	Records are arranged in descending order.
Verify pagination	1. Navigate through available pages.	Correct records are displayed on each page.
Verify page navigation	1. Select next/previous page.	User moves to the correct page and corresponding records are displayed.
Verify horizontal scrolling	1. Scroll horizontally across the grid.	All configured columns can be accessed without data loss.

⸻

3. PM — Landing Page Columns

Corporate Action example

Test Scenario	Test Steps	Expected Result
Verify Case ID column	1. Select Corporate Action. 2. Review Case ID column.	Correct Case ID is displayed for each case.
Verify Trigger Event / Driver column	1. Review Trigger Event / Driver.	Correct Trigger Event / Driver is displayed.
Verify Project Name column	1. Review Project Name.	Correct Project Name is displayed.
Verify Responsible Person column	1. Review Responsible Person.	Correct Responsible Person is displayed.
Verify Transaction column	1. Review Transaction column.	Transaction is displayed using the configured Click to View behaviour where applicable.
Verify Rationale column	1. Review Rationale column.	Rationale is displayed using the configured Click to View behaviour where applicable.
Verify Accountable Executive / Key Stakeholder column	1. Review the column.	Correct Accountable Executive / Key Stakeholder is displayed.
Verify MT Sponsor column	1. Review MT Sponsor.	Correct MT Sponsor is displayed.
Verify Business Function column	1. Review Business Function.	Correct Business Function is displayed.
Verify CFCR RFO column	1. Review CFCR RFO.	Correct CFCR RFO is displayed.
Verify Status column	1. Review Status.	Current status of each case is displayed correctly.
Verify Created By column	1. Review Created By.	Correct creator is displayed.
Verify Created Date column	1. Review Created Date.	Correct creation date is displayed.
Verify Last Updated Date column	1. Review Last Updated Date.	Correct last updated date is displayed.
Verify Completed Date column	1. Review Completed Date for completed/non-completed cases.	Completed Date is displayed correctly for completed cases and remains appropriately blank/not applicable for cases not completed.
Verify Transaction Click to View	1. Click Transaction / Click to View.	Full Transaction content is displayed.
Verify Rationale Click to View	1. Click Rationale / Click to View.	Full Rationale content is displayed.
Verify Transaction content accuracy	1. Open Transaction. 2. Compare with data entered in workflow.	Full Transaction content matches the workflow data.
Verify Rationale content accuracy	1. Open Rationale. 2. Compare with data entered in workflow.	Full Rationale content matches the workflow data.

For New Product/Product Change, NICRA and Other, create the same individual column-level cases using the exact category-specific columns shown in the application.
The five common cases — Status, Created By, Created Date, Last Updated Date, Completed Date — remain applicable to every category.

⸻

4. PM — Landing Page Export

Test Scenario	Test Steps	Expected Result
Verify Landing Page Export option	1. Open COI landing page. 2. Review available actions.	Export option is available to the PM.
Verify My Cases export	1. Select My Cases. 2. Export the grid.	Export contains the applicable My Cases records.
Verify All Cases export	1. Select All Cases. 2. Export the grid.	Export contains the applicable All Cases records.
Verify category export	1. Select a COI category. 2. Export.	Export contains records for the selected category.
Verify export download	1. Click Export.	Export file downloads successfully.
Verify export file opens	1. Open downloaded file.	File opens successfully without corruption.
Verify exported Case ID	1. Open export. 2. Review Case ID.	Exported Case ID matches the landing page.
Verify exported category-specific fields	1. Open export. 2. Review each category-specific column.	Exported values match the landing page values.
Verify exported Status	1. Review Status in export.	Status matches the landing page.
Verify exported Created By	1. Review Created By.	Value matches the landing page.
Verify exported Created Date	1. Review Created Date.	Value matches the landing page.
Verify exported Last Updated Date	1. Review Last Updated Date.	Value matches the landing page.
Verify exported Completed Date	1. Review Completed Date.	Value matches the landing page.
Verify Transaction export	1. Export a Corporate Action record. 2. Review Transaction.	Complete Transaction information is exported without unintended truncation.
Verify Rationale export	1. Export a Corporate Action record. 2. Review Rationale.	Complete Rationale information is exported without unintended truncation.
Verify filtered export	1. Apply a filter. 2. Export.	Export reflects the applicable filtered records.
Verify searched export	1. Perform a search. 2. Export.	Export reflects the applicable search results.
Verify status-based export	1. Select a status tile. 2. Export.	Export contains the records applicable to the selected status.
Verify export data accuracy	1. Compare exported data against landing page data.	Exported information accurately matches the landing page.

⸻

5. PM — Workflow

General workflow

Test Scenario	Test Steps	Expected Result
Verify PM can open assessment	1. Open COI landing page. 2. Select a case.	Selected COI assessment opens successfully.
Verify workflow is displayed	1. Open an assessment.	COI workflow is displayed.
Verify workflow stages	1. Review workflow progress indicator.	Configured COI workflow stages are displayed in the correct sequence.
Verify current stage	1. Open an assessment in progress.	Current workflow stage is clearly indicated.
Verify current status	1. Open assessment.	Current assessment status is displayed correctly.
Verify Details panel	1. Open Details panel.	Case information is displayed.
Verify Info tab	1. Open Info tab.	Assessment information is displayed.
Verify History tab	1. Open History tab.	Relevant assessment history/audit information is displayed.
Verify Case ID in Details	1. Open Details.	Correct Case ID is displayed.
Verify Initiative Category in Details	1. Open Details.	Correct Initiative Category is displayed.
Verify Trigger Event / Driver in Details	1. Open Details.	Correct Trigger Event / Driver is displayed where applicable.
Verify Project Name in Details	1. Open Details.	Correct Project Name is displayed where applicable.
Verify Responsible Person in Details	1. Open Details.	Correct Responsible Person is displayed.
Verify Transaction in Details	1. Open Details. 2. Select Transaction/Click to View.	Complete Transaction information is displayed.
Verify Rationale in Details	1. Open Details. 2. Select Rationale/Click to View.	Complete Rationale information is displayed.
Verify Accountable Executive	1. Open Details.	Correct Accountable Executive is displayed.
Verify MT Sponsor	1. Open Details.	Correct MT Sponsor is displayed.
Verify Business Function	1. Open Details.	Correct Business Function is displayed.
Verify CFCR RFO	1. Open Details.	Correct CFCR RFO is displayed.

⸻

6. PM — Risk Assessment

Test Scenario	Test Steps	Expected Result
Verify Risk Assessment stage	1. Open an assessment at Risk Assessment stage.	Risk Assessment stage is displayed correctly.
Verify risk questions	1. Navigate through the Risk Assessment.	Applicable COI risk questions are displayed.
Verify Potential COI Risk question	1. Review Potential COI Risk.	Potential COI Risk question is displayed and is mandatory where specified.
Verify Potential COI Risk = Yes	1. Select Yes for Potential COI Risk.	Applicable follow-up risk information is displayed/enabled.
Verify Potential COI Risk = No	1. Select No.	Applicable follow-up fields behave according to the requirement.
Verify mandatory Potential COI Risk	1. Leave Potential COI Risk unanswered. 2. Attempt to proceed.	User cannot proceed and mandatory validation is displayed.
Verify risk response persistence	1. Enter risk responses. 2. Navigate through workflow.	Entered risk responses are retained.
Verify PM can edit risk responses	1. Open Risk Assessment as PM. 2. Modify an editable response.	PM can modify permitted responses.
Verify risk response data appears in subsequent stage	1. Complete Risk Assessment. 2. Navigate to next applicable stage.	Relevant risk assessment information is carried forward correctly.

⸻

7. PM — Mitigation Plan

Test Scenario	Test Steps	Expected Result
Verify Mitigation Plan stage	1. Complete applicable Risk Assessment information. 2. Navigate to Mitigation Plan.	Mitigation Plan stage is displayed.
Verify mitigation plan creation	1. Add a mitigation plan. 2. Enter required information.	Mitigation plan is created successfully.
Verify mitigation target	1. Enter target information.	Target is accepted and retained.
Verify action owner	1. Select Action Owner.	Available applicable owners are displayed and selected value is retained.
Verify mitigation status	1. Open mitigation status dropdown.	Configured status values are displayed.
Verify supporting document upload	1. Upload a supporting document where required/available.	Document is uploaded and associated with the mitigation plan.
Verify supporting document is optional where specified	1. Leave optional supporting document blank. 2. Proceed.	User can proceed without the optional document.
Verify mitigation plan mapping	1. Select the applicable COI question/risk item. 2. Map mitigation plan to it.	Mitigation plan is mapped to the selected item.
Verify mitigation plan mapping to multiple questions	1. Create one mitigation plan. 2. Select multiple applicable questions.	One mitigation plan can be mapped to the permitted multiple questions.
Verify mitigation plan data persistence	1. Save/proceed. 2. Return to Mitigation Plan.	Previously entered mitigation information is retained.
Verify mandatory mitigation information	1. Leave required mitigation information blank. 2. Attempt to proceed.	User cannot proceed and the required field validation is displayed.

⸻

8. PM — Pending Endorsement / RFO Coverage

Test Scenario	Test Steps	Expected Result
Verify Pending Endorsement stage	1. Complete applicable PM assessment information. 2. Submit for endorsement.	Assessment moves to Pending Endorsement.
Verify assigned RFO	1. Open assessment after submission.	Applicable RFO/coverage information is displayed.
Verify RFO coverage status	1. Open RFO/Coverage status section.	Correct RFO coverage status is displayed.
Verify RFO comments visibility	1. Open RFO comments after RFO has provided comments.	Relevant RFO comments are visible to PM.
Verify RFO endorsement status	1. Open assessment after RFO endorsement.	RFO endorsement status is updated correctly.
Verify RFO refer-back status	1. Open assessment after RFO refers back.	Assessment status changes to Refer Back and PM can review the feedback.
Verify PM can review refer-back comments	1. Open referred-back assessment.	RFO refer-back comments are displayed to PM.
Verify PM can amend referred-back assessment	1. Open a referred-back assessment. 2. Modify the required information.	PM can make permitted amendments.
Verify resubmission after refer back	1. Correct the referred-back information. 2. Resubmit.	Assessment is resubmitted for RFO review.

⸻

9. PM — Offline Endorsement / Final Submission

Test Scenario	Test Steps	Expected Result
Verify Offline Endorsement option where applicable	1. Open assessment requiring offline endorsement.	Offline endorsement functionality is available as configured.
Verify PM uploads offline endorsement evidence	1. Obtain offline endorsement evidence. 2. Upload the evidence.	Evidence is uploaded successfully and associated with the assessment.
Verify uploaded evidence	1. Open uploaded evidence.	Correct endorsement evidence is available for review.
Verify final endorsement information	1. Review RFO endorsement/coverage information.	Endorsement information is accurately displayed.
Verify final submission	1. Complete required endorsement/coverage information. 2. Perform final submission.	Assessment is submitted successfully for final completion.
Verify completed status	1. Complete the required final workflow action. 2. Return to landing page.	Assessment moves to Completed status.
Verify Completed Date	1. Open completed assessment.	Completed Date is populated correctly.
Verify history after completion	1. Open History.	Final submission/completion activity is recorded in the history.

⸻

10. PM — Workflow Export

Test Scenario	Test Steps	Expected Result
Verify Workflow Export option	1. Open COI workflow. 2. Review available actions.	Workflow Export option is available.
Verify workflow export download	1. Select Workflow Export.	Export file downloads successfully.
Verify workflow export file	1. Open downloaded file.	File opens successfully.
Verify exported Case ID	1. Review Case ID in export.	Case ID matches workflow.
Verify exported Initiative Category	1. Review Initiative Category.	Value matches workflow.
Verify exported category-specific information	1. Review all applicable category-specific fields.	Values match workflow information.
Verify exported Transaction	1. Review Transaction in export.	Complete Transaction information is exported.
Verify exported Rationale	1. Review Rationale in export.	Complete Rationale information is exported.
Verify exported Risk Assessment information	1. Review risk assessment fields.	Export contains the applicable workflow risk assessment information.
Verify exported Mitigation Plan information	1. Review mitigation plan fields.	Export contains the applicable mitigation information.
Verify exported RFO information	1. Review RFO-related information.	Correct RFO information is exported.
Verify exported RFO status	1. Review RFO status.	Exported RFO status matches workflow.
Verify exported RFO comments	1. Review RFO comments.	Applicable comments are exported correctly.
Verify exported Status	1. Review Status.	Status matches workflow.
Verify exported Created By	1. Review Created By.	Value matches workflow.
Verify exported Created Date	1. Review Created Date.	Value matches workflow.
Verify exported Last Updated Date	1. Review Last Updated Date.	Value matches workflow.
Verify exported Completed Date	1. Review Completed Date.	Value matches workflow.
Verify long text is not truncated	1. Export an assessment containing long Transaction/Rationale content. 2. Review export.	Complete long-text content is available in the export.
Verify export data matches workflow	1. Compare exported information against workflow UI.	Exported data accurately matches workflow information.
Verify export after refer back	1. Export a referred-back/re-submitted assessment.	Export reflects the latest applicable workflow information.
Verify export after completion	1. Export a completed assessment.	Export contains the final completed assessment information.

⸻

COI — RFO

Now the RFO suite.

No Initiative sheet for RFO.

The RFO starts from the landing page and works through the assessment assigned to them.

⸻

11. RFO — Landing Page

Test Scenario	Test Steps	Expected Result
Verify RFO can access COI landing page	1. Login as RFO. 2. Navigate to COI.	COI landing page is displayed successfully.
Verify RFO My Cases	1. Select My Cases.	Cases assigned/relevant to the RFO are displayed according to RFO access.
Verify RFO All Cases access	1. Select All Cases where available.	RFO sees only records permitted by their access rights.
Verify category dropdown	1. Open Initiative Category dropdown.	Available COI categories are displayed.
Verify New Product / Product Change	1. Select New Product / Product Change.	Applicable records and columns are displayed.
Verify Corporate Action	1. Select Corporate Action.	Applicable Corporate Action records and columns are displayed.
Verify NICRA	1. Select NICRA.	Applicable NICRA records and columns are displayed.
Verify Other	1. Select Other.	Applicable Other records and columns are displayed.
Verify category switching	1. Select one category. 2. Select another.	Grid refreshes to the selected category.
Verify In Progress tile	1. Select In Progress.	Applicable In Progress cases are displayed.
Verify Pending Endorsement tile	1. Select Pending Endorsement.	Applicable Pending Endorsement cases are displayed.
Verify Refer Back tile	1. Select Refer Back.	Applicable Refer Back cases are displayed according to RFO access.
Verify Endorsement by RFO tile	1. Select Endorsement by RFO.	Applicable RFO endorsement cases are displayed.
Verify Completed tile	1. Select Completed.	Applicable completed cases are displayed.
Verify status counts	1. Review each status count. 2. Select the relevant status.	Count and displayed records are consistent.
Verify Search	1. Enter a valid search value.	Matching accessible records are displayed.
Verify invalid Search	1. Enter a non-matching value.	No matching records are displayed.
Verify Filter	1. Apply a valid filter.	Only matching accessible records are displayed.
Verify Clear Filter	1. Apply filter. 2. Clear filter.	Original accessible record list is restored.
Verify ascending sort	1. Sort a column ascending.	Records are sorted correctly.
Verify descending sort	1. Sort a column descending.	Records are sorted correctly.
Verify Pagination	1. Navigate through pages.	Correct accessible records are displayed on each page.
Verify horizontal scrolling	1. Scroll horizontally through the grid.	All configured columns can be viewed.

⸻

12. RFO — Landing Page Columns

Use the same category-specific columns as the PM landing page, but validate them from the RFO’s access perspective.

Test Scenario	Test Steps	Expected Result
Verify Case ID column	1. Open an RFO-accessible category. 2. Review Case ID.	Correct Case ID is displayed.
Verify category-specific columns	1. Select the relevant category. 2. Review each configured category-specific column individually.	Each column displays the correct information.
Verify Transaction Click to View	1. Select Transaction/Click to View.	Full Transaction content is displayed.
Verify Rationale Click to View	1. Select Rationale/Click to View.	Full Rationale content is displayed.
Verify Status	1. Review Status.	Correct current status is displayed.
Verify Created By	1. Review Created By.	Correct creator is displayed.
Verify Created Date	1. Review Created Date.	Correct creation date is displayed.
Verify Last Updated Date	1. Review Last Updated Date.	Correct last updated date is displayed.
Verify Completed Date	1. Review Completed Date.	Correct completed date is displayed for completed assessments.
Verify RFO access restriction	1. Compare records visible to RFO with records outside RFO access.	RFO cannot access records outside the permitted scope.

⸻

13. RFO — Landing Page Export

Test Scenario	Test Steps	Expected Result
Verify RFO Landing Page Export option	1. Open RFO landing page.	Export option is available according to RFO permissions.
Verify RFO export download	1. Select Export.	Export file downloads successfully.
Verify export file opens	1. Open downloaded file.	File opens successfully.
Verify exported Case ID	1. Review Case ID.	Exported Case ID matches landing page.
Verify exported category-specific fields	1. Review each applicable category-specific field.	Exported values match landing page.
Verify exported Status	1. Review Status.	Status matches landing page.
Verify exported Created By	1. Review Created By.	Value matches landing page.
Verify exported Created Date	1. Review Created Date.	Value matches landing page.
Verify exported Last Updated Date	1. Review Last Updated Date.	Value matches landing page.
Verify exported Completed Date	1. Review Completed Date.	Value matches landing page.
Verify Transaction export	1. Export a record containing Transaction. 2. Review export.	Complete Transaction information is exported.
Verify Rationale export	1. Export a record containing Rationale. 2. Review export.	Complete Rationale information is exported.
Verify filtered export	1. Apply filter. 2. Export.	Export reflects applicable filtered records.
Verify searched export	1. Search for a record. 2. Export.	Export reflects applicable search results.
Verify status-based export	1. Select status tile. 2. Export.	Export contains applicable records.
Verify RFO access-controlled export	1. Export records as RFO.	Export does not expose records/data outside the RFO’s permitted access.
Verify export matches landing page	1. Compare landing page and export.	Exported data matches landing-page data.

⸻

14. RFO — Workflow

General access

Test Scenario	Test Steps	Expected Result
Verify RFO can open assigned assessment	1. Login as RFO. 2. Open an assessment assigned to the RFO.	Assessment opens successfully.
Verify RFO cannot access unauthorized assessment	1. Attempt to open an assessment outside RFO access.	Access is restricted according to permissions.
Verify workflow stages	1. Open assigned assessment.	Configured workflow stages are displayed.
Verify current stage	1. Open assigned assessment.	Current stage is displayed correctly.
Verify current status	1. Open assigned assessment.	Current status is displayed correctly.
Verify Details panel	1. Open Details.	Relevant assessment details are displayed.
Verify Info tab	1. Open Info.	Assessment information is displayed.
Verify History tab	1. Open History.	Relevant workflow history is displayed.
Verify Case ID	1. Open Details.	Correct Case ID is displayed.
Verify Initiative Category	1. Open Details.	Correct category is displayed.
Verify Project/Initiative information	1. Open Details.	PM-entered initiative/project information is displayed correctly.
Verify Transaction	1. Open Transaction/Click to View.	Complete Transaction information is available for RFO review.
Verify Rationale	1. Open Rationale/Click to View.	Complete Rationale information is available for RFO review.
Verify Business Function	1. Open Details.	Correct Business Function is displayed.
Verify CFCR RFO	1. Open Details.	Correct RFO/coverage information is displayed.

⸻

15. RFO — Risk Assessment Review

Test Scenario	Test Steps	Expected Result
Verify RFO can view Risk Assessment	1. Open assigned assessment. 2. Navigate to Risk Assessment.	RFO can view the applicable Risk Assessment information.
Verify PM-entered risk responses	1. Review risk responses.	PM-entered responses are displayed correctly.
Verify RFO read-only access	1. Attempt to edit PM-entered risk assessment information.	RFO cannot edit information that is read-only for the RFO.
Verify Potential COI Risk response	1. Review Potential COI Risk response.	Correct response entered by PM is displayed.
Verify supporting risk information	1. Review applicable risk information.	All relevant information is available for RFO review.
Verify risk information consistency	1. Compare Risk Assessment information with landing/workflow information.	Information is consistent across the assessment.

⸻

16. RFO — Mitigation Plan Review

Test Scenario	Test Steps	Expected Result
Verify RFO can view Mitigation Plan	1. Open assessment. 2. Navigate to Mitigation Plan.	RFO can view applicable mitigation plans.
Verify mitigation target	1. Review target.	Correct target is displayed.
Verify mitigation Action Owner	1. Review Action Owner.	Correct Action Owner is displayed.
Verify mitigation status	1. Review mitigation status.	Correct status is displayed.
Verify supporting document	1. Open supporting document where available.	Document is accessible to the RFO where permitted.
Verify mitigation mapping	1. Review mitigation plan mapping to risk questions.	Mapping is displayed correctly.
Verify multiple-question mapping	1. Review a mitigation plan mapped to multiple questions.	Mapping to the applicable multiple questions is displayed correctly.
Verify RFO cannot edit PM mitigation information where read-only	1. Attempt to edit PM-entered mitigation information.	RFO cannot edit fields configured as read-only.

⸻

17. RFO — Endorsement

Test Scenario	Test Steps	Expected Result
Verify RFO endorsement stage	1. Open assessment pending RFO endorsement.	Endorsement stage is displayed.
Verify RFO coverage status	1. Open RFO/Coverage status section.	Correct coverage information is displayed.
Verify RFO can endorse	1. Complete the required RFO review. 2. Select Endorse.	RFO can submit endorsement successfully.
Verify endorsement mandatory action	1. Attempt to complete the stage without selecting an endorsement action.	Assessment cannot be completed until the required endorsement action is selected.
Verify endorsement comments	1. Enter comments where applicable. 2. Submit endorsement.	Comments are saved and associated with the endorsement.
Verify endorsement status update	1. Submit endorsement. 2. Review assessment status.	RFO endorsement status is updated correctly.
Verify PM receives endorsement status	1. Endorse assessment as RFO. 2. Login/open as PM.	PM can see the updated RFO endorsement status.
Verify individual RFO endorsement	1. Complete endorsement for the applicable business/function coverage.	The relevant RFO endorsement is recorded correctly.
Verify other RFO behaviour after individual endorsement	1. Have one applicable RFO complete endorsement. 2. Review the assessment for other RFOs.	System applies the configured endorsement/coverage logic and updates the requirement for other RFOs where applicable.

⸻

18. RFO — Refer Back

Test Scenario	Test Steps	Expected Result
Verify RFO can Refer Back	1. Open assigned assessment. 2. Select Refer Back.	Refer Back action is available where applicable.
Verify Refer Back comments mandatory	1. Select Refer Back. 2. Leave comments blank. 3. Submit.	Refer Back cannot be submitted without the required comments.
Verify Refer Back with comments	1. Select Refer Back. 2. Enter comments. 3. Submit.	Assessment is successfully referred back to PM.
Verify Refer Back status	1. Refer back the assessment. 2. Review status.	Assessment status changes to Refer Back.
Verify PM can see Refer Back comments	1. Refer back assessment. 2. Open as PM.	PM can view the RFO’s refer-back comments.
Verify RFO sees updated assessment after resubmission	1. PM corrects the assessment. 2. PM resubmits. 3. RFO opens it.	Updated assessment is available for RFO review.
Verify RFO can endorse after resubmission	1. Review corrected assessment. 2. Select Endorse.	RFO can endorse the resubmitted assessment.

⸻

19. RFO — Offline Endorsement

Test Scenario	Test Steps	Expected Result
Verify Offline Endorsement process	1. Review assessment requiring offline endorsement.	Offline endorsement process is available where configured.
Verify offline endorsement evidence	1. Complete endorsement outside the system as required. 2. PM uploads evidence.	Evidence is associated with the assessment.
Verify offline endorsement evidence visibility	1. Open assessment after evidence upload.	Relevant endorsement evidence is available for review according to RFO permissions.
Verify offline endorsement status	1. Review RFO/Coverage status after offline endorsement.	Status reflects the configured offline endorsement process.

⸻

20. RFO — Final / Completion

Test Scenario	Test Steps	Expected Result
Verify final endorsement information	1. Review all applicable RFO endorsements.	Correct endorsement information is displayed.
Verify all required RFO endorsements	1. Review assessment with multiple RFOs.	System accurately reflects completion/pending status of required RFO endorsements.
Verify final completion	1. Complete the required RFO endorsement activity. 2. Complete any configured final action.	Assessment progresses to the appropriate final/completed state.
Verify Completed status	1. Return to landing page after completion.	Assessment appears under Completed status.
Verify Completed Date	1. Open completed assessment.	Completed Date is populated correctly.
Verify completion history	1. Open History.	Endorsement and completion activities are recorded in the audit/history.

⸻

21. RFO — Workflow Export

Test Scenario	Test Steps	Expected Result
Verify RFO Workflow Export option	1. Open RFO workflow.	Workflow Export is available according to permissions.
Verify RFO workflow export download	1. Select Export.	Export file downloads successfully.
Verify exported Case ID	1. Review Case ID.	Case ID matches the workflow.
Verify exported category	1. Review Initiative Category.	Category matches workflow.
Verify exported category-specific fields	1. Review applicable category-specific fields.	Values match workflow.
Verify exported Transaction	1. Review Transaction.	Complete Transaction information is exported.
Verify exported Rationale	1. Review Rationale.	Complete Rationale information is exported.
Verify exported Risk Assessment	1. Review risk assessment information.	Applicable risk assessment information is exported correctly.
Verify exported Mitigation Plan	1. Review mitigation information.	Applicable mitigation plan information is exported correctly.
Verify exported RFO status	1. Review RFO status.	Exported RFO status matches workflow.
Verify exported RFO comments	1. Review RFO comments.	Applicable RFO comments are exported correctly.
Verify exported endorsement information	1. Review endorsement information.	Endorsement details match workflow.
Verify exported Refer Back information	1. Review a referred-back assessment export.	Relevant Refer Back information/comments are exported correctly.
Verify exported Status	1. Review Status.	Status matches workflow.
Verify exported Created By	1. Review Created By.	Value matches workflow.
Verify exported Created Date	1. Review Created Date.	Value matches workflow.
Verify exported Last Updated Date	1. Review Last Updated Date.	Value matches workflow.
Verify exported Completed Date	1. Review Completed Date.	Value matches workflow.
Verify long Transaction is not truncated	1. Export assessment with long Transaction. 2. Review export.	Complete Transaction is available.
Verify long Rationale is not truncated	1. Export assessment with long Rationale. 2. Review export.	Complete Rationale is available.
Verify export matches workflow	1. Compare workflow UI with exported data.	Exported information accurately matches the workflow.
Verify RFO export access control	1. Export assessment as RFO. 2. Review exported information.	Export contains only information the RFO is permitted to access.

⸻

The structure you should manually create

So your COI workbook will effectively be:

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

And don’t make the mistake of creating one generic “Category Columns” test case.

For every category, you expand the actual fields individually. And the common landing-page fields are always:

* Status
* Created By
* Created Date
* Last Updated Date
* Completed Date

Also, Transaction and Rationale each need both UI and data-validation coverage because the landing page shows them through Click to View rather than displaying the entire description directly.

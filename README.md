Test Scenario

Test Steps

Expected Result

Verify header is displayed on top of the screen

1. Login to Service Bench application.2. Navigate to Conduct Risk plugins.3. Click Conduct Risk Assessment → Initiate Risk Assessment.4. Select Project ID and impacted Business Function with RFO.5. Complete Part 1 and click Next.

1. User navigates to Risk Assessment – Part 2.2. Header is displayed as Conduct – Risk Assessment.

Verify details panel is displayed

Same navigation steps as above.

Case ID, Initiative ID, Programme ID, Initiative Name, Programme Name, Impacted Business Function and other details are displayed as read-only.

Verify sensitive data warning visibility

Same navigation steps.

Sensitive Data Warning message is displayed.

Verify guideline visibility

Same navigation steps.

Conduct guideline section and View Guideline link are displayed.

Verify only eligible Conduct Risk Areas are displayed

1. In Part 1 mark selected Conduct Areas as Applicability = Yes and Conduct Risk = Yes.2. Complete Part 1.3. Click Next.

Only Conduct Risk Areas where Applicability = Yes and Conduct Risk = Yes are displayed in Part 2.

Verify Conduct Risk Description is displayed from Part 1

1. Enter Conduct Risk Description in Part 1.2. Navigate to Part 2.

Conduct Risk Description entered in Part 1 is displayed against the corresponding Conduct Risk Area.

Verify updated Conduct Risk Description synchronization

1. Navigate back to Part 1.2. Update Conduct Risk Description.3. Save and return to Part 2.

Latest saved Conduct Risk Description is displayed in Part 2.

Verify Conduct Risk Impact Scale dropdown

Navigate to Part 2.

Impact Scale dropdown is displayed with values Red, Amber and Green.

Verify Red impact scale selection

Select Red from the dropdown.

Red is selected successfully and Upload Document field becomes mandatory.

Verify Amber impact scale selection

Select Amber from the dropdown.

Amber is selected successfully and Upload Document field becomes mandatory.

Verify Green impact scale selection

Select Green from the dropdown.

Green is selected successfully and Upload Document field remains optional.

Verify Upload Document is mandatory for Red

Select Red and click Next/Submit without uploading a document.

Validation message is displayed and user cannot proceed until a document is uploaded.

Verify Upload Document is mandatory for Amber

Select Amber and click Next/Submit without uploading a document.

Validation message is displayed and user cannot proceed until a document is uploaded.

Verify Upload Document is optional for Green

Select Green and click Next without uploading a document.

User can proceed without uploading a document.

Verify Upload Document functionality

Click Upload Document and select a supported file.

Document uploads successfully and filename is displayed.

Verify Remove Uploaded Document

Upload a document and click the Delete/Remove icon.

Uploaded document is removed successfully.

Verify Replace Uploaded Document

Upload a document, remove it and upload another document.

Newly uploaded document replaces the previous document successfully.

Verify warning popup when Conduct Risk Area is removed in Part 1

1. Complete Part 2.2. Navigate back to Part 1.3. Change Applicability Yes→No or Conduct Risk Yes→No for an existing Conduct Area.

Confirmation popup is displayed stating that downstream data in Part 2 and Mitigation Plan will be removed.

Verify Confirm removes downstream data from Part 2

Click Confirm in the warning popup and navigate to Part 2.

Corresponding Conduct Risk Area, Conduct Risk Description, Impact Scale and uploaded document are removed from Part 2.

Verify Cancel retains downstream data

Click Cancel in the warning popup and return to Part 2.

Previously entered Conduct Risk Area, Description, Impact Scale and uploaded document remain unchanged.

Verify Save as Draft functionality

Complete Part 2 and click Save as Draft.

Assessment is saved successfully, remains in In Progress status and user is redirected appropriately.

Verify Clear All functionality

Enter Impact Scale and upload a document. Click Clear All.

All user-entered values are cleared while auto-populated project details remain unchanged.

Verify Previous button navigation

Click Previous.

User navigates back to Risk Assessment – Part 1.

Verify Next button navigation

Complete all mandatory fields and click Next.

User navigates to Mitigation Plan & Commentary screen.

Verify Submit functionality

Complete all mandatory fields and click Submit.

Assessment is submitted successfully and moves to the next workflow stage.

Verify mandatory field validations

Leave mandatory fields blank and click Next/Submit.

Validation messages are displayed and user cannot proceed until mandatory fields are completed.

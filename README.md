Common Test Steps (Steps 1–6)

1. Login to Service Bench application.
2. Navigate to Conduct Risk plugins → Click Conduct Risk Assessment plugin → Click Initiate Risk Assessment.
3. Select Project ID and Impacted Business Function with RFO.
4. Click Submit.
5. Complete Risk Assessment – Part 1.
6. Click Next to navigate to Risk Assessment – Part 2.

⸻

TC-01 Verify header is displayed on top of the screen

Test Steps

Common Steps (1–6)

Expected Result

1. User navigates to Risk Assessment – Part 2.
2. Header is displayed as Conduct – Risk Assessment.

⸻

TC-02 Verify Details panel is displayed

Test Steps

Common Steps (1–6)

Expected Result

1. Case ID is displayed.
2. Initiative ID is displayed.
3. Programme ID is displayed.
4. Initiative Name is displayed.
5. Programme Name is displayed.
6. Impacted Business Function is displayed.
7. Details are read-only.

⸻

TC-03 Verify Sensitive Data Warning visibility

Test Steps

Common Steps (1–6)

Expected Result

1. Sensitive Data Warning message is displayed.

⸻

TC-04 Verify Guideline visibility

Test Steps

Common Steps (1–6)

7. Click View Guideline.

Expected Result

1. Guideline section is displayed.
2. Guideline document opens successfully.

⸻

TC-05 Verify only eligible Conduct Risk Areas are displayed

Test Steps

Common Steps (1–6)

7. Observe the Conduct Risk Areas displayed.

Expected Result

1. Only Conduct Risk Areas with Applicability = Yes and Conduct Risk = Yes are displayed.
2. Remaining Conduct Risk Areas are not displayed.

⸻

TC-06 Verify Conduct Risk Description is displayed from Part 1

Test Steps

Common Steps (1–6)

7. Observe the Conduct Risk Description for each Conduct Risk Area.

Expected Result

1. Conduct Risk Description entered in Part 1 is displayed for the corresponding Conduct Risk Area.

⸻

TC-07 Verify updated Conduct Risk Description synchronization

Test Steps

Common Steps (1–6)

7. Click Previous.
8. Update Conduct Risk Description in Part 1.
9. Click Next.
10. Observe the Conduct Risk Description.

Expected Result

1. Updated Conduct Risk Description is displayed.
2. Latest saved value is reflected in Part 2.

⸻

TC-08 Verify Conduct Risk Impact Scale dropdown

Test Steps

Common Steps (1–6)

7. Click the Conduct Risk Impact Scale dropdown.

Expected Result

1. Dropdown displays:
    * Red
    * Amber
    * Green

⸻

TC-09 Verify Red Impact Scale selection

Test Steps

Common Steps (1–6)

7. Select Red from Conduct Risk Impact Scale dropdown.

Expected Result

1. Red Impact Scale is selected successfully.
2. Upload Document field becomes mandatory.

⸻

TC-10 Verify Amber Impact Scale selection

Test Steps

Common Steps (1–6)

7. Select Amber from Conduct Risk Impact Scale dropdown.

Expected Result

1. Amber Impact Scale is selected successfully.
2. Upload Document field becomes mandatory.

⸻

TC-11 Verify Green Impact Scale selection

Test Steps

Common Steps (1–6)

7. Select Green from Conduct Risk Impact Scale dropdown.

Expected Result

1. Green Impact Scale is selected successfully.
2. Upload Document remains optional.

⸻

TC-12 Verify Upload Document mandatory for Red

Test Steps

Common Steps (1–6)

7. Select Red Impact Scale.
8. Do not upload any document.
9. Click Next.

Expected Result

1. Validation message is displayed.
2. User cannot proceed without uploading a supporting document.

⸻

TC-13 Verify Upload Document mandatory for Amber

Test Steps

Common Steps (1–6)

7. Select Amber Impact Scale.
8. Do not upload any document.
9. Click Next.

Expected Result

1. Validation message is displayed.
2. User cannot proceed without uploading a supporting document
TC-14 Verify Upload Document is optional for Green

Test Steps

Common Steps (1–6)

7. Select Green from Conduct Risk Impact Scale dropdown.
8. Do not upload a supporting document.
9. Click Next.

Expected Result

1. User is able to proceed to the next stage successfully.
2. Upload Document is optional for Green Impact Scale.

⸻

TC-15 Verify Upload Document functionality

Test Steps

Common Steps (1–6)

7. Select Red or Amber Impact Scale.
8. Click Upload Document.
9. Browse and select a supported document.
10. Upload the document.

Expected Result

1. Document is uploaded successfully.
2. Uploaded document name is displayed.

⸻

TC-16 Verify Remove Uploaded Document

Test Steps

Common Steps (1–6)

7. Select Red or Amber Impact Scale.
8. Upload a supporting document.
9. Click the Delete/Remove icon.

Expected Result

1. Uploaded document is removed successfully.
2. Upload Document control is available to upload another file.

⸻

TC-17 Verify Replace Uploaded Document

Test Steps

Common Steps (1–6)

7. Select Red or Amber Impact Scale.
8. Upload a supporting document.
9. Remove the uploaded document.
10. Upload another supported document.

Expected Result

1. Previously uploaded document is removed.
2. Newly uploaded document is displayed successfully.

⸻

TC-18 Verify warning popup when Conduct Risk Area is removed in Part 1

Test Steps

Common Steps (1–6)

7. Select Conduct Risk Impact Scale.
8. Upload supporting document.
9. Click Previous.
10. Change Applicability = Yes to No or Conduct Risk = Yes to No.
11. Observe the confirmation popup.

Expected Result

1. Warning popup is displayed.
2. Popup informs the user that downstream data in Part 2 and Mitigation Plan will be removed.

⸻

TC-19 Verify Confirm removes downstream data from Part 2

Test Steps

Common Steps (1–6)

7. Select Conduct Risk Impact Scale.
8. Upload supporting document.
9. Click Previous.
10. Change Applicability = Yes to No or Conduct Risk = Yes to No.
11. Click Confirm.
12. Click Next.

Expected Result

1. Corresponding Conduct Risk Area is removed.
2. Conduct Risk Description is removed.
3. Conduct Risk Impact Scale is removed.
4. Uploaded supporting document is removed.

⸻

TC-20 Verify Cancel retains downstream data

Test Steps

Common Steps (1–6)

7. Select Conduct Risk Impact Scale.
8. Upload supporting document.
9. Click Previous.
10. Change Applicability = Yes to No or Conduct Risk = Yes to No.
11. Click Cancel.
12. Return to Part 2.

Expected Result

1. Previously entered Conduct Risk Area remains.
2. Conduct Risk Description remains.
3. Impact Scale remains.
4. Uploaded document remains.

⸻

TC-21 Verify Save as Draft functionality

Test Steps

Common Steps (1–6)

7. Select Conduct Risk Impact Scale.
8. Upload supporting document where applicable.
9. Click Save as Draft.
10. Reopen the assessment.

Expected Result

1. Assessment is saved successfully.
2. Status remains In Progress.
3. Previously entered values are retained.

⸻

TC-22 Verify Clear All functionality

Test Steps

Common Steps (1–6)

7. Select Conduct Risk Impact Scale.
8. Upload supporting document.
9. Click Clear All.
10. Confirm the action.

Expected Result

1. Selected Impact Scale is cleared.
2. Uploaded document is removed.
3. Auto-populated project details remain unchanged.

⸻

TC-23 Verify Previous button navigation

Test Steps

Common Steps (1–6)

7. Click Previous.

Expected Result

1. User is navigated to Risk Assessment – Part 1.

⸻

TC-24 Verify Next button navigation

Test Steps

Common Steps (1–6)

7. Complete all mandatory fields.
8. Click Next.

Expected Result

1. User is navigated to Mitigation Plan & Commentary stage.

⸻

TC-25 Verify Submit functionality

Test Steps

Common Steps (1–6)

7. Complete all mandatory fields.
8. Click Submit.

Expected Result

1. Assessment is submitted successfully.
2. Assessment moves to the next workflow stage.

⸻

TC-26 Verify mandatory field validations

Test Steps

Common Steps (1–6)

7. Leave one or more mandatory fields blank.
8. Click Next or Submit.

Expected Result

1. Appropriate validation message is displayed.
2. User cannot proceed until all mandatory fields are completed

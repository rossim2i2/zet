# Unlock Protected Excel Sheets Without Password

1. Make a copy of the Excel Document
1. Change extension from `.xlsx` to `.zip`
1. Open new Zip file
1. Navigate to `\xl\worksheets` and open the `xml` document for the
   protected worksheet
1. Search for the word "protect" to navigate to the `sheetProtection`
   tag
1. Copy `xml` document to local drive, open it for editing, and delete the
   tag
1. Delete the `xml` sheet from the zip file and add the changed `xml`
   document
1. Save the zip file and rename it back to `.xlsx`
1. Open the Excel file and the sheet is now unprotected

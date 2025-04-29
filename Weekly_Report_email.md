# Scheduled_Weekly_Report_email_from_Workbook_data

## Summary

This Power Automate flow automates the process of compiling and sending a weekly report to someone. It retrieves data from an Excel file containing lead information, processes the data, and formats it for reporting. The flow is designed to streamline weekly reporting, reduce manual effort, and ensure timely communication using Excel and Power Automate's scheduling capabilities.

## Flow Trigger

- **Recurrence:**
The flow is triggered automatically every scheduled day at scheduled time.


## Flow Actions

- **Initialize Variable:**
Sets up a string variable (`ConcatRows`) to accumulate formatted row data for the report.
- **Get Data from Table:**
Connects to an Excel file stored in a SharePoint or OneDrive location and retrieves rows from a specified table containing leads' weekly report data.
- **Loop Through Each Row:**
Iterates through each row of the Excel table, appending formatted data to the `ConcatRows` variable.
- **Compiling the report:**
Introduce condition to avoid empty cells
- **Sending it via email:**
- Use the data and integrate it with HTML/CSS code to present it well in email. 

## Prerequisites

- **Excel Online (Business):**
Required to access and read the weekly report data from the Excel file.
- **Power Automate:**
For scheduling and running the flow.
- The Excel file must exist at the specified location and contain the relevant table structure for weekly reports.


## Deployment

1. Download the ZIP file from this repository.
2. Go to Power Automate > My Flows > Import.
3. Upload the ZIP file and configure connections for Excel Online (Business).
4. Update the Excel file path and table reference in the flow if needed.
5. Save and enable the flow.

---

<img src="https://r2cdn.perplexity.ai/pplx-full-logo-primary-dark%402x.png" class="logo" width="120"/>

# Leads_Weekly_Report_to_Shashank

## Summary

This Power Automate flow automates the process of compiling and sending a weekly report to Shashank. It retrieves data from an Excel file containing lead information, processes the data, and formats it for reporting. The flow is designed to streamline weekly reporting, reduce manual effort, and ensure timely communication using Excel Online (Business) and Power Automate's scheduling capabilities.

## Flow Trigger

- **Recurrence:**
The flow is triggered automatically every Wednesday at 1:00 PM (GMT).


## Flow Actions

- **Initialize Variable:**
Sets up a string variable (`ConcatRows`) to accumulate formatted row data for the report.
- **Get Data from Table:**
Connects to an Excel file stored in a SharePoint or OneDrive location and retrieves rows from a specified table containing leads' weekly report data.
- **Loop Through Each Row:**
Iterates through each row of the Excel table, appending formatted data to the `ConcatRows` variable.
- **(Further actions may include compiling the report and sending it via email, but these are not fully visible in the provided definition.)**


## Prerequisites

- **Excel Online (Business):**
Required to access and read the weekly report data from the Excel file.
- **Power Automate:**
For scheduling and running the flow.
- The Excel file must exist at the specified location and contain the relevant table structure for leads' weekly reports.


## Deployment

1. Download the ZIP file from this repository.
2. Go to Power Automate > My Flows > Import.
3. Upload the ZIP file and configure connections for Excel Online (Business).
4. Update the Excel file path and table reference in the flow if needed.
5. Save and enable the flow.

---

*If you provide the full flow definition or additional details, I can further elaborate on the actions and outcomes for an even more comprehensive README section.*

<div style="text-align: center">⁂</div>

[^1]: https://ppl-ai-file-upload.s3.amazonaws.com/web/direct-files/attachments/43633442/b791f012-4f1a-4b30-8f6a-dfa46ead8f84/definition.json


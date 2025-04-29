<img src="https://r2cdn.perplexity.ai/pplx-full-logo-primary-dark%402x.png" class="logo" width="120"/>

# Recurrence flow - Reminder to Leads

## Summary

This Power Automate flow automatically sends reminder emails to team leads who have not submitted their weekly report. It leverages Excel Online (Business) to track submission statuses and Office 365 Outlook to deliver high-importance reminders, ensuring timely reporting and improved team accountability.

## Flow Trigger

- Scheduled recurrence: The flow runs every Tuesday and Wednesday at 9:00 AM and 1:00 PM (GMT), once per week.


## Flow Actions

- **Get data from Names Table:**
Retrieves rows from an Excel table containing leads' names, email addresses, and submission statuses, filtering for those marked as "Not Submitted".
- **Loop through each name:**
Iterates over each lead who has not submitted their report.
- **Send reminder email:**
Sends a personalized, high-importance reminder email from the RDK Connectivity Team to each lead, including instructions and a link to the weekly report form.


## Prerequisites

- **Excel Online (Business):** Connection to access and read the leads' status table.
- **Office 365 Outlook:** Connection to send reminder emails.
- The Excel file must exist at the specified location (OneDrive or SharePoint) and contain columns for Name, Mail ID, and Status.


## Deployment

1. Download the ZIP file from this repository.
2. Go to Power Automate > My Flows > Import.
3. Upload the ZIP file and configure connections for Excel Online (Business) and Office 365 Outlook.
4. Update the Excel file path and table reference in the flow if needed.
5. Save and enable the flow.

<div style="text-align: center">⁂</div>

[^1]: https://ppl-ai-file-upload.s3.amazonaws.com/web/direct-files/attachments/43633442/b187eb39-22de-4269-9c46-64d6375e81ea/definition.json


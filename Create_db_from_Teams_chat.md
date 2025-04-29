<img src="https://r2cdn.perplexity.ai/pplx-full-logo-primary-dark%402x.png" class="logo" width="120"/>

# when 'CRECRE' is asked in GroupChat

## Summary

This Power Automate flow listens for the keyword **"CRECRE"** in a specific Microsoft Teams group chat. When the keyword is detected, it extracts relevant message details, processes the content, posts a response in the group chat, and logs specific data into an Excel table. The flow automates keyword-triggered actions for Teams group chats, leveraging Teams and Excel Online (Business) connectors.

## Flow Trigger

- **Teams Group Chat Keyword Trigger:**
The flow is triggered whenever the keyword **"CRECRE"** is mentioned in a designated Microsoft Teams group chat.


## Flow Actions

- **Get Message Details:**
Retrieves the full details of the message where "CRECRE" was mentioned.
- **Find Text Position:**
Searches for the position of the substring `"CRECRE:"` within the message content to locate relevant data.
- **Condition – If Position Found:**
    - **Post Message in Group Chat:**
Posts a response in the same Teams group chat.
    - **Add Row to Excel Table:**
Extracts the "Rpi Label" and "User" from the message content and adds a new row with this data to a specified Excel table.
- **Handles All Matching Messages:**
Applies the above actions to each message containing the keyword.


## Prerequisites

- **Microsoft Teams connection:**
Required for monitoring group chat messages and posting responses.
- **Excel Online (Business) connection:**
Required for logging data into the Excel table.
- **Excel file/table:**
The specified Excel file and table must exist and be accessible to the flow.


## Deployment

1. Download the ZIP file from this repository.
2. Go to Power Automate > My Flows > Import.
3. Upload the ZIP file and configure connections for Microsoft Teams and Excel Online (Business).

<div style="text-align: center">⁂</div>

[^1]: https://ppl-ai-file-upload.s3.amazonaws.com/web/direct-files/attachments/43633442/4795fa7d-f165-4921-a2d6-0e8cce6511d8/definition.json


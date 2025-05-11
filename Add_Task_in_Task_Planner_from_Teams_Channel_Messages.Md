# Power Automate Flow: Add Task in Task Planner from Teams Channel Messages

## Overview

This Power Automate flow is designed to create tasks in Microsoft Planner based on specific messages posted in a channel. When a message containing the trigger word "<trigger word>" followed by a statement and a keyword <say P1 for priority> is posted, the flow extracts the statement to create a task and uses the keyword as the label.

## Flow Details

### Trigger
- **Event:** When a new message is posted in a channel.

### Get the message and its details
- **Action:** Get message details.

### In the Action

1. **Get Message Details**
   - **Expression:** `toLower(outputs('Get_message_details')?['body/body/plainTextContent'])`

2. **Condition: Check if Find Position of Text is Greater Than or Equal to 0**
   - **Expression:** `indexOf(outputs('Get_message_details')?['body/body/plainTextContent'], '<keyword>') >= 0`

3. **Compose: Extract the Task Statement**
   - **Expression:**
     ```plaintext
     trim(
       substring(
         outputs('Get_message_details')?['body/body/plainTextContent'],
         add(indexOf(outputs('Get_message_details')?['body/body/plainTextContent'], '<keyword>'), 7),
         sub(
           indexOf(
             substring(outputs('Get_message_details')?['body/body/plainTextContent'], add(indexOf(outputs('Get_message_details')?['body/body/plainTextContent'], '<keyword>'), 7)),
             ' P'
           ),
           0
         )
       )
     )
     ```

4. **Compose: Extract the Keyword**
   - **Expression:**
     ```plaintext
     substring(
       outputs('Get_message_details')?['body/body/plainTextContent'],
       add(indexOf(outputs('Get_message_details')?['body/body/plainTextContent'], ' P'), 1),
       2
     )
     ```

5. **Create a Task in Planner**
   - **Title:** Output of the first "Compose" action.
   - **Label:** Output of the second "Compose" action.

## Example

### Input Message
```
<keyword> Run tests for tomorrow P1
```

### Output Task
- **Title:** Run tests for tomorrow
- **Label:** P1

## Usage

1. Ensure the flow is connected to the appropriate channel and Planner.
2. Post a message in the channel with the format: `<keyword> <Task Statement> <label>`.
3. The flow will automatically create a task in Planner with the extracted statement and keyword.

## Notes

- The trigger word "<keyword>" must be followed by a space and the task statement.
- The keyword (P1/P2/P3) must be preceded by a space and follow the task statement.

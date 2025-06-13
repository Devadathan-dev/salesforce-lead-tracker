
# Lead Follow-Up Email Flow

This Salesforce Flow automates sending follow-up reminder emails to Lead Owners whose Leads have a `Follow_up__c` date matching today's date.

## Flow Details
- **Trigger:** Scheduled to run daily (e.g., 10 PM)
- **Main Actions:**
  - Find all Leads with `Follow_up__c = TODAY`
  - Loop through each Lead record
  - Retrieve the Lead Owner's email and name
  - Send a follow-up email with Lead details
  - Create an Email_Log__c record capturing email status (SENT or FAILED)
- **Fault Handling:**  
  - Logs email failures with details for troubleshooting.

## Benefits
- Automates timely follow-ups
- Tracks email status via logs
- Supports scalability by handling multiple Leads daily


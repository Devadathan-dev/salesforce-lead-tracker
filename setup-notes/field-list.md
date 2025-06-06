# Lead Tracker Fields

- Lead Source: Website, Referral, Ad, Event, Cold Call
- Status: New- Not Contacted ,Closed - Converted, Closed - Not Converted , New, Contacted, Qualified, Converted, Closed
- Follow-up Date: Date

## ✅ Email Flow Test - 6 June 2025

- Flow: Sends a follow-up email to Leads where `Follow_up__c = Today`
- Fields used: Email, Id, Name
- Email Format:
  - **Subject**: "Follow-up Reminder: <Lead Name>"
  - **Body**: "Hello, this is a reminder to follow up with lead <Lead Name>."
- Test Lead: *Saul Goodman*
- Test Email Received: ✅ Yes
- Error Fixes Applied:
  - Removed `logEmailOnSend = true` to prevent `bad Id` and `unsupported whatId` errors
- Flow Debug: Successful (6 June 2025, 22:15

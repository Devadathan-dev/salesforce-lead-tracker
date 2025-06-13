# Salesforce Lead Tracker - Field List

## Lead Object - Custom Fields Used

| Field Name       | API Name         | Type         | Description                                                      |
|------------------|------------------|--------------|------------------------------------------------------------------|
| Lead Source      | LeadSource       | Picklist     | Source of the lead (Website, Referral, Ad, Event, Cold Call)     |
| Status           | Status           | Picklist     | Lead status (New, Contacted, Qualified, Converted, Closed, etc.) |
| Follow-up Date   | Follow_up__c     | Date         | Date for follow-up reminders                                     |

---

## Email_Log__c Object - Custom Fields

| Field Name       | API Name          | Type            | Description                       |
|------------------|-------------------|-----------------|-----------------------------------|
| Email Sent To    | Email_Sent_To__c  | Email           | Recipient email address           |
| Email Subject    | Email_Subject__c  | Text            | Subject of the email              |
| Email Body       | Email_Body__c     | Long Text Area  | Full body content of the email    |
| Lead             | Lead__c           | Lookup (Lead)   | Related Lead record               |
| Sent By          | Sent_By__c        | Lookup (User)   | User who sent the email           |
| Sent On          | Sent_On__c        | DateTime        | Date and time email was sent      |
| Status           | Status__c         | Picklist        | Email send status (SENT, FAILED)  |

---

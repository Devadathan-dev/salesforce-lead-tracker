# 📩 Salesforce Lead Tracker Project

This project sends automatic follow-up emails to Lead Owners whose Leads have a `Follow_up__c` date matching **today**.


## 🧾 Lead Tracker Fields

**Lead Source Options:**
- Website
- Referral
- Ad
- Event
- Cold Call

**Status Values:**
- New - Not Contacted
- New
- Contacted
- Qualified
- Converted
- Closed - Converted
- Closed - Not Converted
- Closed

**Custom Field:**
- `Follow_up__c`: Follow-up Date (Date)

## ✅ Email Flow Test - 6 June 2025

- **Flow Logic:**  
  Sends a follow-up email to all Leads where `Follow_up__c = TODAY`.

- **Fields Used in Flow:**  
  `Email`, `Id`, `Name`

- **Email Format:**

  **Subject:**  
  `Follow-up Needed - {!Loop_Through_Leads.Company}`

  **Body:**
Hello {!Get_Lead_Owner.Name},

This is a friendly reminder to follow up with the lead you were assigned on {!Loop_Through_Leads.Follow_up__c}.

📌 Lead Details:

Name: {!Loop_Through_Leads.Name}

Email: {!Loop_Through_Leads.Email}

Company: {!Loop_Through_Leads.Company}

Status: {!Loop_Through_Leads.Status}

Please take the appropriate action today.

Best regards,
Your Salesforce Automation Bot 🤖


- **Test Lead Used:** Saul Goodman  
- **Test Email Received:** ✅ Yes  
- **Flow Debug Status:** ✅ Successful (6 June 2025, 22:15)

- **Fixes Applied:**
- Removed `logEmailOnSend = true` to prevent invalid `whatId` errors

## ✅ Email Flow Update - 9 June 2025

- **Enhancements Made:**
- Email now sent to the **Lead Owner** (retrieved via `OwnerId`)
- Salutation now uses the **Owner’s Name**
- Confirmed flow works with real user records

- **Email Content Includes:**
- Owner’s Name
- Lead Name, Email, Company, and Status
- Follow-up Date (`Follow_up__c`)

- **Email Subject:**  
`Follow-up Needed - {!Loop_Through_Leads.Company}`

- **Email Received:** ✅ Yes (Verified on real record: george Smith)

- **Fixes Applied:**
- Corrected `OwnerId` usage in flow Get Records
- Removed duplicate "Subject:" prefix

---




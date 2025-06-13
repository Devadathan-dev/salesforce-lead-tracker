# 📩 Salesforce Lead Tracker

A Salesforce automation project that tracks and manages Leads, and sends follow-up email reminders to Lead Owners when the `Follow_up__c` date matches today.

## 🛠️ Built With

- **Salesforce Flows** (Visual Automation)
- **Lightning App Builder**
- **Custom Fields**
- 🧼 100% Declarative (No Apex or SOQL)

---

## ✨ Features

- ✅ **Follow-up Reminder Flow**  
  Automatically sends follow-up emails to Lead Owners for leads where `Follow_up__c = TODAY`.

- ✅ **Email Log Creation**  
  Flow creates a record in the custom object `Email_Log__c` to track sent emails.

- ✅ **Custom Field**  
  `Follow_up__c`: A custom Date field on the Lead object.

- ✅ **Tested with Real Data**  
  Verified email delivery and logging with actual test Leads and real user Owners.

---

## 📂 Flow Details

- Flow File: [`WORKING_FLOW.flow-meta.xml`](flows/WORKING_FLOW.flow-meta.xml)
- Screenshots in the `flows/` folder:
  - `flow.png`, `flow-zoom1.png`, `log-email-assignment.png`, `email-log-record.png`, etc.

---

## 🧪 Test Summary

- 🧪 **Test Dates:** 6 June & 9 June 2025
- ✅ **Email Sent To:**
  - Test Lead: *Saul Goodman*
  - Real Lead Owner: *Devadathan Namboothiri P*
- 🛠️ **Fixes Made:**
  - Corrected Owner lookup using `OwnerId`
  - Removed `logEmailOnSend = true` (which caused invalid `whatId` errors)
  - Logging enhancement using `Email_Log__c`
  - Created variable 'LOG' to store essential fields
---

## 📝 Field & Setup Notes

- Field documentation: [`field-list.md`](setup-notes/field-list.md)
- Logic:  
  Flow finds all Leads where:
  Follow_up__c == Today
  and sends follow-up email to Lead Owner with all details.

---

## 👤 Author

**Devadathan Namboothiri P**  
Salesforce Developer & Trailblazer  
[GitHub Profile](https://github.com/Devadathan-dev)

---
## 🎓 Key Salesforce Badges

[![Apex Basics & Database](https://badges.salesforce.com/apex-basics-database.svg)](https://trailhead.salesforce.com/en/content/learn/modules/apex_database)

[![Flow Builder Basics](https://badges.salesforce.com/flow-builder-basics.svg)](https://trailhead.salesforce.com/en/content/learn/modules/flow-builder-basics)

[![Data Modeling](https://badges.salesforce.com/data-modeling.svg)](https://trailhead.salesforce.com/en/content/learn/modules/data-modeling)

[![Lightning Experience Customization](https://badges.salesforce.com/lightning-experience-customization.svg)](https://trailhead.salesforce.com/en/content/learn/modules/lightning_experience_customization)

[![Platform Development Basics](https://badges.salesforce.com/platform-development-basics.svg)](https://trailhead.salesforce.com/en/content/learn/modules/platform_dev_basics)




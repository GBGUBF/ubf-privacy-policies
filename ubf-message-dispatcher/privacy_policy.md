# Privacy Policy - UBF Utskick

**Last updated:** December 9, 2025

## Overview

UBF Utskick is a Chrome extension developed for Utbildningsförvaltningen Göteborgs Stad (UBF) to send communication messages via SMS and email to students and guardians.

## What data is collected?

The extension collects the following information:

**From Google Workspace:**
- Names and email addresses of students in selected classes/groups
- Class names and school names

**From SS12000 API (planned):**
- Private email addresses for guardians
- Private mobile phone numbers for SMS messaging

## How is the data used?

Data is used **only** for:
- Displaying recipient lists in the extension
- Sending SMS messages to specified recipients
- Sending email messages to specified recipients
- Saving message templates for reuse

## Where is data stored?

- **Temporary storage:** Data is only stored temporarily in the browser's memory during use
- **Local cache:** Authentication status is cached locally (1 hour)
- **Firestore:** Student data and templates are stored in Firebase Firestore
- **Cloud Functions:** API keys are stored securely in Google Secret Manager

## Third parties

The extension communicates with the following third-party services:

| Service | Purpose | Data sent |
|---------|---------|-----------|
| **Infobip** | SMS delivery | Phone numbers, message text |
| **Gmail API** | Email delivery | Email addresses, subject, message |
| **SS12000 API** | Contact information | Student identifiers |

All communication is encrypted via HTTPS.

## Permissions

The extension requests the following permissions:
- **identity:** To authenticate with Google Workspace and UBF Auth API
- **storage:** For local caching of authentication status
- **sidePanel:** To display the interface in the Chrome side panel

## Message logging

- Sent SMS messages are **not** logged in the extension
- Email messages are saved in the user's "Sent" folder in Gmail
- No message logs are stored on our servers

## Data retention

- Student data is synchronized daily and old records are removed
- Authentication cache expires after 1 hour
- Message templates are stored until manually deleted

## Contact

For questions about this privacy policy, contact Utbildningsförvaltningen Göteborgs Stad.

## Changes

We may update this policy as needed. Changes will be published on this page.

---

**Developer:** Utbildningsförvaltningen Göteborgs Stad  
**Support:** [ServiceNow - UBF](https://intraservice.service-now.com/ubf)

# Privacy Policy - UBF Adminverktyg

**Last updated:** February 10, 2026

## Overview

UBF Adminverktyg is a Chrome extension developed for Utbildningsförvaltningen Göteborgs Stad (UBF) to provide IT administrators with tools for user management, two-factor authentication (2FA) handling and school organisation overview.

## What data is collected?

The extension collects the following information:

**From Google Workspace:**
- Names and email addresses of users
- Group memberships and statistics (student/staff counts)

**From MMD005/MMD006 API:**
- Staff information: name, email, mobile, position, manager
- Student information: name, class, school
- Organisation and school unit data: names, addresses, leadership

## How is the data used?

Data is used **only** for:
- Searching and displaying user information for IT support purposes
- Managing two-factor authentication (2FA) for users
- Displaying organisation and school unit overviews
- Sending 2FA setup instructions via email

## Where is data stored?

- **Session storage:** Organisation data is cached in Chrome's session storage (cleared when browser closes)
- **Firestore:** Organisation data is cached in Firebase Firestore (synced daily)
- **Cloud Functions:** API keys are stored securely in Google Secret Manager
- **No personal data is persisted** in the extension's local storage

## Third parties

The extension communicates with the following third-party services:

| Service | Purpose | Data sent |
|---------|---------|-----------|
| **Google Admin Directory API** | User management, 2FA status | User identifiers |
| **MMD005 API** | Staff lookup | Search queries |
| **MMD006 API** | Student and organisation lookup | Search queries, organisation IDs |
| **Gmail API** | Sending 2FA instructions | Email addresses, instruction text |

All communication is encrypted via HTTPS.

## Permissions

The extension requests the following permissions:
- **identity:** To authenticate with Google Workspace
- **storage:** For caching authentication status and organisation data
- **sidePanel:** To display the interface in the Chrome side panel
- **contextMenus:** To add a right-click search option for quick user lookup

## Data retention

- Session cache is cleared when the browser is closed
- Firestore organisation cache is refreshed daily at 05:00
- No user search queries or results are logged or stored
- 2FA moved-user records are stored until the user activates 2FA

## Access control

- The extension is restricted to authorized IT administrators
- Authentication is handled via Google Workspace OAuth2
- Access is controlled through Google Groups membership

## Contact

For questions about this privacy policy, contact Utbildningsförvaltningen Göteborgs Stad.

## Changes

We may update this policy as needed. Changes will be published on this page.

---

**Developer:** Utbildningsförvaltningen Göteborgs Stad  
**Support:** [ServiceNow - UBF](https://intraservice.service-now.com/ubf)

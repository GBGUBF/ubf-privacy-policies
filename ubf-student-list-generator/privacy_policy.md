# Privacy Policy - UBF Klasslistor

**Last updated:** December 9, 2025

## Overview

UBF Klasslistor is a Chrome extension developed for Utbildningsförvaltningen Göteborgs Stad (UBF) to generate student lists from Google Workspace.

## What data is collected?

The extension collects the following information:

**From Google Workspace:**
- Names and email addresses of students and teachers in selected classes/groups
- Class names and school names

## How is the data used?

Data is used **only** for:
- Displaying student lists in the extension
- Exporting lists to PDF (with or without QR codes)
- Exporting lists to Google Docs
- Exporting lists to Google Sheets
- Exporting lists to CSV

## Where is data stored?

- **Temporary storage:** Data is only stored temporarily in the browser's memory during use
- **Local cache:** Authentication status is cached locally (1 hour)
- **Firestore:** Student data is cached in Firebase Firestore for faster access

## Third parties

The extension communicates with the following services:

| Service | Purpose | Data sent |
|---------|---------|-----------|
| **Google Docs API** | Export to documents | Document content |
| **Google Sheets API** | Export to spreadsheets | Spreadsheet content |
| **Google Drive API** | Save exported files | File metadata |

All communication is encrypted via HTTPS.

## Permissions

The extension requests the following permissions:
- **identity:** To authenticate with Google Workspace and UBF Auth API
- **storage:** For local caching of authentication status
- **sidePanel:** To display the interface in the Chrome side panel
- **drive.file:** To create exported files in Google Drive
- **documents:** To create Google Docs exports
- **spreadsheets:** To create Google Sheets exports

## Data retention

- Student data is synchronized daily and old records are removed
- Authentication cache expires after 1 hour
- Exported files are stored in the user's Google Drive and managed by the user

## Your rights

As a user you have the right to:
- Request information about what data is processed
- Request correction of incorrect data
- Request deletion of data (contact system administrator)

## Contact

For questions about this privacy policy, contact Utbildningsförvaltningen Göteborgs Stad.

## Changes

We may update this policy as needed. Changes will be published on this page.

---

**Developer:** Utbildningsförvaltningen Göteborgs Stad  
**Support:** [ServiceNow - UBF](https://intraservice.service-now.com/ubf)

# Privacy Policy - Alma (UBF Chatbot)

**Last updated:** April 24, 2026

## Overview

Alma is an AI assistant developed for Utbildningsförvaltningen Göteborgs Stad (UBF) to help students, teachers and staff with information about schools, meals, schedules, grades, staff contacts, IT support and general guidance within the organisation. Alma is available as a Google Workspace Add-on in Google Chat.

## What data is collected?

The application collects the following information:

**From Google Workspace (Google Chat):**
- User's email address (for authentication and personalisation)
- User's name (for display and context)
- Message content sent to Alma (questions and conversation history)

**From internal UBF APIs (on behalf of the authenticated user):**
- Staff information: name, email, phone, position, school (MMD005)
- Student information: name, class, school (MMD006)
- Organisation and school unit data (MMD006)
- School meal menus and schedules

## How is the data used?

Data is used **only** for:
- Authenticating the user via Google Workspace
- Generating contextual AI responses based on the user's role (student, teacher, staff)
- Looking up requested information (e.g. meals, schedules, contact details)
- Logging conversations for quality assurance and debugging (see Data retention)
- Sending emails on behalf of the user (e.g. 2FA instructions) only after explicit confirmation

Data is **never** used for:
- Training external AI models
- Advertising or marketing
- Sharing with parties outside UBF's approved service providers

## Where is data stored?

- **Firestore (chatLogs):** Conversation logs are stored in Google Firestore within the `ubf-chatbot` GCP project for quality assurance and debugging
- **Cloud Run:** Messages are processed in-memory by Cloud Run services (`gchat-bridge`, `chatbot-api`) and not persisted outside Firestore
- **Google Cloud Secret Manager:** API keys and credentials are stored securely
- **No personal data is persisted** in the Google Chat client beyond Google's own message history

All data is stored within the European Union (region `europe-north1`, Finland).

## Third parties

The application communicates with the following third-party services:

| Service | Purpose | Data sent |
|---------|---------|-----------|
| **Google Chat API** | Message delivery | Message content, user identifiers |
| **Google Identity / OAuth2** | Authentication | JWT tokens |
| **Google Gemini (Vertex AI)** | AI response generation | Message content, conversation context |
| **MMD005 API** | Staff lookup | Search queries |
| **MMD006 API** | Student and organisation lookup | Search queries, organisation IDs |
| **Gmail API** | Sending emails on behalf of user | Email addresses, email content |
| **Firestore** | Conversation logging | Message content, user identifiers |

All communication is encrypted via HTTPS.

## Permissions and scopes

The Workspace Add-on requests the following OAuth scopes:
- **`chat.bot`:** To receive and respond to messages in Google Chat
- **`userinfo.email`:** To identify the user
- **`userinfo.profile`:** To personalise responses with the user's name

## Data retention

- Conversation logs are retained in Firestore for up to 90 days for quality assurance
- No conversation data is retained longer than necessary for the service
- Users may request deletion of their conversation history by contacting UBF support

## Access control

- Alma is restricted to authorised users within `skola.goteborg.se` and `educ.goteborg.se` domains
- Authentication is handled via Google Workspace OAuth2 with JWT verification
- Role-based access (student, teacher, staff) determines which information Alma can retrieve
- All backend services are protected by Cloud Run IAM invoker checks

## AI disclosure

Alma uses generative AI (Google Gemini) to produce responses. Responses are generated based on the user's question and context retrieved from UBF's internal systems. AI-generated responses may occasionally contain errors — users are encouraged to verify critical information through official channels.

## Contact

For questions about this privacy policy or to request data deletion, contact Utbildningsförvaltningen Göteborgs Stad.

## Changes

We may update this policy as needed. Changes will be published on this page.

---

**Developer:** Utbildningsförvaltningen Göteborgs Stad  
**Support:** [ServiceNow - UBF](https://intraservice.service-now.com/ubf)

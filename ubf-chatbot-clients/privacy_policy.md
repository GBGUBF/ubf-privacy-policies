# Privacy Policy - Alma (UBF Chatbot)

**Last updated:** May 12, 2026

## Overview

Alma is an AI assistant developed for Utbildningsförvaltningen Göteborgs Stad (UBF) to help students, teachers and staff with information about schools, meals, schedules, grades, staff contacts, IT support and general guidance within the organisation.

Alma is available through the following clients:

- **Chrome Extension** (side panel) — [Chrome Web Store](https://chrome.google.com/webstore/detail/jhmphpbnklhhmkjignffpljfngikakea)
- **Google Chat** — Google Workspace Add-on

All clients connect to the same backend (`ubf-chatbot`) and are governed by this single privacy policy.

## What data is collected?

The application collects the following information:

**From the Chrome Extension:**
- User's email address and profile (via Google OAuth through UBF Auth API)
- User's display name and profile photo (for display in the chat interface)
- Message content sent to Alma (questions and conversation history)
- Theme preference (light/dark mode, stored locally in Chrome storage)

**From Google Chat (Workspace Add-on):**
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
- Authenticating the user via Google OAuth (Chrome Extension) or Google Workspace (Google Chat)
- Generating contextual AI responses based on the user's role (student, teacher, staff)
- Looking up requested information (e.g. meals, schedules, contact details)
- Logging conversations for quality assurance and debugging (see Data retention)
- Sending emails on behalf of the user (e.g. 2FA instructions) only after explicit confirmation

Data is **never** used for:
- Training external AI models
- Advertising or marketing
- Sharing with parties outside UBF's approved service providers
- Tracking browsing activity or web history

## Where is data stored?

- **Firestore (chatLogs):** Conversation logs are stored in Google Firestore within the `ubf-chatbot` GCP project for quality assurance and debugging
- **Cloud Run:** Messages are processed in-memory by Cloud Run services (`gchat-bridge`, `chatbot-api`) and not persisted outside Firestore
- **Chrome local storage:** Theme preference only (no personal data)
- **Google Cloud Secret Manager:** API keys and credentials are stored securely
- **No personal data is persisted** in the Chrome Extension or Google Chat client beyond what is described above

All data is stored within the European Union (region `europe-north1`, Finland).

## Third parties

The application communicates with the following third-party services:

| Service | Purpose | Data sent | Used by |
|---------|---------|-----------|---------|
| **UBF Auth API** | Authentication (Chrome Extension) | OAuth tokens, email | Extension |
| **Google Chat API** | Message delivery | Message content, user identifiers | Google Chat |
| **Google Identity / OAuth2** | Authentication | JWT tokens, OAuth tokens | Both |
| **Google Gemini (Vertex AI)** | AI response generation | Message content, conversation context | Both |
| **MMD005 API** | Staff lookup | Search queries | Both |
| **MMD006 API** | Student and organisation lookup | Search queries, organisation IDs | Both |
| **Gmail API** | Sending emails on behalf of user | Email addresses, email content | Both |
| **Firestore** | Conversation logging | Message content, user identifiers | Both |

All communication is encrypted via HTTPS.

## Permissions

### Chrome Extension

The extension requests the following permissions:
- **`identity`:** To authenticate via Google OAuth
- **`storage`:** To save theme preference (light/dark mode)
- **`sidePanel`:** To display the chat interface in Chrome's side panel
- **Host permissions:** To communicate with `ubf-chatbot` API and `ubf-auth-api`

The extension does **not** request:
- Access to browsing history
- Access to page content or tabs
- Access to bookmarks, downloads, or other browser data

### Google Chat (Workspace Add-on)

The add-on requests the following OAuth scopes:
- **`chat.bot`:** To receive and respond to messages in Google Chat
- **`userinfo.email`:** To identify the user
- **`userinfo.profile`:** To personalise responses with the user's name

## Data retention

- Conversation logs are retained in Firestore for up to 90 days for quality assurance
- No conversation data is retained longer than necessary for the service
- Users may request deletion of their conversation history by contacting UBF support
- Chrome local storage (theme preference) can be cleared by uninstalling the extension

## Access control

- Alma is restricted to authorised users within `skola.goteborg.se` and `educ.goteborg.se` domains
- Chrome Extension: Authentication is handled via UBF Auth API with Google OAuth
- Google Chat: Authentication is handled via Google Workspace OAuth2 with JWT verification
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

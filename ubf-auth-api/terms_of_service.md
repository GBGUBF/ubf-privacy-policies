# Terms of Service - UBF Auth API

**Last updated:** February 9, 2026

## Overview

UBF Auth API is a centralized authentication and authorization service operated by Utbildningsförvaltningen Göteborgs Stad (UBF). These terms govern the use of the service.

## Intended use

This service is intended **exclusively** for:
- Employees of Utbildningsförvaltningen Göteborgs Stad
- Users with a valid Google Workspace account under `skola.goteborg.se` or `educ.goteborg.se`
- Internal Chrome extensions and tools developed by UBF

## Access requirements

To use this service, you must:
- Have an active Google Workspace account provided by Göteborgs Stad
- Be a member of the relevant Google Groups for your role and school
- Use an approved UBF Chrome extension or tool

## User responsibilities

Users agree to:
- Not share authentication tokens or API keys with unauthorized parties
- Not attempt to access permissions or data beyond their authorized scope
- Report any suspected security incidents to IT support immediately

## Service availability

- The service is hosted on Google Cloud Run and is available 24/7
- Planned maintenance will be communicated in advance when possible
- No uptime guarantees are provided for this internal service

## Permissions and access

- Access permissions are determined by Google Groups membership
- Admin permissions are granted per service based on designated admin groups
- School-level access is determined by `allpersonal` group membership
- Permissions are cached and synchronized automatically every 4 hours

## Limitation of liability

This service is provided "as is" for internal use within Utbildningsförvaltningen. The development team is not liable for:
- Service interruptions or downtime
- Data loss due to system failures
- Incorrect permissions due to Google Groups misconfiguration

## Changes to these terms

We may update these terms as needed. Changes will be published on this page. Continued use of the service constitutes acceptance of updated terms.

## Contact

For questions about these terms, contact Utbildningsförvaltningen Göteborgs Stad.

---

**Developer:** Utbildningsförvaltningen Göteborgs Stad  
**Support:** [ServiceNow - UBF](https://intraservice.service-now.com/ubf)

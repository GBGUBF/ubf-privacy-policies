# UBF Privacy Policies

Detta repo innehåller integritetspolicys, användarvillkor och supportsidor för GBGUBF:s olika projekt och tillägg.

Sidorna publiceras automatiskt via GitHub Pages på: https://gbgubf.github.io/ubf-privacy-policies/

## Tillgängliga dokument

| Projekt | Privacy Policy | Terms of Service | Support |
|---------|---------------|-----------------|---------|
| Alma (UBF Chatbot) | [Privacy Policy](ubf-chatbot-clients/privacy_policy.md) | [Terms of Service](ubf-chatbot-clients/terms_of_service.md) | [Support](ubf-chatbot-clients/support.md) |
| UBF Adminverktyg | [Privacy Policy](ubf-admin-console/privacy_policy.md) | — | — |
| UBF Klasslistor | [Privacy Policy](ubf-student-list-generator/privacy_policy.md) | — | — |
| UBF Auth API | [Privacy Policy](ubf-auth-api/privacy_policy.md) | [Terms of Service](ubf-auth-api/terms_of_service.md) | — |

## Hur man lägger till en ny policy

1. Skapa en ny mapp med projektets namn
2. Lägg till en `privacy_policy.md`-fil i mappen
3. Uppdatera tabellen ovan
4. Länka policyn i respektive projekt/tillägg

## Struktur

```
ubf-privacy-policies/
├── README.md
├── CHANGELOG.md
├── ubf-chatbot-clients/
│   ├── privacy_policy.md
│   ├── terms_of_service.md
│   └── support.md
├── ubf-admin-console/
│   └── privacy_policy.md
├── ubf-auth-api/
│   ├── privacy_policy.md
│   └── terms_of_service.md
└── [framtida-projekt]/
    └── privacy_policy.md
```

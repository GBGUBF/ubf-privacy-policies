# Integritetspolicy för UBF Klasslistor

**Senast uppdaterad:** 5 december 2025

## Översikt

UBF Klasslistor är ett Chrome-tillägg utvecklat av Utbildningsförvaltningen Göteborgs Stad för intern användning. Tillägget hjälper personal att generera klasslistor från Google Workspace.

## Vilka uppgifter samlas in?

### Uppgifter som hämtas (men inte lagras av tillägget):
- **Namn** på elever och lärare från Google Workspace
- **E-postadresser** för elever och lärare
- **Klassgruppsinformation** från Google Workspace

### Uppgifter som lagras lokalt:
- **Autentiseringscache** (e-post och behörigheter) i Chrome Storage (max 1 timme)

## Hur används uppgifterna?

Uppgifterna används endast för att:
1. Visa klasslistor för användaren
2. Exportera klasslistor till PDF, Google Dokument eller Google Kalkylark
3. Verifiera användarens behörighet att se specifika skolor

## Datadelning med tredje part

**Vi delar inte personuppgifter med tredje part.**

All kommunikation sker inom Göteborgs Stads egna system:
- Google Workspace (organisationens befintliga system)
- Firebase/Firestore (cachad data för snabbare åtkomst)
- UBF Auth API (intern behörighetskontroll)

## Datalagring

| Data | Lagringsplats | Lagringstid |
|------|---------------|-------------|
| Elevdata (cache) | Google Cloud Firestore | Synkas dagligen, gamla poster tas bort |
| Auth-cache | Chrome lokal lagring | Max 1 timme |
| Exporterade filer | Användarens Google Drive | Hanteras av användaren |

## Säkerhet

- All kommunikation sker över HTTPS (TLS 1.3)
- OAuth 2.0 används för autentisering
- Tillägget kan endast läsa data, inte modifiera
- Endast behörig personal inom Göteborgs Stad kan använda tillägget

## Dina rättigheter

Som användare har du rätt att:
- Begära information om vilka uppgifter som behandlas
- Begära rättelse av felaktiga uppgifter
- Begära radering av uppgifter (kontakta systemadministratör)

## Ändringar i policyn

Vid väsentliga ändringar uppdateras denna policy och datumet ovan ändras.

## Kontakt

**Systemägare:** Utbildningsförvaltningen Göteborgs Stad  
**Support:** [ServiceNow - UBF](https://intraservice.service-now.com/ubf)  
**E-post:** daniel.dichter.heineman@educ.goteborg.se

# 06 — Security-architectuur, Privacy/AVG & EU AI Act

> Geen juridisch advies. Laat de juridische conclusies vóór commerciële lancering toetsen door een privacy-/IT-jurist.

## Deel A — Security-architectuur

### A1. Securitymodel

| Domein | Maatregel | Fase |
|---|---|---|
| Encryptie in transit | TLS 1.2+ (bij voorkeur 1.3), HSTS, alleen moderne cipher suites; interne verkeer via private endpoints | MVP |
| Encryptie at rest | AES-256 (platform-managed) voor DB, blob, backups; gevoelige velden (gezondheid) extra applicatie-encryptie (envelope encryption, Key Vault) | MVP |
| Customer-managed keys | CMK per enterprise-tenant (Key Vault, BYOK) | 6 |
| Authenticatie | OIDC/SAML SSO, MFA verplicht voor beheerders en standaard voor alle kantoorgebruikers; passkeys; veld-login met device-binding + pincode | MVP |
| Microsoft Entra ID | SSO, conditional access respecteren (klant-tenant), groepen → rollen mapping | MVP/3 |
| SCIM | Automatische provisioning/deprovisioning | 3–4 |
| Autorisatie | RBAC + scope/ABAC (zie [05](05-technische-architectuur.md)), least privilege, RLS | MVP |
| Tenant-isolatie | RLS + geautomatiseerde isolatietests + periodieke pentest specifiek op cross-tenant | MVP |
| Audit logs | Onveranderlijk (append-only, hash-chain) voor: login, rechtenwijziging, export, verwijdering, AI-acties, record-wijzigingen (wie/wat/wanneer/oud/nieuw); klant-exporteerbaar; SIEM-feed enterprise | MVP (basis), 4 (SIEM) |
| Secrets | Key Vault, managed identities, geen secrets in code/CI-logs, secret scanning in repo | MVP |
| Logging & monitoring | Centrale logs zonder persoonsgegevens in plain text; security-alerts (brute force, anomalie exports) | MVP |
| Netwerk | WAF, DDoS-basisbescherming, private endpoints voor DB/storage, geen publieke DB | MVP |
| Bestanden | Malware-scanning bij upload, content-type-validatie, kortlevende SAS-URL's | MVP |
| Secure SDLC | Threat modeling per module, code review (4-ogen), SAST (Semgrep/CodeQL), SCA (Dependabot/Renovate), container scanning, DAST op staging, SBOM | MVP |
| Vulnerability management | SLA's: kritiek 7 dagen, hoog 30 dagen; responsible disclosure-beleid (security.txt) | MVP |
| Pentest | Extern vóór commerciële launch, daarna jaarlijks + bij grote releases; rapport-samenvatting deelbaar met klanten | 3 |
| Incident response | IR-plan, runbooks, on-call, 24/72-uursmelding (AVG-meldplicht klant als verwerkingsverantwoordelijke, NIS2-ketenverplichtingen), jaarlijkse tabletop | MVP (plan), 3 (oefening) |
| Business continuity | Backups, DR-test 2×/jaar, RPO/RTO zie [05](05-technische-architectuur.md) | 3 |
| Personeel | Screening (VOG), security awareness, offboarding-checklist, MFA overal, device management | MVP |

### A2. Certificering: SOC 2 vs. ISO 27001

| | **ISO 27001** | SOC 2 Type II |
|---|---|---|
| Relevantie NL/EU-klanten | **Zeer hoog** (wordt gevraagd in aanbestedingen; past bij IMS-verhaal: "wij leven onze eigen normen") | Laag–midden (vooral US-klanten) |
| Kosten eerste jaar | € 30–60k (consultancy/tooling € 15–30k, certificatie-audit € 10–20k, interne tijd) | $ 40–80k |
| Doorlooptijd | 6–12 maanden | 9–15 maanden (incl. observatieperiode) |
| **Advies** | **Ja — start ISMS in fase 2, certificeren in fase 4 (maand 15–24).** Uitbreiden met ISO 42001 (AI-managementsysteem) als marketing- en AI Act-ondersteuning in fase 5 | Alleen bij US-expansie |

Kanttekening: een IMS-softwarebedrijf zónder eigen ISO 27001 verliest geloofwaardigheid bij QHSE-kopers. Gebruik het eigen platform (ISO 27001-normkader) als **dogfooding** en showcase.

### A3. NIS2 / Cyberbeveiligingswet

Veel klanten (energie, transport, afval, maakindustrie, digitale dienstverleners) vallen onder NIS2 en moeten **ketenrisico's** beheersen. IMS Nexus wordt dan een geëvalueerde leverancier. Zorg voor: security-whitepaper, ingevulde standaardvragenlijsten (bijv. CAIQ/SIG-lite), DPA + securitybijlage, pentest-samenvatting.

## Deel B — Privacy / AVG

### B1. Rollen

| Verwerking | IMS Nexus-rol | Klantrol |
|---|---|---|
| Klantdata in het platform (medewerkers, incidenten, documenten) | **Verwerker** (art. 28) | Verwerkingsverantwoordelijke |
| Accountbeheer, facturatie, support-contact, marketing | Verwerkingsverantwoordelijke | — |
| Productanalytics (gebruiksstatistieken) | Verantwoordelijke voor geaggregeerde/pseudonieme analytics — beperk en documenteer, of behandel als verwerker-instructie | — |
| Gebruik van klantdata voor verbetering AI (evaluatiesets) | **Alleen met expliciete contractuele toestemming**, geanonimiseerd; anders word je (gezamenlijk) verantwoordelijke → vermijden | — |

### B2. Contractuele set

- **Verwerkersovereenkomst (DPA)** conform art. 28, bij voorkeur gebaseerd op de **EU Standard Contractual Clauses voor art. 28** of het NL-model (Data Pro Code).
- **Sub-processorlijst** (publiek, met 30 dagen notificatie bij wijziging en bezwaarrecht): cloud (Azure EU), LLM-endpoints (EU), e-mail, auth-provider, monitoring, support-tool.
- **Securitybijlage** (TOMs).
- **SLA** en **exit-clausule** (export binnen 30 dagen, verwijdering binnen 30–90 dagen inclusief backups-rotatie).

### B3. Specifieke aandachtspunten

| Onderwerp | Risico | Maatregel in product |
|---|---|---|
| **Gezondheidsgegevens** (letsel, verzuim na ongeval) = bijzondere categorie (art. 9) | Hoog | Aparte velden met strengere autorisatie, encryptie op veldniveau, standaard níet naar AI, retentie apart instelbaar, minimaliseren (vaak volstaat "letsel: ja/nee + type") |
| Strafrechtelijke gegevens (art. 10) — bijv. diefstal, geweld | Midden | Waarschuwing in formulieren, vrije-tekstscan door AI op gevoelige gegevens (lokaal signaal) |
| **Werknemersdata / OR** | Hoog | NL: systeem dat gedrag/prestaties kan volgen valt onder **instemmingsrecht OR (WOR art. 27 lid 1 sub l)**. Lever een **OR-informatiepakket** en configuratie "geen persoonsgerichte rapportages" |
| Anoniem melden | Midden | Echte anonimiteit (geen user-ID opslaan, metadata strippen van foto's — EXIF/GPS) |
| Foto's | Midden | EXIF-strip, gezichtsvervaging optioneel (fase 4) |
| Retentie | Midden | Configureerbaar per recordtype; standaardsuggesties (bijv. incidenten 5–10 jaar i.v.m. aansprakelijkheid/Arbowet-registratie, NB: valideren) |
| Verwijdering | Midden | Soft delete → hard delete na termijn; cryptografische verwijdering voor backups via rotatie |
| Export / dataportabiliteit | Laag | Volledige tenant-export (JSON + CSV + bestanden), per persoon export voor DSAR |
| **DSAR** (inzageverzoeken) | Midden | Tool: "zoek alle data over persoon X" over records, vrije tekst (met AI-hulp), documenten; klant handelt af |
| **DPIA** | Hoog bij klant | Lever **DPIA-template** per standaardconfiguratie; eigen DPIA voor AI-functies |
| **Internationale doorgifte** | Midden | EU-hosting; vermijd US-sub-processors waar mogelijk; waar onvermijdelijk: EU-US Data Privacy Framework + SCC's + transfer impact assessment. Let op: CLOUD Act-risico bij US-hyperscalers is een terugkerend inkoopargument — bied als optie EU-soevereine hosting (bijv. Azure EU Data Boundary; enterprise: EU-provider) |
| Privacy by design/default | — | Minimale standaardvelden, AI-functies uit tot beheerder activeert (of aan met duidelijke melding — commerciële afweging), korte retentie AI-logs |

## Deel C — EU AI Act

### C1. Tijdlijn (status te verifiëren)

| Datum | Verplichting |
|---|---|
| 1 aug 2024 | Inwerkingtreding |
| 2 feb 2025 | Verboden praktijken (art. 5) + **AI-geletterdheid** (art. 4) — geldt voor jou én je klanten |
| 2 aug 2025 | Verplichtingen voor aanbieders van general-purpose AI-modellen (raakt de modelleveranciers, niet IMS Nexus direct) |
| 2 aug 2026 (oorspronkelijk) | High-risk (bijlage III) en transparantieverplichtingen (art. 50). **Let op:** het *Digital Omnibus*-voorstel (nov. 2025) stelt uitstel van high-risk-verplichtingen voor tot uiterlijk eind 2027 / 2028. Controleer de actuele status. |

### C2. Classificatie van IMS Nexus-functies

| Functie | Classificatie | Verplichtingen | Advies |
|---|---|---|---|
| Documentanalyse, gap-analyse, clausule-mapping | Minimaal risico | AI-geletterdheid; vrijwillige gedragscodes | Bouwen |
| Chat/Q&A, generatieve concepten (rapporten, CAPA) | Beperkt risico (transparantie, art. 50) | Gebruikers informeren dat ze met AI interageren; AI-gegenereerde content markeren | Bouwen, labelen |
| Classificatie van meldingen, risicosuggesties (decision support over situaties) | Minimaal–beperkt | Idem; documenteer human oversight | Bouwen |
| **AI die werknemers beoordeelt, monitort of rangschikt** (veiligheidsgedrag-score, competentiebeoordeling, taakverdeling op basis van persoonlijk gedrag) | **High-risk — bijlage III punt 4 (werkgelegenheid)** | Risicomanagementsysteem, datagovernance, technische documentatie, logging, transparantie, human oversight, nauwkeurigheid/robuustheid, conformiteitsbeoordeling, CE-markering, registratie in EU-databank, post-market monitoring | **Niet bouwen** (kosten € 100k+ en reputatie/OR-risico) |
| AI als veiligheidscomponent van een machine/product (bijlage I) | High-risk | — | Buiten scope (IMS Nexus stuurt geen machines aan) |
| Emotieherkenning op de werkplek | **Verboden** (art. 5) | — | Nooit |

### C3. Rollen onder de AI Act

- IMS Nexus = **aanbieder (provider)** van een AI-systeem (het product met AI-functies), gebouwd op GPAI-modellen van derden.
- Klant = **gebruiksverantwoordelijke (deployer)**: moet AI-geletterdheid borgen en menselijk toezicht inrichten.
- Lever klanten: AI-factsheet per functie (doel, beperkingen, menselijk toezicht, logging), instructies voor gebruik, AI-geletterdheid-microtraining in de app.
- Contractueel: verbied gebruik van de AI-functies voor personeelsbeoordeling (acceptable use policy) om "functiewijziging naar high-risk" door de klant te voorkomen.

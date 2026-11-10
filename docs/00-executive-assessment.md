# 00 — Executive Assessment

> Rolcombinatie: SaaS-strateeg, CTO, AI-architect, security/privacy, ISO-specialist, CFO-adviseur, investeringsanalist.
> Toon: kritisch. Waar het idee zwak is, staat dat er.

---

## 1. Executive summary

**IMS Nexus AI** wil een AI-native platform worden voor geïntegreerde managementsystemen (IMS): kwaliteit, milieu, veiligheid en gezondheid (en later informatiebeveiliging) in één datamodel, met AI die administratieve last wegneemt en audit-readiness verhoogt.

**Oordeel in één zin:** het probleem is echt en er wordt al voor betaald, maar de markt is druk, gefragmenteerd en wordt gedomineerd door gevestigde partijen. IMS Nexus AI wint alleen met een **scherpe wedge** (smalle doelgroep, smal probleem, aantoonbaar sneller audit-ready), niet met een brede "alles-in-één"-belofte.

| Dimensie | Score (1–5) | Toelichting |
|---|---|---|
| Probleemurgentie | 4 | Certificering (ISO/VCA) is een harde commerciële eis voor aanbestedingen en klanten; audits zijn jaarlijks terugkerende pijn. |
| Betalingsbereidheid | 4 | Organisaties betalen nu al consultants (€ 5–25k/jaar) en software (€ 3–60k/jaar). Budget bestaat. |
| Concurrentiedruk | 2 (= zwaar) | Tientallen spelers; enterprise (Intelex, Cority, Enablon, Sphera), mid-market (Quentic, EcoOnline, Ideagen), mobiel (SafetyCulture), NL lokaal (o.a. Zenya). |
| Differentiatiepotentieel | 3 | AI is een *tijdelijke* differentiator: alle spelers voegen in 2025–2027 AI toe. Duurzame moat moet komen uit workflow-lock-in, datamodel, partnerkanaal en verticale content. |
| Technische haalbaarheid | 4 | Bewezen technologie; het moeilijke deel is productdiscipline, niet techniek. |
| Juridische complexiteit | 3 | Gezondheidsdata (incidenten), werknemersdata, OR-instemming, EU AI Act (personeelsbeoordeling = high-risk). Beheersbaar mits by design. |
| Schaalbaarheid internationaal | 3 | Normen zijn internationaal (ISO), maar wet- en regelgeving (Arbo, VCA, milieu) is lokaal. Taal en partnerkanaal per land nodig. |
| Investeerbaarheid | 3 | Venture-case is mogelijk maar niet vanzelfsprekend; realistischer pad is capital-efficient (pre-seed → seed) met optie op VC na bewezen traction. |

---

## 2. Belangrijkste strategische keuzes

Per keuze: **beste optie**, alternatief, en de afweging.

### Keuze 1 — Doelgroep (ICP)

| | Beste optie | Alternatief |
|---|---|---|
| Keuze | **Benelux mid-market (50–500 FTE) in bouw, installatietechniek, industriële dienstverlening, onderhoud en logistiek**, die ISO 9001 + VCA hebben en ISO 14001/45001 erbij hebben of willen. | Generiek: alle organisaties met ISO-certificering, internationaal. |
| Voordelen | Hoge pijn (meerdere certificaten, veel veldwerk, LMRA/toolbox-verplichtingen), budget, korte beslislijnen, bereikbaar via certificatie-instellingen en adviseurs. | Grotere TAM. |
| Nadelen | Beperkte TAM in NL alleen (~5–8k bedrijven). | Geen focus, geen referenties, generieke marketing, concurreren met iedereen. |
| Kosten / complexiteit | Laag — één taal, één regelgevingskader. | Hoog — meertaligheid, lokale wetgeving. |
| Time-to-market | 6–9 maanden tot betalende klanten. | 12–18 maanden. |
| Commerciële impact | Snelle referenties en word-of-mouth binnen sectornetwerken. | Lage conversie. |

### Keuze 2 — Productpositionering

**Beste optie:** *"Het IMS dat zichzelf bijhoudt: van veldmelding tot management review, audit-ready in één platform, met AI die het papierwerk doet."*
Kern: **integratie (één registratie, meerdere normen) + veldgebruik (mobiel) + AI-auditvoorbereiding.**

**Alternatief:** "AI compliance copilot" — alleen een AI-laag bovenop bestaande documenten (SharePoint) zonder eigen registers.
- Voordeel: sneller te bouwen (3–4 maanden), lage switching-drempel.
- Nadeel: geen system of record → lage switching costs, lage ACV, makkelijk te kopiëren door Microsoft Copilot/SharePoint-agents en door gevestigde spelers.
- **Advies:** gebruik de copilot als *instap* (gap-analyse op bestaande documenten als lead magnet en onboardingtool), maar bouw het system of record. Daar zit de recurring revenue en de moat.

### Keuze 3 — Architectuur

**Beste optie:** modulaire monoliet (TypeScript of .NET), PostgreSQL met row-level security, Azure EU-regio's, PWA voor mobiel. Zie [05](05-technische-architectuur.md).
**Alternatief:** microservices op Kubernetes. Afgewezen voor fase 0–4: 2–3× hogere bouw- en beheerkosten zonder klantwaarde.

### Keuze 4 — AI-rol

**Beste optie:** AI is **adviserend en traceerbaar** (bronverwijzingen, human-in-the-loop, audit log). Alle compliance-status, workflows, termijnen, rechten en berekeningen blijven **deterministisch**. AI beoordeelt **nooit individuele werknemers** (voorkomt high-risk onder de EU AI Act, zie [06](06-security-privacy-ai-act.md)).

### Keuze 5 — Verdienmodel

**Beste optie:** hybride prijsmodel — platformfee per tier + prijs per medewerker (degressief), **onbeperkt gratis meldende gebruikers** (veldwerkers), plus betaalde implementatie. Zie [08](08-pricing-businessmodel.md).
Reden: per-user-pricing remt adoptie in het veld, terwijl juist brede veldadoptie (meldingen, LMRA, toolbox) de data en lock-in oplevert.

### Keuze 6 — Financieringspad

**Beste optie:** "klein team"-scenario (pre-seed € 0,6–1,0 mln), na 10–15 betalende klanten seed (€ 2–3 mln). VC-scale-up pas na bewezen NRR > 105% en een tweede land/kanaal. Zie [09](09-financieel-model.md).

---

## 3. Grootste risico's (top 10)

| # | Risico | Kans | Impact | Mitigatie |
|---|---|---|---|---|
| 1 | **Te breed product** — 30 modules half af, niets beter dan concurrent | Hoog | Zeer hoog | Harde MVP-scope (§4), "niet bouwen"-lijst, elke module moet een betalende design partner hebben. |
| 2 | **AI-differentiatie verdampt** — concurrenten en Microsoft Copilot leveren vergelijkbare AI | Hoog | Hoog | Moat in datamodel, workflow, sectorcontent en kanaal; AI als versneller, niet als enige USP. |
| 3 | **Verkoopcycli langer dan verwacht** (3–9 mnd mid-market) | Hoog | Hoog | Wedge via certificatie-/audittijdstip, partners (adviesbureaus), pilot → betaald binnen 60 dagen. |
| 4 | **Migratie van bestaande documenten/registers** is zwaar | Hoog | Midden | AI-gestuurde import (documentclassificatie, clausule-mapping) als product-feature én betaalde dienst. |
| 5 | **Hallucinatie in compliance-context** leidt tot verkeerde auditconclusies | Midden | Zeer hoog | Bronverplichting, confidence, reviewstap, geen AI-output als formele status. |
| 6 | **Copyright ISO-normteksten** — normtekst mag niet zonder licentie in het product | Hoog | Hoog | Alleen clausulenummers, titels en eigen parafrases/vragenlijsten; licentiegesprek met NEN/ISO; klant uploadt eigen exemplaar. |
| 7 | **Privacy/OR** — incidenten bevatten gezondheidsdata; systeem kan als personeelsvolgsysteem gelden (WOR art. 27) | Midden | Hoog | Privacy by design, DPIA-template voor klant, OR-informatiepakket, pseudonimisering. |
| 8 | **Security-incident / tenant-lek** in vroege fase | Laag–midden | Fataal | RLS + tenant-tests in CI, pentest vóór lancering, ISO 27001 binnen 18–24 mnd. |
| 9 | **Founder/teamrisico** — domeinkennis zonder technische cofounder of andersom | Onbekend | Hoog | Cofounder-/CTO-keuze vóór fase 2; geen volledige outsourcing van de kern. |
| 10 | **Runway** — te vroeg schalen van sales vóór product-market fit | Midden | Hoog | Stage-gates op metrics (zie [10](10-mvp-roadmap-validatie.md)). |

---

## 4. Beste MVP-positionering

**MVP-belofte:** *"Binnen 30 dagen audit-ready voor ISO 9001, 14001, 45001 en VCA — met één registratie voor alle normen en meldingen direct vanuit het veld."*

**MVP = vier samenhangende kernstromen** (meer niet):

1. **Normen & documenten** — normkader (clausulestructuur volgens Harmonized Structure), documentbeheer met versies en goedkeuring, koppeling document ↔ clausule.
2. **Melden & opvolgen** — mobiele meldingen (incident, bijna-ongeval, observatie, klacht), actie/CAPA-workflow met termijnen.
3. **Audits & inspecties** — interne auditplanning, checklists (mobiel), bevindingen → CAPA.
4. **AI-auditvoorbereiding** — gap-analyse van bestaande documenten tegen de normstructuur, auditdossier per clausule met bronverwijzing, management review-concept.

**Expliciet niet in MVP:** permits/PTW, assets, contractor-portaal, training-LMS, uitgebreide workflowdesigner, Power BI-connector, native apps, SAP. Zie [10](10-mvp-roadmap-validatie.md).

**Bewijs dat het MVP werkt:** ≥ 5 betalende klanten (niet "pilots met korting naar nul") met ≥ € 5k ACV binnen 6 maanden na MVP-oplevering, en ≥ 60% wekelijks actieve kerngebruikers.

---

## 5. Kritische kanttekeningen bij het oorspronkelijke idee

1. **De moduleslijst (30+ modules) is een enterprise-EHS-suite.** Intelex en Cority hebben daar 20+ jaar en honderden ontwikkelaars over gedaan. Starten met die breedte garandeert middelmatigheid. Bouw de *datamodel-fundering* breed (zie [07](07-datamodel-iso.md)), maar de *UI-modules* smal.
2. **"AI" is geen positionering.** Kopers in QHSE kopen audit-readiness, minder administratie en grip; AI is hoe je dat levert.
3. **Enterprise (10.000 medewerkers) is geen vroege doelgroep.** Vereist SOC 2/ISO 27001, SSO/SCIM, SAP-integratie, inkoopprocessen van 6–12 maanden. Pas vanaf fase 6.
4. **ISO 27001 als vierde norm** is een andere koper (CISO/IT) en een andere markt (Vanta, Drata e.d.). Ondersteun hem in het datamodel, maar verkoop er niet mee in de eerste twee jaar.
5. **Native apps zijn in het begin niet nodig.** Een goede PWA met offline-modus dekt 90% van het veldgebruik.

---

## 6. Eindadvies (samenvatting — uitgebreid in [11](11-gtm-risicos-investering.md))

**Doorgaan, onder voorwaarden:**

1. Start met 8–12 weken discovery: 25+ interviews met QHSE-managers in de ICP, 3–5 design partners met intentieverklaring (LOI) en betaalbereidheid.
2. Bouw een klikbaar prototype + AI-gap-analyse op echte klantdocumenten vóór het eigen platform.
3. Bouw het MVP (4–6 maanden, team van 3–5) op de hier beschreven architectuur.
4. Verkoop founder-led + via 2–3 adviesbureaus/certificatiepartners.
5. Schaal pas (seed) bij: ≥ 15 betalende klanten, logo-churn < 10%, gemiddelde ACV ≥ € 8k, CAC-payback < 18 maanden.

**Niet doorgaan / pivoteren als:** na discovery minder dan 3 van 10 doelgroeporganisaties concreet willen betalen boven € 4k/jaar, of als de pijn vooral bij consultants zit (dan: product voor adviesbureaus als kanaal i.p.v. eindklant).

---

## 7. Aannames

| # | Aanname | Gevolg als onjuist |
|---|---|---|
| A1 | Thuismarkt is Nederland/België, taal NL + EN. | Andere startmarkt verandert GTM en compliance (bijv. DE: Betriebsrat, DSGVO-praktijk strenger). |
| A2 | De founder heeft QHSE/ISO-domeinkennis en een netwerk in de doelgroep. | Zonder netwerk: CAC 2–3× hoger, langere validatie. |
| A3 | Er is (nog) geen technische cofounder; ontwikkeling via klein eigen team, eventueel met freelancers. | Met technische cofounder: lagere burn, snellere MVP. |
| A4 | Startkapitaal bootstrap € 50–150k of pre-seed € 0,6–1,0 mln. | Zie scenario's in [09](09-financieel-model.md). |
| A5 | Gangbare loonkosten NL 2026: developer fully loaded € 85–115k/jaar; freelance € 85–125/uur. | Kosten schalen lineair mee. |
| A6 | LLM-API-prijzen blijven gelijk of dalen (trend 2023–2026: sterk dalend per capaciteitsniveau). | AI-marge is gevoelig; modelrouting is noodzakelijk. |
| A7 | De oorspronkelijke FDS beschrijft de genoemde 30+ modules; prioritering hier wijkt daar bewust van af. | Afstemmen in PRD-fase. |

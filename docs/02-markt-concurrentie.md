# 02 — Marktanalyse & Concurrentieanalyse

> Alle cijfers zijn **indicatief**. Marktrapporten (Verdantix, Gartner, MarketsandMarkets e.d.) hanteren uiteenlopende definities. Verifieer en citeer bronnen vóór gebruik in een investeringsmemorandum.

## 1. Marktdefinitie

IMS Nexus AI zit op het snijvlak van vier softwaremarkten:

| Segment | Mondiale omvang (indicatief, 2025/26) | Groei (CAGR) | Relevantie |
|---|---|---|---|
| EHS-software | USD 2–3 mld | ~9–12% | Hoog |
| QMS-software (excl. life-sciences-specifiek) | USD 3–6 mld (afhankelijk van definitie) | ~9–11% | Hoog |
| GRC / compliance-automatisering | USD 15+ mld | ~12–14% | Midden (ISO 27001-hoek) |
| Inspectie-/field-apps | USD 1–2 mld | ~12–15% | Midden |

**Waarom de markt groeit:** strengere wetgeving (CSRD/ESG-rapportage — deels uitgesteld via de EU Omnibus, maar keten-eisen blijven), NIS2 (in NL de Cyberbeveiligingswet), aanbestedingseisen (ISO, VCA, CO2-Prestatieladder), personeelstekort (minder QHSE-capaciteit → automatisering), en AI die de kosten van compliance-werk structureel verlaagt.

## 2. TAM / SAM / SOM (bottom-up)

| Laag | Definitie | Aantal organisaties | Gem. ACV | Waarde/jaar |
|---|---|---|---|---|
| **SOM NL (5 jaar)** | 4–6% van ICP A+B in NL | 250–350 | € 11k | **€ 2,8–3,9 mln ARR** |
| **SAM NL/BE** | ICP A+B (50–1.000 FTE, ISO/VCA) | ~7.000–9.000 | € 11k | € 75–100 mln |
| **SAM Europa (tweede golf)** | Zelfde ICP in DACH, Nordics, UK, FR (lokalisatie vereist) | ~60.000–80.000 | € 13k | € 0,8–1,0 mld |
| **TAM** | Alle organisaties met ≥ 1 ISO-managementsysteemcertificaat wereldwijd (> 1,5 mln certificaten volgens ISO Survey) incl. MKB/enterprise | ~1 mln+ sites | sterk variabel | USD 8–12 mld |

**Kritische conclusie:** de **Nederlandse markt alleen** ondersteunt een gezond, winstgevend bedrijf van € 3–8 mln ARR, maar geen venture-scale uitkomst (> € 50–100 mln ARR). Voor een VC-case is internationale expansie (DACH/Nordics/UK) of een enterprise-beweging vanaf jaar 3 noodzakelijk. Dat is een bewuste keuze, geen gegeven.

## 3. Concurrentielandschap

### Segmentering

```mermaid
quadrantChart
  title Positionering (indicatief)
  x-axis Smal / point solution --> Breed / suite
  y-axis MKB / mid-market --> Enterprise
  quadrant-1 Enterprise suites
  quadrant-2 Enterprise niche
  quadrant-3 Mid-market tools
  quadrant-4 Mid-market suites
  Enablon: [0.9, 0.92]
  Cority: [0.85, 0.85]
  Intelex: [0.82, 0.8]
  Sphera: [0.8, 0.88]
  VelocityEHS: [0.72, 0.7]
  Benchmark Gensuite: [0.78, 0.75]
  Quentic: [0.7, 0.5]
  EcoOnline: [0.62, 0.42]
  Ideagen: [0.66, 0.6]
  SafetyCulture: [0.35, 0.35]
  Zenya: [0.5, 0.4]
  Capptions: [0.25, 0.25]
  Effivity: [0.45, 0.15]
  Vanta/Drata: [0.3, 0.55]
  IMS Nexus AI (doel): [0.55, 0.3]
```

### Vergelijkingsmatrix

Legenda: ●●● sterk, ●● gemiddeld, ● zwak, — niet/onbekend. Indicatief; te valideren met demo's en klantgesprekken.

| Speler | HQ / eigenaar | Doelgroep | Breedte | UX | AI (2026) | Mobiel | Integraties | Pricing (indicatief) | Sterkte | Zwakte | Gap voor IMS Nexus |
|---|---|---|---|---|---|---|---|---|---|---|---|
| **Enablon** | FR / Wolters Kluwer | Enterprise | ●●● | ● | ●● | ●● | ●●● | € 100k–1 mln+/jr | Volledigheid, ESG/GRC | Complex, lange implementatie | Mid-market onbereikbaar voor hen |
| **Cority** | CA | Enterprise | ●●● | ●● | ●● | ●● | ●●● | $ 50k–500k+/jr | Occupational health, analytics | Prijs, implementatieduur | Idem |
| **Intelex** | CA / Fortive | Enterprise / upper-mid | ●●● | ●● | ●● | ●● | ●●● | $ 30k–300k/jr | Configureerbaarheid, ISO-modules | Verouderde UX-onderdelen | Idem |
| **Sphera** | US | Enterprise (procesindustrie) | ●●● | ● | ●● | ●● | ●●● | $ 100k+/jr | Process safety, ESG | Niet voor mid-market | — |
| **VelocityEHS** | US | Mid–enterprise (US) | ●●● | ●● | ●● | ●● | ●● | $ 20k–200k/jr | Chemicaliën, ergonomie, AI | US-focus | EU/NL-lokalisatie |
| **Benchmark Gensuite** | US | Enterprise | ●●● | ●● | ●● (AI-assistent) | ●● | ●● | Op aanvraag | Breed, vroeg met AI | US-focus | Idem |
| **Quentic** | DE / Wolters Kluwer | Mid-market DACH | ●●● | ●● | ●● | ●● | ●● | € 10k–80k/jr modulair | Modulair, DACH-sterk | Beperkte NL-aanwezigheid | NL/VCA |
| **EcoOnline** | NO | Mid-market Europa | ●● | ●● | ●● | ●● | ●● | € 5k–50k/jr | Chemicaliën, incidenten, Europa | Minder sterk in QMS/ISO 9001 | Geïntegreerd ISO + VCA |
| **Ideagen** | UK | Gereguleerde sectoren | ●●● | ●● | ●● | ●● | ●● | € 10k–100k/jr | Kwaliteit/audit, veel overnames | Gefragmenteerde productsuite | Eén samenhangend product |
| **SafetyCulture** | AU | MKB–enterprise, frontline | ●● | ●●● | ●● | ●●● | ●● | Freemium; ~$ 20–30/user/mnd | UX, inspecties, adoptie | Geen volwaardig IMS/clausulebeheer | ISO-clausule-integratie, management review |
| **Zenya (Infoland)** | NL | Zorg, overheid, mid-market | ●● | ●● | ● | ●● | ●● | € 5k–40k/jr | Documentbeheer, NL-markt, zorg | Minder veld/VCA-gericht, AI beperkt | Bouw/industrie, AI |
| **Capptions** | NL | MKB, inspecties/meldingen | ● | ●● | ● | ●●● | ● | € 1–10k/jr | Simpele mobiele formulieren | Geen IMS | Upsell: van melding naar IMS |
| **Effivity e.a.** | UK/IN | MKB ISO | ●● | ● | ● | ● | ● | € 1–5k/jr | Prijs | UX, diepgang | Kwaliteit |
| **Vanta / Drata / Secureframe** | US | Tech-bedrijven (SOC 2/ISO 27001) | ● (security) | ●●● | ●●● | — | ●●● (tech stack) | $ 10k–80k/jr | Automatisering, UX, AI | Geen QHSE | Inspiratie voor UX en automatisering; niet direct concurrent |
| **Microsoft 365 + Copilot + Power Platform** | US | Iedereen | DIY | ●● | ●●● | ●● | ●●● | Al betaald | Al aanwezig, Copilot op SharePoint | Geen datamodel, geen workflow-out-of-the-box | **Grootste substituut**: bouw *bovenop* M365, niet ertegen |
| **Excel + consultant** | — | MKB/mid | — | — | — | — | — | € 5–25k/jr consultancy | Vertrouwd | Foutgevoelig, niet schaalbaar | Echte concurrent in ICP A |

### Belangrijkste inzichten

1. **De echte concurrent in de ICP is Excel + SharePoint + consultant**, niet Enablon. Verkoop tegen *status quo*, niet tegen features.
2. **Enterprise-spelers zijn te duur en te zwaar** voor 50–500 FTE. **SafetyCulture is te smal** (geen IMS). **Quentic/EcoOnline** zijn de meest directe mid-market concurrenten, maar zwak op NL/VCA-specifieke content.
3. **AI is in 2026 geen onderscheid meer op zich.** Bijna elke speler heeft een "AI-assistent". Het verschil zit in *diepte*: AI die het geïntegreerde datamodel begrijpt (clausule ↔ bewijs ↔ actie) vs. een chatbot over documenten.
4. **Microsoft Copilot** zal eenvoudige "vraag-je-documenten"-use-cases commoditiseren. IMS Nexus moet daarom *gestructureerde* compliance-data en workflow bezitten.

## 4. Opportunity gaps

| Gap | Bewijs/indicatie | Kans voor IMS Nexus |
|---|---|---|
| Geïntegreerd ISO 9001/14001/45001 + VCA in één mid-market product met moderne UX | NL-tools zijn document-centrisch; internationale tools missen VCA | **Primaire wedge** |
| Auditvoorbereiding is nog grotendeels handwerk | Consultancy-uitgaven in ICP | AI-auditdossier per clausule |
| Veldadoptie: QHSE-systemen worden alleen door kantoor gebruikt | Onder-rapportage van meldingen | Gratis veld-seats, 60-sec-melding, spraak |
| Adviseurs hebben geen multi-klant-tool | Adviseurs gebruiken Word-templates | Partnerportaal (kanaal + lock-in) |
| Management review (ISO §9.3) is overal handwerk | Klantinterviews te valideren | AI-gegenereerde review uit live data |
| Wet- en regelgevingsregister NL is duur/handmatig | Abonnementen bij specialisten | Later: partnercontent i.p.v. zelf bouwen |

## 5. Wat te leren van concurrenten

| Van | Overnemen | Vermijden |
|---|---|---|
| SafetyCulture | Freemium-veldadoptie, extreem snelle mobiele UX, template-bibliotheek | Breedte zonder diepte |
| Vanta/Drata | "Compliance-status als live score", automatische bewijsverzameling, onboarding in dagen | Tech-only focus |
| Quentic | Modulaire licentie, sterk datamodel | Complexe configuratie |
| Zenya | Lokale aanwezigheid, gebruikersgroepen | Document-centrisch denken |
| Enterprise-suites | Audit trail, configureerbaarheid, rapportages | Implementatietrajecten van 6–12 maanden |

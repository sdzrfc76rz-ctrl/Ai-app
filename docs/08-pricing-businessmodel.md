# 08 — Pricing & businessmodel

## 1. Prijsmodellen vergeleken

| Model | Voordelen | Nadelen | Fit met IMS Nexus | Oordeel |
|---|---|---|---|---|
| Per user (alle gebruikers) | Simpel, bekend | **Remt veldadoptie**: klant beperkt accounts → minder meldingen → minder waarde | Slecht | ✗ |
| Per actieve gebruiker | Eerlijk | Onvoorspelbaar budget, boekhoudkundig gedoe, perverse prikkel (minder gebruik = goedkoper) | Matig | ✗ |
| **Per volledige gebruiker + gratis veld-gebruikers** | Adoptie in veld, betalen voor kantoorgebruik | Klanten "delen" kantooraccounts; lagere ACV bij grote organisaties | Goed voor MKB | ✓ (instap) |
| **Per medewerker (FTE-band)** | Schaalt met waarde en organisatiegrootte, voorspelbaar, iedereen mag gebruiken | Lastig bij veel inhuur/flexkrachten; uitleg nodig | Zeer goed | ✓ (kern) |
| Per site | Logisch voor multi-site industrie | Bouwprojecten = tijdelijke sites → onwerkbaar voor ICP A | Matig | Alleen enterprise |
| Module-based | Upsell-pad, klant betaalt wat hij gebruikt | Complexe offertes, "nickel-and-diming" | Goed in combinatie met tiers | ✓ (beperkt: 2–3 add-ons) |
| Tiered SaaS | Duidelijk, upsell via tiers | Tiers moeten logisch zijn | Zeer goed | ✓ |
| Enterprise contract | Hoge ACV, maatwerk | Lange cycli, maatwerkverleiding | Fase 6 | ✓ (later) |

**Aanbeveling:** **Tiered + per medewerker (degressief) + platformfee + gratis veld-gebruikers**, met maximaal 2–3 add-ons.

Aannames voor de rekenvoorbeelden:

| Organisatiegrootte (medewerkers) | 20 | 100 | 500 | 2.000 | 10.000 |
|---|---|---|---|---|---|
| Volledige (kantoor)gebruikers | 3 | 8 | 25 | 70 | 250 |
| Sites (vaste vestigingen) | 1 | 2 | 5 | 15 | 60 |

## 2. Strategie A — Laagdrempelig (per volledige gebruiker)

- **€ 39 per volledige gebruiker per maand** (jaarcontract), veld-gebruikers gratis, minimum € 149/maand.
- Inclusief: documenten, normen, meldingen, acties, inspecties, basis-AI.
- Self-serve onboarding, geen implementatiefee (optioneel € 995 quickstart).

| Medewerkers | Berekening | €/maand | **€/jaar** | €/medewerker/maand |
|---|---|---|---|---|
| 20 | 3 × 39 = 117 → minimum | 149 | **1.788** | 7,45 |
| 100 | 8 × 39 | 312 | **3.744** | 3,12 |
| 500 | 25 × 39 | 975 | **11.700** | 1,95 |
| 2.000 | 70 × 39 | 2.730 | **32.760** | 1,37 |
| 10.000 | 250 × 39 (lijst) | 9.750 | **117.000** (realistisch na korting ~80k) | 0,98 |

Oordeel: goed voor < 50 FTE en product-led groei; **te lage ACV** voor sales-gedreven mid-market (CAC wordt niet terugverdiend bij 100 FTE / € 3,7k).

## 3. Strategie B — Mid-market (AANBEVOLEN)

| Tier | Platformfee/maand | Per medewerker/maand | Inhoud |
|---|---|---|---|
| **Essentials** | € 149 | € 3,00 (1–100), € 1,50 (> 100) | Documenten, normen (1 norm + VCA), meldingen, acties, inspecties/LMRA, basis-AI (classificatie, spraak) |
| **Professional** | € 395 | € 4,00 (1–500), € 2,50 (501–2.000), € 1,25 (> 2.000) | + alle normen, audits, CAPA, risico's/TRA, management review, **AI-auditdossier & gap-analyse**, SSO (Entra ID), API (read) |
| **Enterprise** | vanaf € 40k/jaar | maatwerk | + SCIM, multi-entity, silo-DB/CMK, SLA 99,9%, SIEM-export, Power BI, dedicated CSM |
| Add-on **AI Advanced** | + 20% op licentie | — | Agents, bulk-analyses, onbeperkte gap-analyses, wetgevingsduiding (fase 4+) |
| Add-on **Contractor & PTW** | + € 1–2k/maand | — | Fase 5 |

Rekenvoorbeelden (lijstprijs, jaarcontract):

| Medewerkers | Tier | Berekening/maand | €/maand | **€/jaar** | €/medewerker/maand |
|---|---|---|---|---|---|
| 20 | Essentials | 149 + 20 × 3 | 209 | **2.508** | 10,45 |
| 20 | Professional | 395 + 20 × 4 | 475 | 5.700 | 23,75 |
| 100 | Essentials | 149 + 100 × 3 | 449 | 5.388 | 4,49 |
| 100 | **Professional** | 395 + 100 × 4 | 795 | **9.540** | 7,95 |
| 500 | **Professional** | 395 + 500 × 4 | 2.395 | **28.740** | 4,79 |
| 2.000 | Professional | 395 + 2.000 + 1.500 × 2,50 | 6.145 | **73.740** | 3,07 |
| 10.000 | Enterprise (lijstberekening) | 395 + 2.000 + 3.750 + 8.000 × 1,25 | 16.145 | 193.740 lijst → **€ 120–160k** onderhandeld | 1,0–1,6 |

Plus **implementatiefee**: Essentials € 0–1.500; Professional € 2.500–7.500 (incl. documentimport + AI-gap-analyse + training); Enterprise € 25–100k.

Waarom B:
- 100 FTE Professional (€ 9,5k) ligt **onder** wat de doelgroep nu aan consultancy uitgeeft (€ 5–25k) en levert meer → makkelijke business case.
- Iedereen mag gebruiken → maximale veldadoptie → data + lock-in.
- Per-medewerker schaalt met organisatiegroei (NRR > 100% zonder upsell-gevecht).
- Platformfee beschermt de marge bij kleine klanten.

Risico's van B en mitigatie: discussie over "wat is een medewerker" (flex/inhuur) → definitie = gemiddeld aantal personen dat in het systeem kan worden geregistreerd als medewerker of veldgebruiker, jaarlijkse true-up, bandbreedtes van 25.

## 4. Strategie C — Enterprise (platform + per site + modules)

- Platformlicentie € 30k/jaar (incl. 3 kernmodules, SSO/SCIM, SLA 99,9%).
- Per site: € 3k/jaar (1–20), € 1,5k/jaar (> 20).
- Extra modules: € 8k/jaar per module (rekenvoorbeeld: 2 extra modules).

| Medewerkers | Sites | Berekening | **€/jaar** | €/medewerker/maand |
|---|---|---|---|---|
| 20 | 1 | 30k + 3k + 16k | **49.000** | 204 — ongeschikt |
| 100 | 2 | 30k + 6k + 16k | **52.000** | 43 — ongeschikt |
| 500 | 5 | 30k + 15k + 16k | **61.000** | 10,2 — te duur |
| 2.000 | 15 | 30k + 45k + 16k | **91.000** | 3,79 |
| 10.000 | 60 | 30k + 60k + 60k + 16k | **166.000** | 1,38 |

Oordeel: alleen geschikt voor ≥ 2.000 medewerkers en multi-site industrie. Gebruik in fase 6 als *contractvorm* bovenop strategie B.

## 5. Vergelijking per organisatiegrootte (€/jaar)

| Medewerkers | A (laagdrempelig) | **B (mid-market, Professional tenzij anders)** | C (enterprise) | Marktindicatie (concurrentie) |
|---|---|---|---|---|
| 20 | 1.788 | 2.508 (Essentials) | 49.000 | € 1–5k |
| 100 | 3.744 | 9.540 | 52.000 | € 4–15k |
| 500 | 11.700 | 28.740 | 61.000 | € 15–50k |
| 2.000 | 32.760 | 73.740 | 91.000 | € 40–150k |
| 10.000 | ~80.000 | 120–160k | 166.000 | € 100–500k |

**Pricing-validatie:** test vóór lancering met Van Westendorp-vragen (20+ interviews) en met echte offertes aan design partners (prijs ankeren met consultancykosten). Verwachting: Professional voor 100 FTE ligt aan de bovenkant van acceptabel; overweeg een lanceringsprijs van € 6–7/medewerker zonder platformfee voor de eerste 20 klanten, met prijsgarantie van 24 maanden.

## 6. Businessmodel

| Inkomstenstroom | Aandeel (jaar 3) | Bruto marge | Toelichting |
|---|---|---|---|
| **SaaS-abonnementen** | 75–85% | 78–82% | Kern; jaarcontracten vooraf gefactureerd (cashflow) |
| **Implementatie & onboarding** | 10–15% | 30–50% | Gestandaardiseerde pakketten (S/M/L), niet uurtje-factuurtje; AI-documentimport maakt het schaalbaar |
| Consultancy (IMS-inrichting, interne audits) | 0–5% | 20–40% | **Bewust beperken** — liever via partners (kanaal). Eigen consultancy verdringt partners en verlaagt de waardering |
| Premium AI (add-on) | 3–8% | 70–85% | Vanaf fase 4 |
| Enterprise-integraties | 2–5% | 40–60% | Eenmalig + jaarlijkse onderhoudsfee |
| Support-tiers | in licentie / enterprise-premium | — | Standaard support inbegrepen; premium (SLA, CSM) in Enterprise |
| Training / academy | 1–3% | 50–70% | AI-geletterdheid (AI Act), IMS-basistraining, certificering "IMS Nexus-consultant" voor partners |
| Partnerinkomsten (revenue share van contentpartners) | 0–2% | hoog | Wetgevingscontent, templates |

**Partnermodel (adviesbureaus):** 15–20% recurring commissie op doorverwezen licenties in jaar 1, 10% daarna; óf wholesale-prijs (–25%) als het bureau zelf factureert. Partner-tenant met multi-klantoverzicht gratis.

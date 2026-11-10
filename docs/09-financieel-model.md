# 09 — Financieel model

> Alle bedragen in euro's, nominaal, excl. btw. Indicatief model op basis van de aannames hieronder; uitwerken in een spreadsheet met maandgranulariteit vóór gebruik richting investeerders.

## 1. Gemeenschappelijke aannames

| Parameter | Waarde | Toelichting |
|---|---|---|
| Developer (fully loaded, NL) | € 95–110k/jaar | Salaris + werkgeverslasten + tooling |
| Freelance developer | € 90–120/uur | ~€ 150–190k/jaar bij voltijd |
| Founders | € 60–80k/jaar elk (onder marktconform) | — |
| Sales/CS-medewerker | € 75–95k + variabel | — |
| Bruto marge abonnementen | 65% (jr 1) → 72% (jr 2) → 78–80% (jr 3+) | Cloud, AI, support, payment, hosting-tools |
| Gross logo churn | 12% (jr 1–2) → 8–10% (jr 3+) | Mid-market benchmark |
| Net revenue retention (NRR) | 100% → 105–110% | Groei in medewerkers, tier-upgrades, add-ons |
| Implementatiefee | gem. € 3k per nieuwe klant (jr 1–2), € 4k later | — |
| Omzetherkenning | Abonnement: gemiddeld ARR van begin- en eindjaar | Vereenvoudiging |
| Facturatie | Jaarlijks vooraf | Positief voor cashflow (niet meegenomen in P&L hieronder) |
| Certificering & security | ISO 27001: € 30–60k eerste jaar, € 15–25k/jaar daarna; pentest € 10–20k/jaar | — |
| Legal | € 20–40k opstart (DPA, AV, SLA, AUP, privacybeleid, AI-factsheets, BV-structuur), daarna € 15–30k/jaar | — |

## 2. Vier scenario's — overzicht

| | 1. Bootstrap | **2. Klein team (aanbevolen start)** | 3. Professionele SaaS-startup | 4. VC-funded scale-up |
|---|---|---|---|---|
| Financiering | € 50–100k eigen middelen + omzet uit diensten | Pre-seed € 0,75 mln + seed € 2,0 mln (mnd 12–15) | Seed € 2,5 mln + Series A € 8 mln (jr 3) | Seed € 3 mln + A € 12 mln + B € 30 mln |
| Team einde jr 1 / jr 3 / jr 5 (FTE) | 2 / 4 / 9 | 4 / 14 / 30 | 10 / 35 / 70 | 15 / 70 / 160 |
| Klanten einde jr 1–5 | 6 / 25 / 60 / 110 / 170 | 12 / 45 / 110 / 200 / 320 | 20 / 80 / 200 / 400 / 700 | 25 / 120 / 350 / 800 / 1.500 |
| Gem. ACV jr 1→5 | € 6k → 9k | € 8k → 12k | € 9k → 16k | € 10k → 22k |
| ARR einde jr 5 | **€ 1,5 mln** | **€ 3,8 mln** | **€ 11,2 mln** | **€ 33 mln** |
| Break-even | Jr 2 (dankzij dienstenomzet) | Eind jr 5 (~€ 3,5–3,8 mln ARR) | Eind jr 5 (~€ 11 mln ARR) | Na jr 5 |
| Max. cumulatief tekort | ~€ 35–80k | ~€ 2,75 mln | ~€ 7,9 mln | ~€ 17 mln+ |
| Belangrijkste risico | Te traag; concurrent of Copilot sneller | Seed-ronde moet lukken in mnd 12–15 | Internationale expansie moet slagen | Vereist enterprise + 3+ landen; lage kans |

## 3. Scenario 1 — Bootstrap

Founder bouwt met 1 (freelance) developer; founder verdient bij met IMS-consultancy/implementaties.

| (€ k) | Jr 1 | Jr 2 | Jr 3 | Jr 4 | Jr 5 |
|---|---|---|---|---|---|
| Klanten (einde jaar) | 6 | 25 | 60 | 110 | 170 |
| ARR (einde jaar) | 36 | 175 | 480 | 935 | 1.530 |
| Omzet abonnementen | 15 | 105 | 330 | 710 | 1.230 |
| Omzet diensten (implementatie/consultancy) | 60 | 80 | 100 | 100 | 120 |
| **Totale omzet** | 75 | 185 | 430 | 810 | 1.350 |
| Totale kosten | 110 | 180 | 330 | 560 | 900 |
| **Resultaat** | **–35** | **+5** | **+100** | **+250** | **+450** |

Oordeel: financieel veilig, maar **MVP pas na 12–15 maanden**, founder verdeeld tussen consultancy en product, en het venster ("AI-native IMS") kan sluiten. Geschikt als de founder een sterke consultancypraktijk heeft en een *lifestyle/profitable SaaS* nastreeft.

## 4. Scenario 2 — Klein developmentteam (AANBEVOLEN STARTPAD)

### P&L (indicatief)

| (€ k) | Jr 1 | Jr 2 | Jr 3 | Jr 4 | Jr 5 |
|---|---|---|---|---|---|
| Klanten (einde jaar) | 12 | 45 | 110 | 200 | 320 |
| Gem. ACV | 8,0 | 9,0 | 10,0 | 11,0 | 12,0 |
| **ARR (einde jaar)** | **96** | **405** | **1.100** | **2.200** | **3.840** |
| MRR (einde jaar) | 8 | 34 | 92 | 183 | 320 |
| Omzet abonnementen | 48 | 250 | 753 | 1.650 | 3.020 |
| Omzet implementatie | 36 | 105 | 210 | 300 | 400 |
| **Totale omzet** | **84** | **355** | **963** | **1.950** | **3.420** |
| Cost of revenue | 35 | 110 | 270 | 470 | 790 |
| **Bruto marge** | 58% | 69% | 72% | 76% | 77% |
| R&D | 380 | 610 | 900 | 1.150 | 1.400 |
| Sales & marketing | 80 | 220 | 450 | 700 | 900 |
| G&A (incl. legal, security, certificering) | 105 | 110 | 230 | 280 | 330 |
| **Totale kosten** | **600** | **1.050** | **1.850** | **2.600** | **3.420** |
| **Resultaat (EBITDA)** | **–516** | **–695** | **–887** | **–650** | **0** |
| Cumulatief | –516 | –1.211 | –2.098 | –2.748 | –2.748 |
| FTE (einde jaar) | 4 | 8 | 14 | 22 | 30 |

> Cost of revenue is opgenomen in totale kosten. Totale financieringsbehoefte ≈ **€ 2,75 mln + 15–20% buffer ≈ € 3,2 mln** (pre-seed € 0,75 mln + seed € 2,0–2,5 mln). Break-even rond **maand 55–60** bij ~€ 3,5–3,8 mln ARR. Als Bootstrap-elementen (founder-consultancy, lagere salarissen) worden toegevoegd, schuift break-even 6–12 maanden naar voren.

### Kostenopbouw jaar 1 en jaar 2

| Post (€ k) | Jr 1 | Jr 2 |
|---|---|---|
| Founders (2) | 140 | 160 |
| Development (jr 1: 3 FTE deels freelance; jr 2: 4 FTE) | 300 | 400 |
| Product/UX-design | 40 | 50 |
| Sales / customer success | 0 | 130 |
| Marketing (content, events, LinkedIn, partnerprogramma) | 25 | 60 |
| Cloud + AI | 12 | 30 |
| Tooling/SaaS (auth, monitoring, CRM, design) | 15 | 25 |
| Legal & privacy | 25 | 30 |
| Security (pentest, ISMS-voorbereiding) | 15 | 40 |
| ISO 27001-traject | 0 | 20 |
| Boekhouding, verzekeringen (incl. cyber/beroepsaansprakelijkheid), overig | 28 | 45 |
| Onvoorzien | 0 | 60 |
| **Totaal** | **600** | **1.050** |

### Runway

- Pre-seed € 750k bij gemiddelde netto burn van ~€ 43k/maand (jr 1) en ~€ 58k/maand (jr 2) → kas op rond **maand 16**.
- **Seed-ronde starten in maand 9–10**, sluiten uiterlijk maand 14. Seed-criteria (zie [10](10-mvp-roadmap-validatie.md)): ≥ 15 betalende klanten, ≥ € 120k ARR, bewijs van herhaalbaar kanaal.
- Plan B als seed uitblijft: team terug naar 4 FTE, founders deels consultancy (→ scenario 1-profiel), default alive bij ~€ 700k ARR.

## 5. Scenario 3 — Professionele SaaS-startup

| (€ k) | Jr 1 | Jr 2 | Jr 3 | Jr 4 | Jr 5 |
|---|---|---|---|---|---|
| Klanten | 20 | 80 | 200 | 400 | 700 |
| Gem. ACV | 9 | 11 | 13 | 15 | 16 |
| **ARR** | **180** | **880** | **2.600** | **6.000** | **11.200** |
| Totale omzet | 150 | 730 | 2.190 | 5.100 | 9.800 |
| Totale kosten | 1.500 | 2.800 | 4.600 | 7.200 | 9.800 |
| **Resultaat** | **–1.350** | **–2.070** | **–2.410** | **–2.100** | **0** |
| Cumulatief | –1.350 | –3.420 | –5.830 | –7.930 | –7.930 |

Voorwaarden: tweede land (BE/DE) vanaf jaar 2–3, partnerkanaal draagt ≥ 30% van nieuwe ARR, ISO 27001 in jaar 2, start enterprise-beweging in jaar 4.

## 6. Scenario 4 — VC-funded scale-up

| (€ mln) | Jr 1 | Jr 2 | Jr 3 | Jr 4 | Jr 5 |
|---|---|---|---|---|---|
| Klanten | 25 | 120 | 350 | 800 | 1.500 |
| Gem. ACV (€ k) | 10 | 13 | 16 | 19 | 22 |
| **ARR** | **0,25** | **1,56** | **5,6** | **15,2** | **33,0** |
| Totale omzet | 0,2 | 1,2 | 4,5 | 12,4 | 27,6 |
| Totale kosten | 2,2 | 5,0 | 10,0 | 18,0 | 28,0 |
| **Resultaat** | **–2,0** | **–3,8** | **–5,5** | **–5,6** | **–0,4** |
| Cumulatief | –2,0 | –5,8 | –11,3 | –16,9 | –17,3 |

**Kritisch oordeel:** deze groeicurve (×6, ×3,6, ×2,7, ×2,2) is top-decile voor vertical B2B SaaS. Vereist: 3+ landen, enterprise-sales, waarschijnlijk acquisities (bijv. lokale KAM-/inspectie-apps). **Niet plannen als basisscenario**; alleen nastreven als scenario 2 in jaar 2 duidelijk boven plan presteert (NRR > 110%, CAC-payback < 12 mnd).

## 7. Unit economics (scenario 2, jaar 3)

| Metric | Waarde | Berekening / benchmark |
|---|---|---|
| ACV | € 10.000 | — |
| Bruto marge (abonnement) | 78% | — |
| Gross logo churn | 10%/jaar | Mid-market benchmark 8–15% |
| NRR | 105% | Doel > 105% |
| CAC — founder-led | € 4–6k | Tijd founder + reiskosten + demo's |
| CAC — via partner | € 7–9k | Incl. partnercommissie eerste jaar |
| CAC — outbound/inside sales | € 12–18k | Salaris + tooling + marketing / deals |
| **CAC (blended)** | **€ 12k** | — |
| LTV (= ACV × GM / churn) | € 78k | 10.000 × 0,78 / 0,10 |
| **LTV / CAC** | **6,5** | Doel > 3; optimistisch → valideren |
| **CAC-payback** | **~18 maanden** | 12.000 / (10.000 × 0,78 / 12) |
| Magic number (doel) | > 0,7 | Netto nieuwe ARR / S&M-uitgaven vorig kwartaal |
| Rule of 40 (jr 5) | ~75 (groei 75% + marge 0%) | — |
| Burn multiple (jr 3) | ~1,3 | 887 / 695 netto nieuwe ARR → gezond (< 2) |

## 8. Gevoeligheidsanalyse (scenario 2, ARR jaar 5)

| Variabele | Pessimistisch | Basis | Optimistisch |
|---|---|---|---|
| Nieuwe klanten/jaar (jr 3–5) | –30% → ARR € 2,7 mln | € 3,84 mln | +30% → € 5,0 mln |
| Gem. ACV | € 9k → € 2,9 mln | € 12k | € 15k → € 4,8 mln |
| Logo churn | 15% → € 3,3 mln | 10% | 6% → € 4,2 mln |
| AI-kosten | ×3 → bruto marge –4 pp | — | ×0,5 → +1 pp |

**Grootste hefboom:** ACV (tiering en per-medewerker-pricing) en kanaal (partners verlagen CAC). AI-kosten zijn verwaarloosbaar voor de uitkomst.

# Gala word lists

Public word lists for Gala, a macOS app that helps doctors write
operation reports, clinic letters and meeting summaries with local AI models. Gala checks a
transcript's spelling against these lists — a region's medicines, suburbs and towns, and hospitals, the
generic drug names, and medical device brands and their makers.

Gala downloads them only when a person presses Download on its Speech Engine page. They contain
public reference data only — no patient data.

## Layout

- Each month's lists are a release tagged `lists-YYYY-MM`, holding every file and its manifest
  `lists.json` (each file's region, kind, size, SHA-256, sources, licence and attribution). Lists
  re-issued within their month go in a release of their own (`lists-YYYY-MMb`); the month's stays as
  published.
- The release tagged `lists` holds only the newest manifest, whose `release` names the month's.
  Gala reads `https://github.com/msec9226/gala-lists/releases/download/lists/lists.json`.

Australia's medicines are not here: their licence (the PBS API's) allows redistribution but not
modification, so each Mac fetches them from the PBS itself. Nor is the MBS: the manifest names MBS
Online's own XML (its address, size and SHA-256), which each Mac fetches from there when a person asks.

## Sources and licences

Each list keeps its source's licence. Changes are as stated for each file.

- **au-places.txt** (CC BY 4.0, 15182 entries): ABS ASGS Edition 3, Suburbs and Localities (SAL) 2021. Source: Australian Bureau of Statistics, ASGS Edition 3, Suburbs and Localities 2021, © Commonwealth of Australia, licensed under CC BY 4.0 (https://creativecommons.org/licenses/by/4.0/). Changed: names only, one a line.
- **au-hospitals.txt** (CC BY 4.0, 1571 entries): AIHW MyHospitals API, hospitals. Based on Australian Institute of Health and Welfare material (MyHospitals), licensed under CC BY 4.0. Changed: names only, one a line.
- **nz-medicines.txt** (CC BY 4.0, 2663 entries): PHARMAC Pharmaceutical Schedule 2026-09; PHARMAC Hospital Medicines List 2026-09. Source: Pharmac (Pharmaceutical Management Agency), Pharmaceutical Schedule and Hospital Medicines List (https://schedule.pharmac.govt.nz), licensed under CC BY 4.0. Changed: the chemical and brand names taken out; Pharmac does not endorse this list.
- **nz-places.txt** (CC BY 4.0, 6174 entries): LINZ NZ Suburbs and Localities. This work is based on Toitū Te Whenua Land Information New Zealand data (NZ Suburbs and Localities), which are licensed by Toitū Te Whenua Land Information New Zealand for re-use under the Creative Commons Attribution 4.0 International licence. Changed: names only, one a line.
- **nz-hospitals.txt** (CC BY 4.0, 167 entries): Ministry of Health, certified providers: public and private (NGO) hospitals. Source: Ministry of Health – Manatū Hauora, licensed under CC BY 4.0. Changed: names only, one a line.
- **uk-medicines.txt** (OGL v3, 6875 entries): NHSBSA BNF Code Information (BNF_CODE_CURRENT_202608_VERSION_90). NHSBSA Copyright 2026. Contains public sector information licensed under the Open Government Licence v3.0.
- **uk-places.txt** (OGL v3, 50353 entries): ONS Index of Place Names (July 2024) in GB. Source: Office for National Statistics licensed under the Open Government Licence v3.0. Contains OS data © Crown copyright and database right 2026.
- **uk-hospitals.txt** (OGL v3, 1799 entries): NHS ODS ORD API, NHS trust sites (RO198) named as hospitals; Public Health Scotland, hospital codes. Contains public sector information licensed under the Open Government Licence v3.0 (NHS England; Public Health Scotland).
- **us-medicines.txt** (public domain, 8665 entries): RxNorm prescribable content via RxNav (IN, PIN, MIN, BN). This product uses publicly available data from the U.S. National Library of Medicine (NLM), National Institutes of Health, Department of Health and Human Services; NLM is not responsible for the product and does not endorse or recommend this or any other product. RxNorm as of 2026-09-29.
- **us-places.txt** (public domain, 47021 entries): U.S. Census Bureau Gazetteer Files 2024: places and county subdivisions. Source: U.S. Census Bureau.
- **us-hospitals.txt** (public domain, 5399 entries): CMS Hospital General Information. Source: Centers for Medicare & Medicaid Services.
- **ca-medicines.txt** (OGL–Canada, 5976 entries): Health Canada, Canadian Clinical Drug Data Set (therapeutic moieties, manufactured products). Contains information licensed under the Open Government Licence – Canada (Health Canada).
- **ca-places.txt** (OGL–Canada, 3422 entries): NRCan Canadian Geographical Names Database, concise: cities, towns, villages. Contains information licensed under the Open Government Licence – Canada (Natural Resources Canada).
- **ca-hospitals.txt** (OGL–Canada, 1136 entries): Statistics Canada, Open Database of Healthcare Facilities. Contains information licensed under the Open Government Licence – Canada (Statistics Canada).
- **generics.txt** (public domain; CC0, 6638 entries): RxNorm prescribable ingredients via RxNav; Wikidata items with an ATC code (English labels). This product uses publicly available data from the U.S. National Library of Medicine (NLM), National Institutes of Health, Department of Health and Human Services; NLM is not responsible for the product and does not endorse or recommend this or any other product. Wikidata's data is available under CC0.
- **devices.txt** (public domain (CC0), 16881 entries): openFDA Device Classification (implants; life-sustaining class III); openFDA Unique Device Identification (GUDID): brand and company names; openFDA Premarket Approval (PMA): trade names and applicants. Source: U.S. Food and Drug Administration, openFDA (https://open.fda.gov), public domain under CC0 1.0. Names only, cleaned of marks, model numbers and descriptions; the FDA does not endorse this list. Brand names remain their owners' trademarks.

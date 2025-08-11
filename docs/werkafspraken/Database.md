---
title: Database gebruik
parent: Werkafspraken
layout: default
nav_order: 1
has_toc: false
---

# Databasegebruik

In het GEO-domein maken wij over het algemeen gebruik van twee hoofd-databases:

- **GeoWagDMZ** — SQL  
- **PGEO** — Oracle

---

## GeoWagDMZ

Dit is de SQL-database voor onze DMZ.  
Op deze database zetten wij data die:

- Geen AVG-gevoelige informatie bevat
- Wij willen delen met derden
- Wij willen publiceren op het ArcGIS Online-portaal

---

## PGEO

Dit is de Oracle-database voor onze interne omgeving.  
Op deze database zetten wij data die:

- AVG-gevoelige informatie bevat
- Alleen voor intern gebruik is

### Onderdelen van PGEO

| Database        | Gebruik                                  |
|-----------------|-------------------------------------------|
| `FME@PGEO`      | Actieve database, standaard werkomgeving |
| `GBETLNEW@PGEO` | Oude database, historisch gebruik        |

---

## Waarschuwing

{: .warning }

- Data op **GeoWagDMZ** kan zowel extern als intern gedeeld worden.  
- Data op **PGEO** kan uitsluitend intern gedeeld worden.

---

## Overige databases

Naast de twee hoofd-databases werken wij ook met:

| Database | Doel                                  |
|----------|----------------------------------------|
| `PKIK`   | Database voor BRUTIS (riooldata)       |
| `PDIA`   | Database van DgDialog (BGT-software)   |

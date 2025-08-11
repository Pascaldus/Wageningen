---
title: Naming conventions
parent: Werkafspraken
layout: default
nav_order: 2
has_toc: true
---

# Naming conventions

Als een enkele dataset wordt gebruikt, mag deze in de hoofdstructuur van de database worden geplaatst.

Zijn er meerdere datasets voor één thema, dan mogen deze worden geplaatst in een Feature Dataset.

> **Voorbeeld**  
> Meerdere datasets voor het thema duurzaamheid mogen worden geplaatst in een Feature Dataset genaamd `Duurzaamheid`.

---

# Naming conventions op tabellen

Datasets bouwen wij op met een vaste naamstructuur. Deze bestaat uit drie onderdelen:

## 1. Prefix

| Prefix | Betekenis                                      |
|--------|------------------------------------------------|
| `ST_`  | Statische dataset, handmatig opgebouwd         |
| `ACT_` | Automatisch opgebouwde dataset (FME, Python)   |

## 2. Thema

| Voorbeeld   | Omschrijving                              |
|-------------|-------------------------------------------|
| `ST_BGT`    | Statische dataset binnen het thema BGT    |
| `ACT_BAG`   | Automatisch opgebouwde dataset binnen BAG |

## 3. Beschrijving

Gebruik duidelijke en beschrijvende namen voor het datatype.

{: .important }
Vermijd afkortingen tenzij ze algemeen bekend zijn. Kies voor klare taal zodat datasets makkelijk te herkennen zijn.

### Voorbeelden

| Naam                  | Beoordeling     |
|-----------------------|-----------------|
| ST_BGT_VEGETATIEOBJECT | Correct         |
| ST_BGT_VO              | Niet duidelijk  |

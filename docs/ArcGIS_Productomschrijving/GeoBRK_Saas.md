---
title: GeoBRK SaaS opbouw
parent: Productomschrijving
grand_parent: ArcGIS
layout: default
nav_order: 4
has_toc: false
---

# GeoBRK SaaS Gemeente Wageningen

Op het GIS-portaal van de gemeente Wageningen zijn verschillende lagen als Feature Layer opgenomen. Deze zijn toegevoegd via de SaaS-URL:
https://daas.arcgisonline.nl/arcgis/rest/services/g_wageningen/BRK/MapServer


De volgende lagen zijn opgenomen: `/2`, `/38`, `/39`, `/45`, `/27` en `/31`.

Deze lagen zijn beveiligd met een gebruikersnaam en wachtwoord en gedeeld met de groep **CV Basisregistraties** (GeoHR en GeoBRK). De inloggegevens zijn opgeslagen in het service-item, zodat gebruikers deze niet handmatig hoeven in te voeren.

| Gegevens     | Waarde                          |
|--------------|----------------------------------|
| Gebruikersnaam | `G_Wageningen`                 |
| Wachtwoord     | Zie KeePass of vraag Pascal van de Laak |

---

## Feature Layers

| Naam                                | Link                                                                 |
|-------------------------------------|----------------------------------------------------------------------|
| GeoBRK_SaaS_Perceel Onroerende Zaak | [Item](https://gis.wageningen.nl/portal/home/item.html?id=724593d50d5e47f395e01f1d7bc7c8df) |
| GeoBRK_SaaS_Gerechtigde             | [Item](https://gis.wageningen.nl/portal/home/item.html?id=6a07ef0cad3b450192e24dc7b041b82e) |
| GeoBRK_SaaS_Gerechtigde Anoniem     | [Item](https://gis.wageningen.nl/portal/home/item.html?id=f3946337c40340bc842a628b36b7c372) |
| GeoBRK_SaaS_Publiekrechtelijke beperking | [Item](https://gis.wageningen.nl/portal/home/item.html?id=d398e540a0644646a405ecd37f4a174b) |
| GeoBRK_SaaS_Adres Perceel           | [Item](https://gis.wageningen.nl/portal/home/item.html?id=a3f3d1bf42024d96bedaa0f3b8cd1493) |
| GeoBRK_SaaS_Zoekadres               | [Item](https://gis.wageningen.nl/portal/home/item.html?id=1b1d143c94014d66966c6914923c3aa3) |

---

## WebMap

De lagen *Perceel Onroerende Zaak*, *Gerechtigde*, *Publiekrechtelijke Beperking* en de tabel *Adres Perceel* vormen samen de WebMap:

**GeoBRK_SaaS_WM_Basis**  
[Item](https://gis.wageningen.nl/portal/home/item.html?id=0a9e2f55241d436094c510bd5ebc0889)

---

## Applicaties

### Acceptatieomgeving

| Eigenschap     | Waarde                                                                 |
|----------------|------------------------------------------------------------------------|
| Item           | [GeoBRK_SaaS_Applicatie Acceptatieomgeving](https://gis.wageningen.nl/portal/home/item.html?id=6d46c061947848aba84a8bcf9e85f65e) |
| ClientID       | `hFGilRufKELYByfe`                                                     |
| Directe URL    | [Inloggen](https://acc-apps.arcgisonline.nl/geobrk/?config=eyJwb3J0YWxVcmwiOiJodHRwczovL2dpcy53YWdlbmluZ2VuLm5sL3BvcnRhbCIsImFwcElkIjoiaEZHaWxSdWZLRUxZQnlmZSJ9) |

### Productieomgeving

| Eigenschap     | Waarde                                                                 |
|----------------|------------------------------------------------------------------------|
| Item           | [GeoBRK_SaaS_Applicatie Productieomgeving](https://gis.wageningen.nl/portal/home/item.html?id=728666400cd64060897e8f1e21b833b4) |
| ClientID       | `Rw51Jd0pBFHEirOo`                                                     |
| Directe URL    | [Inloggen](https://apps.arcgisonline.nl/geobrk/?config=eyJwb3J0YWxVcmwiOiJodHRwczovL2dpcy53YWdlbmluZ2VuLm5sL3BvcnRhbCIsImFwcElkIjoiaFpTWUVtZHNMSk1wSG55biJ9) |

---

## Configuratieparameters

```json
{
  "webmapId": "0a9e2f55241d436094c510bd5ebc0889",
  "polygonLayerName": "Perceel onroerende zaak",
  "gerechtigdeLayerName": "Gerechtigde",
  "beperkingenLayerName": "Publiekrechtelijke beperking",
  "zoekAdresTableName": "Zoekadres",
  "adresPerceelTableName": "Adres perceel",
  "selectionColor": "#4052ad",
  "selectionColorOpacity": 0.5,
  "highlightColor": "#71f086",
  "highlightColorOpacity": 0.3,
  "brkVersion": "3.0"
}

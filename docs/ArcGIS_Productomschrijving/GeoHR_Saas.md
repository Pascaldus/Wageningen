---
title: GeoHR SaaS opbouw
parent: Productomschrijving
grand_parent: ArcGIS
layout: default
nav_order: 5
has_toc: false
---

# GeoHR SaaS Gemeente Wageningen

Op het GIS-portaal van de gemeente Wageningen zijn verschillende lagen als Feature Layer opgenomen. Deze zijn toegevoegd via de SaaS-URL:

```
https://daas.arcgisonline.nl/arcgis/rest/services/g_wageningen/HR/MapServer
```

De volgende lagen zijn opgenomen: `/32` en `/33`.

Deze lagen zijn beveiligd met een gebruikersnaam en wachtwoord en gedeeld met de groep **CV Basisregistraties** (GeoHR en GeoBRK). De inloggegevens zijn opgeslagen in het service-item, zodat gebruikers deze niet handmatig hoeven in te voeren.

| Gegevens     | Waarde                          |
|--------------|----------------------------------|
| Gebruikersnaam | `G_Wageningen`                 |
| Wachtwoord     | Zie KeePass of vraag Pascal van de Laak |

---

## Feature Layers

| Naam                                                        | Link                                                                 |
|-------------------------------------------------------------|----------------------------------------------------------------------|
| GeoHR_SaaS_Vestiging (Maatschappelijke activiteit)          | [Item](https://gis.wageningen.nl/portal/home/item.html?id=6cd14a07cac042b58886368d7b7fea31) |
| GeoHR_SaaS_Vestiging (Maatschappelijke activiteit) vlak     | [Item](https://gis.wageningen.nl/portal/home/item.html?id=4882bf44204f46dfaa96706d11eb7b25) |

Deze lagen worden niet gebruikt in GeoHR SaaS en zijn bedoeld voor analyses in ArcGIS Pro.

---

## Service Layer

Volgens dezelfde methode is de volgende laag opgenomen:

| Naam                        | Link                                                                 |
|-----------------------------|----------------------------------------------------------------------|
| GeoHR_SaaS_Service_Compleet | [Item](https://gis.wageningen.nl/portal/home/item.html?id=a7dd8807cd7c4976b9b84cbcf87203f2) |

---

## WebMap

**GeoHR_SaaS_WM_Basis**  
[Item](https://gis.wageningen.nl/portal/home/item.html?id=6dd2721042694b5aa74ecdb8e331ecbd)

---

## Applicaties

### Acceptatieomgeving

| Eigenschap     | Waarde                                                                 |
|----------------|------------------------------------------------------------------------|
| Item           | [GeoHR_SaaS_Applicatie Acceptatieomgeving](https://gis.wageningen.nl/portal/home/item.html?id=c643d7c977b94e0292ed61ee9dfe0e9e) |
| ClientID       | `cnTP4ie8OgAfRQgz`                                                     |
| Directe URL    | [Inloggen](https://acc-apps.arcgisonline.nl/geohr/?config=eyJwb3J0YWxVcmwiOiJodHRwczovL2dpcy53YWdlbmluZ2VuLm5sL3BvcnRhbCIsImFwcElkIjoiY25UUDRpZThPZ0FmUlFneiJ9) |

### Productieomgeving

| Eigenschap     | Waarde                                                                 |
|----------------|------------------------------------------------------------------------|
| Item           | [GeoHR_SaaS_Applicatie Productieomgeving](https://gis.wageningen.nl/portal/home/item.html?id=a6969313ecb943158596da6911c3230b) |
| ClientID       | `oFXLJ7AQggQFTjgv`                                                     |
| Directe URL    | [Inloggen](https://apps.arcgisonline.nl/geohr/?config=eyJwb3J0YWxVcmwiOiJodHRwczovL2dpcy53YWdlbmluZ2VuLm5sL3BvcnRhbCIsImFwcElkIjoib0ZYTEo3QVFnZ1FGVGpndiJ9) |

---

## Configuratieparameters

```json
{
  "webmapId": "6dd2721042694b5aa74ecdb8e331ecbd",
  "pointsLayerName": "Vestiging (Maatschappelijke activiteit) punt",
  "polygonLayerName": "Vestiging (Maatschappelijke activiteit) vlak",
  "selectionColor": "#FF0000",
  "highlightColor": "#FF0000",
  "hrVersion": "2.0"
}
```

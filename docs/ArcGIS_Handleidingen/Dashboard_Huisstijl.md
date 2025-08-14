---
title: Dashboard (kaart) maken
parent: Handleidingen
grand_parent: ArcGIS
layout: default
nav_order: 1
has_toc: false
---

# Handleiding opmaken kaartapplicatie

## 1. Template webmap openen

- **Intern portaal:**  
  [Template webmap](https://gis.wageningen.nl/portal/home/item.html?id=c0d1021541044bb5a9ec000ed418904d)  
- **Extern portaal:**  
  [Template webmap](https://wageningen.maps.arcgis.com/home/item.html?id=75f78d75b15c4bf5a9d1c1ef41064b1a)

**Stappen:**  
1. Klik op **Open in Map Viewer**.  
2. Klik op **Opslaan als**.  
3. Geef de webmap de naam `WM_Onderwerp`.  
4. Plaats de webmap in de map **Kaartapplicaties**.  
5. Voeg de lagen toe die nodig zijn voor de kaartapplicatie.

### Lagen van de webmap vinden

1. Open het Excel-bestand met de werkvoorraad.  
2. Kopieer de ID achter `index.html?id=` in de WebApp‑URL, bijvoorbeeld:  
   [https://wageningen.maps.arcgis.com/apps/webappviewer/index.html?id=9304536403b04f2390637eb2aac92199](https://wageningen.maps.arcgis.com/apps/webappviewer/index.html?id=9304536403b04f2390637eb2aac92199)  
   → De ID is: `9304536403b04f2390637eb2aac92199`.  
3. Ga naar het externe geoportaal: [https://wageningen.maps.arcgis.com/](https://wageningen.maps.arcgis.com/) en klik op **Content**. Open vervolgens een willekeurige laag.  
4. Vervang in de adresbalk de cijfers achter `id=` met de eerder gekopieerde ID.  
5. Je komt nu op de pagina van de **WebApp**. Klik op **Applicatie bewerken**.  
6. Ga naar het tabblad **Kaart**.  
7. Klik op **Meer details...**  
8. Je komt nu op de pagina van de **webmap**.  
9. Klik met de **middelste muisknop** op de lagen onder **Lagen** (opent in nieuw tabblad).  
10. De **Feature Layers** worden geopend; hier zie je de originele laagnamen (bijvoorbeeld `AfgekoppeldeGebieden`).  
11. Neem deze lagen op in de **nieuwe webmap**.  
12. Open de oude webmap naast de nieuwe om waar nodig de **symbologie** over te nemen.

{: .note }  
> Houd de oude en nieuwe webmap in twee tabbladen of vensters naast elkaar voor snel vergelijken en kopiëren.

---

## 2. Template webapp openen

- **Intern portaal:**  
  [Template webapp](https://gis.wageningen.nl/portal/home/item.html?id=0b77fdc492bf4537ad1c9863aab10c47)  
- **Extern portaal:**  
  [Template webapp](https://wageningen.maps.arcgis.com/home/item.html?id=d77c1c44d7c14b15b9e6e74f61f314c5)

**Voorbeeld applicatie:**  
[Leegstand Viewer](https://gis.wageningen.nl/portal/home/item.html?id=86e9945bb8434db5ad2785435562561b)

**Stappen:**  
1. Klik op **Dashboard bewerken**.  
2. Klik op **Opslaan als**.  
3. Geef de applicatie de naam `WA_Onderwerp`.  
4. Plaats de applicatie in de map **Kaartapplicaties**.

---

### 3. Kaart aanpassen

1. Verwijder de kaart in het midden.  
2. Klik op het **+ icoontje**.  
3. Druk in het midden opnieuw op het **+ icoontje** en selecteer **Kaart**.  
4. Kies de eerder aangemaakte `WM_Onderwerp`.  

#### Instellingen voor de kaart

- Onder **Instellingen**:  
  - Meting: **Aan**  
  - Zoeken: **Aan**  
  - Laagzichtbaarheid: **Aan**  
  - Basiskaart‑wisselaar: **Aan**  

- Onder **Algemeen**:  
  - Bijschrift top: **Onderwerpkaart** *(bold, Kop 2, gecentreerd)*  
    - Voorbeelden: *Afkoppelingsgebieden*, *Parkeren*  
  - Tekstkleur: `#102652`  
  - Voorgrondkleur: `#F5F5F5`  

5. Klik opnieuw op het **+ icoontje**, daarna het **plusje rechts**.  
6. Selecteer **Kaartlegenda**.  
7. Bij **Bijschrift top** vul je in: **Legenda** *(bold, Kop 2, gecentreerd)*.  
8. Tekstkleur: `#102652`.  
9. Voorgrondkleur: `#F5F5F5`.  
10. Schuif de balken zodat de kaart **80% breed** is voor de overzichtskaart.  
11. Configureer de categorieselector naar wens (kijk ter inspiratie naar voorbeeldapplicaties).  


### Standaard wijkselectie (categorieselector)

1. Open de categorieselector: **drie puntjes → tandwieltje**.  
2. Onder **Gegevens**:  
  - Instellingen: **Objecten**  
  - Kaartlaag: **CBS Wijk actueel**  
  - Template: **`{field/statnaam}`**  
3. Onder **Keuzeschakelaar**:  
  - Label: **Selecteer wijken**  
  - Presentatiemodus: **Inline**  
  - Weergavetype: **Lijst**  
  - Selectie: **Meerdere**  
  - Maximumhoogte: **Geen**  
4. Onder **Acties**:  
  - Filteren:  
    - Vink de relevante lagen aan, methode: **Spatial** (CBS Gemeente actueel uitgevinkt laten) 
    - Voor **CBS Wijk actueel**: vink **Alleen renderen indien gefilterd** aan  
  - Zoomen:  
    - Vink de **webmap** aan

---

## 4. Notities

- In het interne portaal kun je de opmaak van de zijbalk-elementen aanpassen in het **titelveld**.  
- In ArcGIS Online maak je de titel op via het veld **Bijschrift top**, omdat de zijbalk-titeloptie daar ontbreekt.

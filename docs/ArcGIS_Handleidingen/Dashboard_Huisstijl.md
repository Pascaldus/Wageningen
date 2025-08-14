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
  https://gis.wageningen.nl/portal/home/item.html?id=c0d1021541044bb5a9ec000ed418904d  
- **Extern portaal:**  
  https://wageningen.maps.arcgis.com/home/item.html?id=75f78d75b15c4bf5a9d1c1ef41064b1a

**Stappen:**  
1. Klik op **Open in Map Viewer**.  
2. Klik op **Opslaan als**.  
3. Geef de webmap de naam `WM_Onderwerp`.  
4. Plaats de webmap in de map **Kaartapplicaties**.  
5. Voeg de lagen toe die nodig zijn voor de kaartapplicatie.

### Lagen van de webmap vinden

1. Open het Excel-bestand met de werkvoorraad.  
2. Kopieer de ID achter `index.html?id=` in de WebApp-URL, bijvoorbeeld:  
   `https://wageningen.maps.arcgis.com/apps/webappviewer/index.html?id=9304536403b04f2390637eb2aac92199`  
   → De ID is: `9304536403b04f2390637eb2aac92199`.  
3. Ga naar het externe geoportaal: `https://wageningen.maps.arcgis.com/`, klik op **Content** en open een willekeurige laag.  
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
> **Tip**  
> Houd de oude en nieuwe webmap in twee tabbladen of vensters naast elkaar voor snel vergelijken en kopiëren.

---

## 2. Template webapp openen

- **Intern portaal:**  
  https://gis.wageningen.nl/portal/home/item.html?id=0b77fdc492bf4537ad1c9863aab10c47  
- **Extern portaal:**  
  https://wageningen.maps.arcgis.com/home/item.html?id=d77c1c44d7c14b15b9e6e74f61f314c5

**Voorbeeld applicatie:**  
https://gis.wageningen.nl/portal/home/item.html?id=86e9945bb8434db5ad2785435562561b

**Stappen:**  
1. Klik op **Dashboard bewerken**.  
2. Klik op **Opslaan als**.  
3. Geef de applicatie de naam `WA_Onderwerp`.  
4. Plaats de applicatie in de map **Kaartapplicaties**.

{: .warning } 
> **Let op**  
> Het is niet mogelijk om de kaart te vervangen; maak een nieuw kaartelement aan.

---

## 3. Kaart aanpassen

1. Verwijder de kaart in het midden.  
2. Klik op het **+ icoontje**.  
3. Druk in het midden opnieuw op het **+ icoontje** en selecteer **Kaart**.  
4. Kies de eerder aangemaakte `WM_Onderwerp`.  
5. Ga naar de instellingen van de kaart en open **Bijschrift top**.  
6. Vul in: **Onderwerpkaart** (bold, Kop 2, gecentreerd). Voorbeeld: *Afkoppelingsgebieden*, *Parkeren*.  
7. Stel tekstkleur in op `#102652`.  
8. Stel voorgrondkleur in op `#F5F5F5`.  
9. Klik opnieuw op het

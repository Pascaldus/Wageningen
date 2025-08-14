---
title: Metadatabeheer
parent: Werkafspraken
layout: default
nav_order: 3
has_toc: false
---

Om metadata te beheren willen wij van alle datasets het volgende weten:

| Veldnaam               | Beschrijving                                                                 |
|------------------------|-------------------------------------------------------------------------------|
| Dataset                | De naam van de dataset                                                       |
| Actualisatie_Periode   | Hoe vaak de dataset wordt bijgewerkt: Dagelijks, Wekelijks, Maandelijks, Kwartaal, Half jaar of Jaar |
| Actualisatie_Datum     | Wanneer de dataset voor het laatst is bijgewerkt                             |
| Actualisatie_Soort     | Automatisch of Handmatig                                                     |
| Beheerder_Brondata     | Naam collega (of leverancier) van de brondata                                |
| Beheerder_actualisatie | Wie verantwoordelijk is voor de actualisatie                                  |
| URL_data               | Eventuele link naar applicatie/dashboard                                      |
| URL_FME                | Link naar FME script                                                          |
| Opmerkingen            | Opmerkingen                                                                   |
| Locatie_Dataset1       | Waar het script data wegschrijft                                              |
| Locatie_Dataset2       | Waar het script data wegschrijft                                              |
| Locatie_Dataset3       | Waar het script data wegschrijft                                              |
| Locatie_Dataset4       | Waar het script data wegschrijft                                              |
| Actueel                | Ja/Nee (wordt door script ingevuld)                                           |
| Telaat_dagen           | Wordt door script ingevuld                                                    |
| Script_nummer          | Kies een opvolgend scriptnummer                                               |

## Werkwijze

Om metadata bij te houden zijn er twee dingen nodig:

### 1) Toevoegen data aan MasterMetadata

- Open **ArcGIS Pro** en maak verbinding met de database **FME@PGEO**.
- Open de tabel `FME.ACT_MasterMetadata`.
- Vul de velden in conform bovenstaande tabel (inclusief alle Locatie_Dataset-velden).
- Vergeet niet een uniek en opvolgend **Script_nummer** mee te geven.

> Tip: hanteer een vaste naamgevingsconventie voor datasets en scriptnummers, zodat filtering en automatische rapportages betrouwbaar blijven.

---

### 2) Toevoegen script aan MasterMetadata

Om te zorgen dat **Actualisatie_Datum**, **Actueel** en **Telaat_dagen** automatisch gevuld worden en de scripts worden meegenomen in de automatische mailing, moet een timestamp-logging worden toegevoegd aan het FME-script.

1. Open **FME Form** (Workbench).
2. Gebruik de functie **Download from FME Flow** om een bestaand geplande script te downloaden.
3. Selecteer in dat workspace het blok **Metadata Timestamp**.
4. Kopieer de selectie met `Ctrl+C`.

![Selecteer het blok 'Metadata Timestamp' in FME Workspace](assets/images/Metadata_Timestamp.png)

5. Open je huidige script en plak de selectie met `Ctrl+V`.
6. Pas de instellingen van de reader aan:
   - Ga naar de **WHERE Clause** en wijzig het **Script_nummer** naar het scriptnummer dat je eerder in stap 1 hebt ingevuld in `FME.ACT_MasterMetadata`.

![WHERE Clause met aangepast Script_nummer in FME Reader](assets/images/Metadata_scriptnummer.png)

7. Verbind het timestamp-blok logisch in de workflow:
   - Plaats het ná de schrijvers (writers) die de dataset wegschrijven.
   - Zorg dat de juiste attributen worden ingevuld richting `FME.ACT_MasterMetadata`
     (minimaal: `Script_nummer`, `Actualisatie_Datum`, `Actueel` en `Telaat_dagen`).
8. Sla het script op.
9. Publiceer het script naar FME Flow (indien van toepassing) en voeg het toe aan de juiste schedule.

---

> Let op:
> - Controleer in de timestamp-component de databaseverbinding en veldnamen (moeten overeenkomen met `FME.ACT_MasterMetadata`).
> - Controleer dat het script schrijft met exact hetzelfde **Script_nummer** als in de tabel.
> - Test handmatig een run en verifieer in `FME.ACT_MasterMetadata` dat de velden correct zijn bijgewerkt.


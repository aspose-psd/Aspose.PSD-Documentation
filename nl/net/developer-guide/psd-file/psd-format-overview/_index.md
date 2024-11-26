---
title: Overzicht van PSD-indeling
type: docs
weight: 60
url: /nl/net/psd-indeling-overzicht/
---

## **Beschrijving**
PSD, Photoshop-document, vertegenwoordigt het eigen bestandsformaat van Adobe Photoshop dat wordt gebruikt voor grafisch ontwerp en ontwikkeling.
## **Bestandsindelingspecificaties**
Gegevens in een PSD-bestand worden opgeslagen in de big-endian byte-volgorde. Dit houdt in dat korte en lange integers worden omgewisseld bij het lezen of schrijven op het Windows-platform. Het Photoshop-bestandsformaat is opgedeeld in vijf grote delen. Het heeft vele lengte-aanduidingen die kunnen worden gebruikt om van de ene sectie naar de volgende te gaan. De lengte-aanduidingen zijn meestal gevuld met bytes om naar het dichtstbijzijnde interval van 2 of 4 bytes af te ronden. De vijf grote delen zijn:

- Bestandshoofd
- Kleurmodusgegevens
- Afbeeldingsbronnen
- Laag- en maskerinformatie
- Afbeeldingsgegevens

Voor conformiteit moeten gegevens worden geschreven naar al deze velden in de sectie, omdat Photoshop mogelijk probeert de hele sectie te lezen. Dit impliceert ook dat nullen moeten worden geschreven naar overgeslagen velden bij het schrijven naar een bestand. Het lengteveld in de lengte-begrensde secties moet worden gebruikt om te beslissen wanneer te stoppen met lezen. In de meeste gevallen geeft het lengteveld het aantal bytes aan, geen records, die volgen. De volgende punten moeten worden onthouden bij het lezen van een bestand.

- De waarden in de "Lengte"-kolom in alle tabellen zijn in bytes.
- Alle waarden gedefinieerd als Unicode-tekenreeks bestaan uit:
- Een 4-byte lengteveld dat het aantal karakters in de reeks vertegenwoordigt (geen bytes).
- De reeks Unicode-waarden, twee bytes per karakter.
## **Kenmerken van de indeling**
PSD-bestanden kunnen afbeeldingslagen, aanpassingslagen, laagmaskers, annotaties, bestandsinformatie, trefwoorden en andere specifieke elementen van Photoshop bevatten. Photoshop-bestanden hebben de standaardextensie als.PSD en hebben een maximale hoogte en breedte van 30.000 pixels, en een lengtelimiet van twee gigabytes.
## **Hoe kan het worden gebruikt**
1. Een instrument voor PSD-slicing.
1. [PSD converteren](/psd/nl/net/psd-afbeelding-naar-rasterindeling-omzetten/) naar HTML
1. Het gebruik van [PSD als een sjabloon](/nl/net/het-gebruik-van-psd-bestanden-als-sjablonen-voor-geautomatiseerde-visitekaartjes/) voor e-mail
1. PSD naar specifieke CMS-HTML
1. Identikit in PSD-bestand (Politie tekening)
1. Maak pseudo-3D-voorbeeldafbeeldingen met behulp van slimme objecten voor producten zoals flessen, bekers, T-shirts, enz.
1. Snel bewerken van PSD: Auto-toon, Presets, Slim object, Tekstlaagafbeelding Uitsnijding

En nog veel meer. Als je iets geweldigs hebt gemaakt met Aspose.PSD, deel dan alsjeblieft jouw casestudy met ons via [Aspose Forums](https://forum.aspose.com/).

Meer voorbeelden kunt u leren van:

- [Casestudies](https://downloads.aspose.com/corporate/case-studies/aspose.psd/)
- [Showcases](/nl/net/showcases-html/)

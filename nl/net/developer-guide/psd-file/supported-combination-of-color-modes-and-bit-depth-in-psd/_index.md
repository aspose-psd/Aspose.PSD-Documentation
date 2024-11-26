---
title: Ondersteunde combinatie van Kleurmodi en Bitdiepte in PSD
type: docs
weight: 80
url: /nl/ondersteunde-combinatie-van-kleurmodi-en-bitdiepte-in-psd/
---

## **Beschrijving**
Aspose.PSD ondersteunt het openen van PSD-bestanden met elke combinatie van kleurmodus en bitdieptes in Adobe Photoshop PSD-bestanden. U kunt dergelijke bestanden openen en de Low-Level API gebruiken om de inhoud van het bestand te wijzigen. Maar voor sommige minder populaire combinaties kunnen specifieke problemen optreden, waarvan sommige gerelateerd zijn aan de beperkingen van de kleurmodi.

## **Ondersteunde exportcombinatie van Kleurmodi en Bitdiepte in PSD in de alleen-lezen modus**

| |Bitmap|Grijstint|Geïndexeerd|RGB|CMYK|Multichannel|Duotoon|Lab|
| :- | :- | :- | :- | :- | :- | :- | :- | :- |
|Diepte 1|Ja[](https://issue.kharkov.dynabic.com/issues/PSDNET-283)|-|-|-|-|-|-|-|
|Diepte 8|-|Ja|Ja|Ja|Ja|Nee Q3-Q4|Nee Q3-Q4|Ja[](https://issue.kharkov.dynabic.com/issues/PSDNET-290)|
|Diepte 16|-|Ja|-|Ja|Ja|-[](https://issue.kharkov.dynabic.com/issues/PSDNET-287)|-|Nee (Q3-Q4)|
|Diepte 32|-|Ja*[](https://issue.kharkov.dynabic.com/issues/PSDNET-125)|-|Ja*|-[](https://issue.kharkov.dynabic.com/issues/PSDNET-285)|-[](https://issue.kharkov.dynabic.com/issues/PSDNET-288)|-|-|
\* Kleine problemen in sommige gevallen

## **Ondersteunde exportcombinatie van Kleurmodi en Bitdiepte in PSD in de bewerkbare modus**

| |Bitmap|Grijstint|Geïndexeerd|RGB|CMYK|Multichannel|Duotoon|Lab|
| :- | :- | :- | :- | :- | :- | :- | :- | :- |
|Diepte 1|Ja|-|-|-|-|-|-|-|
|Diepte 8|-|Ja|Nee|Ja|Ja|Nee Q3-Q4|Nee Q3-Q4|Ja*|
|Diepte 16|-|Ja|-|Ja|Ja*|-|-|Nee (Q3-Q4)|
|Diepte 32|-|Nee (Q3-Q4)|-|Nee (Q3-Q4)|-|-|-|-|
\* Kleine problemen in sommige gevallen

Als u ondersteuning nodig heeft voor een specifieke combinatie van kleurmodus / bitdiepte, kunt u posten op [Aspose Forums](https://forum.aspose.com/c/psd)

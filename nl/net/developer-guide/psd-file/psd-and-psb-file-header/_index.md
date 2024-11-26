---
title: PSD- en PSB-bestandkoptekst
type: docs
weight: 40
url: /nl/net/psd-en-psb-bestandkoptekst/
---

## **Beschrijving**
De Adobe Photoshop-bestandskop bevat informatie over de versie van het bestand (1 voor PSD en 2 voor PSB), het aantal kanalen, de kleurmodus en de bitdiepte.

U kunt leren welke combinaties van kleurmodus en bitdiepte worden ondersteund door Aspose.PSD in het gerelateerde artikel.

De bestandskop bevat de basiskenmerken van het beeld.

|**Lengte**|**Beschrijving**|
| :- | :- |
|4|Handtekening: altijd gelijk aan *"8BPS"*|
|2|[PSD-versie](https://reference.aspose.com/psd/nl/aspose.psd.fileformats.psd/fileformatversion): altijd gelijk aan 1 voor PSD-bestanden en 2 voor PSB-bestanden. Aspose.PSD kan een versie van het bestandsformaat detecteren en correct lezen.|
|6|Gereserveerd: moet nul zijn.|
|2|Het aantal kanalen in het beeld, inclusief eventuele alfakanalen. De ondersteunde reeks is 1 tot 56.|
|4|De hoogte van het beeld in pixels. De ondersteunde reeks is 1 tot 30.000. PSB-bestanden ondersteunen hoogtes tot 300.000 pixels. PSB-bestanden worden ook ondersteund door Aspose.PSD.|
|4|De breedte van het beeld in pixels. De ondersteunde reeks is 1 tot 30.000. PSB-bestanden ondersteunen breedtes tot 300.000 pixels. Batchverwerking van grote PSD/PSB-bestanden wordt ook ondersteund door Aspose.PSD.|
|2|Diepte: het aantal bits per kanaal. Ondersteunde waarden zijn 1, 8, 16 en 32. Maar niet elke kleurmodus werkt met elke diepte.|
|2|De [PSD-kleurmodus](https://reference.aspose.com/psd/nl/com.aspose.psd.fileformats.psd/ColorModes) van het bestand. Ondersteunde waarden zijn: Bitmap = 0; Grayscale = 1; Indexed = 2; RGB = 3; CMYK = 4; Multichannel = 7; Duotoon = 8; Lab = 9.|
U kunt onze [PSD-API-referentie](https://reference.aspose.com/psd) hiervoor raadplegen.

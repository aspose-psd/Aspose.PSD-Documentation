---
title: Unterstützte Kombination von Farbmodi und Bit-Tiefe in PSD
type: docs
weight: 80
url: /de/net/unterstutzte-kombination-von-farbmodi-und-bit-tiefe-in-psd/
---

## **Beschreibung**
Aspose.PSD unterstützt das Öffnen von PSD-Dateien mit beliebigen Kombinationen von Farbmodus und Bit-Tiefen in Adobe Photoshop PSD-Dateien. Sie können solche Dateien öffnen und die Low-Level-API verwenden, um den Inhalt der Datei zu ändern. Für einige weniger verbreitete Kombinationen können spezifische Probleme auftreten, einige davon in Bezug auf Farbmodusbeschränkungen.

## **Unterstützte Exportkombination von Farbmodus und Bit-Tiefe in PSD im Nur-Lese-Modus**

| |Bitmap|Graustufen|Indiziert|RGB|CMYK|Multikanal|Duotone|Lab|
| :- | :- | :- | :- | :- | :- | :- | :- | :- |
|Tiefe 1|Ja[](https://issue.kharkov.dynabic.com/issues/PSDNET-283)|-|-|-|-|-|-|-|
|Tiefe 8|-|Ja|Ja|Ja|Ja|Nein Q3-Q4|Nein Q3-Q4|Ja[](https://issue.kharkov.dynabic.com/issues/PSDNET-290)|
|Tiefe 16|-|Ja|-|Ja|Ja|-[](https://issue.kharkov.dynabic.com/issues/PSDNET-287)|-|Nein (Q3-Q4)|
|Tiefe 32|-|Ja*[](https://issue.kharkov.dynabic.com/issues/PSDNET-125)|-|Ja*|-[](https://issue.kharkov.dynabic.com/issues/PSDNET-285)|-[](https://issue.kharkov.dynabic.com/issues/PSDNET-288)|-|-|
\* Geringfügige Probleme in einigen Fällen

## **Unterstützte Exportkombination von Farbmodi und Bit-Tiefe in PSD im Bearbeitungsmodus**

| |Bitmap|Graustufen|Indiziert|RGB|CMYK|Multikanal|Duotone|Lab|
| :- | :- | :- | :- | :- | :- | :- | :- | :- |
|Tiefe 1|Ja|-|-|-|-|-|-|-|
|Tiefe 8|-|Ja|Nein|Ja|Ja|Nein Q3-Q4|Nein Q3-Q4|Ja*|
|Tiefe 16|-|Ja|-|Ja|Ja*|-|-|Nein (Q3-Q4)|
|Tiefe 32|-|Nein (Q3-Q4)|-|Nein (Q3-Q4)|-|-|-|-|
\* Geringfügige Probleme in einigen Fällen

Wenn Sie die Unterstützung einer bestimmten Farbmodus- / Bit-Tiefenkombination benötigen, können Sie dies im [Aspose-Forum](https://forum.aspose.com/c/psd) veröffentlichen.

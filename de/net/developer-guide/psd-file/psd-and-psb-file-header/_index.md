---
title: PSD und PSB Dateikopf
type: docs
weight: 40
url: /de/net/psd-und-psb-dateikopf/
---

## **Beschreibung**
Der Dateikopf für Adobe Photoshop enthält Informationen zur Version der Datei (1 für PSD und 2 für PSB), zur Anzahl der Kanäle, zum Farbmodus und zur Bittiefe.

Sie können die von Aspose.PSD unterstützten Kombinationen von Farbmodus und Bittiefe aus dem entsprechenden Artikel lernen.

Der Dateikopf enthält die grundlegenden Eigenschaften des Bildes.

|**Länge**|**Beschreibung**|
| :- | :- |
|4|Signatur: immer gleich *„8BPS“*|
|2|[PSD Version](https://reference.aspose.com/psd/net/aspose.psd.fileformats.psd/fileformatversion): immer gleich 1 für PSD-Dateien und 2 für PSB-Dateien. Aspose.PSD kann eine Version des Dateiformats erkennen und korrekt lesen.|
|6|Reserviert: muss Null sein.|
|2|Die Anzahl der Kanäle im Bild, einschließlich aller Alphakanäle. Der unterstützte Bereich liegt bei 1 bis 56.|
|4|Die Höhe des Bildes in Pixeln. Der unterstützte Bereich liegt bei 1 bis 30.000. PSB-Dateien unterstützen eine Höhe von bis zu 300.000 Pixeln. PSB-Dateien werden auch von Aspose.PSD unterstützt.|
|4|Die Breite des Bildes in Pixeln. Der unterstützte Bereich liegt bei 1 bis 30.000. PSB-Dateien unterstützen eine Breite von bis zu 300.000 Pixeln. Die Stapelverarbeitung großer PSD/PSB-Dateien wird ebenfalls von Aspose.PSD unterstützt.|
|2|Tiefe: die Anzahl der Bits pro Kanal. Unterstützte Werte sind 1, 8, 16 und 32. Aber nicht jeder Farbmodus funktioniert mit jeder Tiefe.|
|2|Der [PSD-Farbmodus](https://reference.aspose.com/psd/java/com.aspose.psd.fileformats.psd/ColorModes) der Datei. Unterstützte Werte sind: Bitmap = 0; Graustufen = 1; Indiziert = 2; RGB = 3; CMYK = 4; Mehrkanal = 7; Duoton = 8; Lab = 9.|
Weitere Informationen finden Sie in unserer [PSD-API-Referenz](https://reference.aspose.com/psd).

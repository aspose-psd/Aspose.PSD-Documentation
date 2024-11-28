---
title: Intelligente Filtermanipulation in Aspose.PSD für С#
weight: 100
type: docs
description: Beispiele zur Verwendung von Smart Filtern in PSD-Dateien
keywords: [smart filter, add noise, gauss blur, schärfen, filter, psd filter, psd api, C#, csharp, code-beispiel]
url: /de/net/smart-filters/
---

## Überblick

Es gibt drei Möglichkeiten, intelligente Filter in Aspose.PSD für C# anzuwenden.

### Direktes Anwenden des Filters

Dieses Beispiel zeigt, wie intelligente Filter direkt in Aspose.PSD für C# angewendet werden können.

Zuerst wird die Quell-PSD-Datei, die Ausgabedatei für das Originalbild und die Ausgabedatei für das aktualisierte Bild angegeben.

Anschließend wird das PSD-Bild mithilfe der Methode `Image.Load` geladen und in ein `PsdImage`-Objekt umgewandelt.

Speichern Sie das Originalbild mithilfe der Methode `Save` mit dem angegebenen Ausgabedateinamen.

Erstellen Sie ein `SharpenSmartFilter`-Objekt, das den anzuwendenden intelligenten Filter darstellt.

Rufen Sie die reguläre Ebene aus dem PSD-Bild über `psdImage.Layers[1]` ab.

Wenden Sie den `sharpenFilter` dreimal in einer Schleife auf die reguläre Ebene an.

Speichern Sie schließlich das aktualisierte Bild mithilfe der Methode `Save` mit dem angegebenen Ausgabedateinamen.

Dieser Code zeigt, wie intelligente Filter direkt in Aspose.PSD für C# angewendet werden können. Durch Verwendung der entsprechenden Filterobjekte und deren Anwendung auf die gewünschten Ebenen können Sie die gewünschten Effekte auf Ihren Bildern erzielen.

{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "DirectlyApplySmartFilter-DirectlyApplySmartFilter.cs" >}}

### Manipulation von Smart Filtern in Smartobjekten

Dieses Beispiel zeigt, wie Smart Filter in Smartobjekten manipuliert werden können.

Zuerst wird die Quell-PSD-Datei, die Ausgabedatei für das Originalbild und die Ausgabedatei für das aktualisierte Bild angegeben.

Laden Sie das PSD-Bild mithilfe der Methode `Image.Load` und wandeln Sie es in ein `PsdImage`-Objekt um.

Speichern Sie das Originalbild mithilfe der Methode `Save` mit dem angegebenen Ausgabedateinamen.

Wandeln Sie die zweite Ebene des PSD-Bildes in ein `SmartObjectLayer`-Objekt um.

Bearbeiten Sie die Smart Filter. Dieses Beispiel zeigt die Arbeit mit `GaussianBlurSmartFilter` und `AddNoiseSmartFilter`.

Für `GaussianBlurSmartFilter` aktualisieren Sie die Filterwerte, einschließlich Radius, Mischmodus, Deckkraft und Aktivierungszustand.

Für `AddNoiseSmartFilter` setzen Sie die Rauschverteilung auf `NoiseDistribution.UNIFORM`.

Fügen Sie neue Filterelemente zur Smartobjektebene hinzu: ein weiterer `GaussianBlurSmartFilter` und `AddNoiseSmartFilter`.

Wenden Sie die Änderungen mit der Methode `UpdateResourceValues` an.

Wenden Sie die Filter direkt auf die Ebene an und auf die Maske der Ebene mit den Methoden `Apply` bzw. `ApplyToMask`.

Speichern Sie das aktualisierte Bild mithilfe der Methode `Save` mit dem angegebenen Ausgabedateinamen.

{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "ManipulatingSmartFiltersInSmartObjects-ManipulatingSmartFiltersInSmartObjects.cs" >}}

### Anwenden von Smart Filtern auf Maskenebene

Intelligente Filter sind ein leistungsstarkes Bildbearbeitungswerkzeug, mit dem Benutzer verschiedene Filter und Effekte anwenden können. Eine interessante Technik besteht darin, sie auf Masken anzuwenden, um die Bereiche zu kontrollieren, die vom Filter beeinflusst werden.

Eine Maske ist ein Graustufenbild, das die Transparenz bestimmter Bildbereiche bestimmt und selektiv Filter, Anpassungen oder Effekte anwendet.

Wenn intelligente Filter auf Masken angewendet werden, werden sie nur auf die durch die Maske angegebenen Bereiche angewendet. Diese präzise Steuerung ermöglicht die Manipulation von Intensität und Ausdehnung des Filters.

Für weitere ausführliche Informationen und Beispiele lesen Sie die [Aspose.PSD für C# Dokumentation](https://docs.aspose.com/psd/net/).

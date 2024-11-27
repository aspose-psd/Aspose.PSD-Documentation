---
title: Aspose.PSD für Python via .NET 24.3 - Versionshinweise
type: docs
weight: 10
url: /de/net/aspose-psd-fuer-python-via-net-24-3-release-notes/
---

{{% alert color="primary" %}}

Diese Seite enthält Versionshinweise für [Aspose.PSD für Python via .NET 24.3](https://pypi.org/project/aspose-psd/)

{{% /alert %}}

| **Schlüssel** | **Zusammenfassung**                                                    | **Kategorie**|
|:-------------|:---------------------------------------------------------------------|:------------|
| PSDPYTHON-42 | [AI-Format] Reduzierung der Ladezeit großer mehrseitiger AI-Bilder    | Verbesserung |
| PSDPYTHON-45 | PSD-Datei nach der Konvertierung von 8 Bit auf 16 Bit wurde unlesbar | Fehler       |
| PSDPYTHON-46 | PSD-Datei nach der Konvertierung von 8 Bit auf 32 Bit wurde unlesbar | Fehler       |
| PSDPYTHON-47 | [AI-Format] Behebung der Kurvenrenderung im AI-Datei                 | Fehler       |



## **Änderungen an der öffentlichen API**
# **Hinzugefügte APIs:**
- Keine

# **Entfernte APIs:**
- Keine


## **Beispiele für die Verwendung:**

**PSDPYTHON-42. [AI-Format] Reduzierung der Ladezeit großer mehrseitiger AI-Bilder**

{{< highlight python >}}
   # Kein Beispiel
{{< /highlight >}}

**PSDPYTHON-45. PSD-Datei nach der Konvertierung von 8 Bit auf 16 Bit wurde unlesbar**

{{< highlight python >}}
        sourceFile = "test_smart_layer.psd"
        outputFile = "export.psd"

        with PsdImage.load(sourceFile) as psdImage8:
            psdOptions16 = PsdOptions()
            psdOptions16.channel_bits_count = 16

            psdImage8.save(outputFile, psdOptions16)

        with PsdImage.load(outputFile) as image:
            psdImage16 = cast(PsdImage, image)

            testResource = as_of(psdImage16.global_layer_resources[5], Lr16Resource)
            if testResource is not None:
                # ist in Ordnung
                pass
            else:
                raise Exception("Falsche globale Ressource, die erste Ressource sollte Lr16Resource sein")
{{< /highlight >}}

**PSDPYTHON-46. PSD-Datei nach der Konvertierung von 8 Bit auf 32 Bit wurde unlesbar**

{{< highlight python >}}
        sourceFile = "test_smart_layer.psd"
        outputFile = "export.psd"

        with PsdImage.load(sourceFile) as psdImage8:
            psdOptions32 = PsdOptions()
            psdOptions32.channel_bits_count = 32

            psdImage8.save(outputFile, psdOptions32)

        with PsdImage.load(outputFile) as image:
            psdImage32 = cast(PsdImage, image)

            testResource = as_of(psdImage32.global_layer_resources[5], Lr32Resource)
            if testResource is not None:
                # ist in Ordnung
                pass
            else:
                raise Exception("Falsche globale Ressource, die erste Ressource sollte Lr32Resource sein")
{{< /highlight >}}

**PSDPYTHON-47. [AI-Format] Behebung der Kurvenrenderung in der AI-Datei**

{{< highlight python >}}
        sourceFile = "shortCurve.ai"
        outputFilePath = "shortCurve.png"

        with AiImage.load(sourceFile) as image:
            image.save(outputFilePath, PngOptions())
{{< /highlight >}}

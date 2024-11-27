---
title: Aspose.PSD für Python via .NET 24.7 - Versionshinweise
type: docs
weight: 10
url: /de/python-net/aspose-psd-fur-python-uber-net-24-7-versionshinweise/
---

{{% alert color="primary" %}}

Diese Seite enthält Versionshinweise für [Aspose.PSD für Python via .NET 24.7](https://pypi.org/project/aspose-psd/)

{{% /alert %}}

| **Schlüssel** | **Zusammenfassung**                                                                        | **Kategorie** |
|:-------------|:----------------------------------------------------------------------------------------------|:-------------|
| PSDPYTHON-86 | Ausnahme "Bildladen fehlgeschlagen." beim Öffnen des AI-Dokuments                                | Fehler      |
| PSDPYTHON-87 | Text wird in AusgabepDF-Dateien falsch gerendert                                               | Fehler      |
| PSDPYTHON-88 | Behebung von ImageSaveException: Bildexport fehlgeschlagen für die angegebene Datei unter Linux | Fehler      |
| PSDPYTHON-89 | Behebung von Schriftartenladen bei Verwendung von Aspose.Drawing                              | Fehler      |
| PSDPYTHON-90 | 'Arithmetische Operation führte zu einem Überlauf' beim Erstellen einer Smartobjektschicht mit großem JPEG | Fehler      |
| PSDPYTHON-91 | Die AI-Datei kann nicht in eine JPG-Datei konvertiert werden                                    | Fehler      |

## **Öffentliche API-Änderungen**
# **Hinzugefügte APIs:**
- P:Aspose.PSD.FileFormats.Psd.Layers.FillSettings.NoiseGradientFillSettings.ExpansionCount
- M:Aspose.PSD.FileFormats.Psd.PsdImage.AddGradientMapAdjustmentLayer
- T:Aspose.PSD.FileFormats.Psd.Layers.AdjustmentLayers.GradientMapLayer
- P:Aspose.PSD.FileFormats.Psd.Layers.AdjustmentLayers.GradientMapLayer.GradientSettings
- P:Aspose.PSD.FileFormats.Ai.AiImage.XmpData

# **Entfernte APIs:**
- Keine

## **Beispiele zur Verwendung:**

**PSDPYTHON-86. Ausnahme "Bildladen fehlgeschlagen." beim Öffnen des AI-Dokuments**
{{< highlight python >}}
        sourceFile = self.GetFileInBaseFolder("[SA]_ID_card_template.ai")
        outputFile = self.GetFileInOutputFolder("[SA]_ID_card_template.png")

        with AiImage.load(sourceFile) as image:
            image.save(outputFile, PngOptions())
{{< /highlight >}}

**PSDPYTHON-87. Text wird in AusgabepDF-Dateien falsch gerendert**
{{< highlight python >}}
        src = self.GetFileInBaseFolder("CVFlor.psd")
        output = self.GetFileInOutputFolder("output.pdf")

        with PsdImage.load(src) as psdImage:
            saveOptions = PdfOptions()
            saveOptions.pdf_core_options = PdfCoreOptions()

            psdImage.save(output, saveOptions)
{{< /highlight >}}


**PSDPYTHON-88. Behebung von ImageSaveException: Bildexport fehlgeschlagen für die angegebene Datei unter Linux**
{{< highlight python >}}
        sourceFile = self.GetFileInBaseFolder("Bed_Roll-Sticker4_1.psd")
        outputFile = self.GetFileInOutputFolder("output.jpg")

        loadOpt = PsdLoadOptions()
        loadOpt.load_effects_resource = True
        saveOpt = JpegOptions()
        saveOpt.quality = 70
        with PsdImage.load(sourceFile, loadOpt) as psdImage:
            psdImage.save(outputFile, saveOpt)
{{< /highlight >}}


**PSDPYTHON-89. Behebung von Schriftartenladen bei Verwendung von Aspose.Drawing**
{{< highlight python >}}
        with InstalledFontCollection() as installedFonts:
            print("- Vor dem Update. Installierte Schriftartenanzahl: " + str(len(installedFonts.families)))
            print("- Aktualisieren des Schriftarten-Caches durch Versuch, den Adobe-Schriftartnamen für 'Arial' zu erhalten: ")
            FontSettings.get_adobe_font_name("Arial")
            print("- Nach dem Update. Installierte Schriftartenanzahl: " + str(len(installedFonts.families))

            assert len(installedFonts.families) > 1
{{< /highlight >}}


**PSDPYTHON-90. 'Arithmetische Operation führte zu einem Überlauf' beim Erstellen einer Smartobjektschicht mit großem JPEG**
{{< highlight python >}}
        # Behebung erfolgt, aber es gibt ein anderes Problem in Aspose.PSD für Python, das diesen Test einschränkt
        #srcFile = self.GetFileInBaseFolder("source.psd")
        #imageJpg = self.GetFileInBaseFolder("test.jpg")

        #loadOpt = PsdLoadOptions()
        #loadOpt.data_recovery_mode = DataRecoveryMode.MAXIMAL_RECOVER
        #with PsdImage.load(srcFile, loadOpt) as image:
            #with open(imageJpg, "rb", buffering=0) as stream:
                #addedLayer = SmartObjectLayer(stream)
                #addedLayer.Name = "Test Layer"
                #image.AddLayer(addedLayer)
{{< /highlight >}}


**PSDPYTHON-91. Die AI-Datei kann nicht in eine JPG-Datei konvertiert werden**
{{< highlight python >}}
        sourceFile = self.GetFileInBaseFolder("aaa.ai")
        outputFile = self.GetFileInOutputFolder("aaa.png")

        with AiImage.load(sourceFile) as image:
            image.save(outputFile, PngOptions())
{{< /highlight >}}

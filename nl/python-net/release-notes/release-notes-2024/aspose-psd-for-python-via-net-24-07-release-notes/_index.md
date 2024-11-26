---
title: Aspose.PSD voor Python via .NET 24.7 - Release-opmerkingen
type: docs
weight: 10
url: /nl/python-net/aspose-psd-voor-python-via-net-24-7-release-opmerkingen/
---

{{% alert color="primary" %}}

Deze pagina bevat release-opmerkingen voor [Aspose.PSD voor Python via .NET 24.7](https://pypi.org/project/aspose-psd/)

{{% /alert %}}

| **Sleutel**   | **Samenvatting**                                                                              | **Categorie** |
|:------------- |:-----------------------------------------------------------------------------------------------|:-------------|
| PSDPYTHON-86  | Uitzondering 'Afbeeldingsladen mislukt.' bij openen AI-document                                 | Fout         |
| PSDPYTHON-87  | Tekst verkeerd weergegeven in uitvoer-PDF-bestanden                                           | Fout         |
| PSDPYTHON-88  | Oplossing voor ImageSaveException: Afbeeldingsexport mislukt voor het opgegeven bestand op Linux | Fout         |
| PSDPYTHON-89  | Oplossing voor lettertypen laden bij gebruik van Aspose.Drawing                                | Fout         |
| PSDPYTHON-90  | 'Arithmetische bewerking resulteerde in een overflow' bij maken van slim objectlaag met grote JPEG | Fout         |
| PSDPYTHON-91  | Het AI-bestand kan niet worden geconverteerd naar een JPG-bestand                              | Fout         |

## **Wijzigingen in openbare API**
# **Toegevoegde API's:**
- P:Aspose.PSD.FileFormats.Psd.Layers.FillSettings.NoiseGradientFillSettings.ExpansionCount
- M:Aspose.PSD.FileFormats.Psd.PsdImage.AddGradientMapAdjustmentLayer
- T:Aspose.PSD.FileFormats.Psd.Layers.AdjustmentLayers.GradientMapLayer
- P:Aspose.PSD.FileFormats.Psd.Layers.AdjustmentLayers.GradientMapLayer.GradientSettings
- P:Aspose.PSD.FileFormats.Ai.AiImage.XmpData

# **Verwijderde API's:**
- Geen

## **Gebruikvoorbeelden:**

**PSDPYTHON-86. Uitzondering 'Afbeeldingsladen mislukt.' bij openen AI-document**
{{< highlight python >}}
        sourceFile = self.GetFileInBaseFolder("[SA]_ID_card_template.ai")
        outputFile = self.GetFileInOutputFolder("[SA]_ID_card_template.png")

        with AiImage.load(sourceFile) as image:
            image.save(outputFile, PngOptions())
{{< /highlight >}}

**PSDPYTHON-87. Tekst verkeerd weergegeven in uitvoer-PDF-bestanden**
{{< highlight python >}}
        src = self.GetFileInBaseFolder("CVFlor.psd")
        output = self.GetFileInOutputFolder("output.pdf")

        with PsdImage.load(src) as psdImage:
            saveOptions = PdfOptions()
            saveOptions.pdf_core_options = PdfCoreOptions()

            psdImage.save(output, saveOptions)
{{< /highlight >}}


**PSDPYTHON-88. Oplossing voor ImageSaveException: Afbeeldingsexport mislukt voor het opgegeven bestand op Linux**
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


**PSDPYTHON-89. Oplossing voor lettertypen laden bij gebruik van Aspose.Drawing**
{{< highlight python >}}
        with InstalledFontCollection() as installedFonts:
            print("- Vóór de update. Aantal geïnstalleerde lettertypen: " + str(len(installedFonts.families)))
            print("- Vernieuw de lettertypecache door te proberen de Adobe-lettertypenaam voor 'Arial' te verkrijgen: ")
            FontSettings.get_adobe_font_name("Arial")
            print("- Na de update. Aantal geïnstalleerde lettertypen: " + str(len(installedFonts.families))

            assert len(installedFonts.families) > 1
{{< /highlight >}}


**PSDPYTHON-90. 'Arithmetische bewerking resulteerde in een overflow' bij maken van slim objectlaag met grote JPEG**
{{< highlight python >}}
        # De oplossing is toegepast, maar er is een ander probleem in Aspose.PSD voor Python dat deze test beperkt
        #srcFile = self.GetFileInBaseFolder("source.psd")
        #imageJpg = self.GetFileInBaseFolder("test.jpg")

        #loadOpt = PsdLoadOptions()
        #loadOpt.data_recovery_mode = DataRecoveryMode.MAXIMAL_RECOVER
        #with PsdImage.load(srcFile, loadOpt) as image:
            #with open(imageJpg, "rb", buffering=0) as stream:
                #addedLayer = SmartObjectLayer(stream)
                #addedLayer.Name = "Testlaag"
                #image.AddLayer(addedLayer)
{{< /highlight >}}


**PSDPYTHON-91. Het AI-bestand kan niet worden geconverteerd naar een JPG-bestand**
{{< highlight python >}}
        sourceFile = self.GetFileInBaseFolder("aaa.ai")
        outputFile = self.GetFileInOutputFolder("aaa.png")

        with AiImage.load(sourceFile) as image:
            image.save(outputFile, PngOptions())
{{< /highlight >}}

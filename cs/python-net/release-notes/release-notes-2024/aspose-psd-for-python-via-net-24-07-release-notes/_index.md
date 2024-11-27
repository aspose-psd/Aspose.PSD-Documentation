---
title: "Aspose.PSD pro Python pomocí .NET 24.7 - Poznámky k vydání"
type: docs
weight: 10
url: /cs/python-net/aspose-psd-pro-python-pomoci-net-24-7-poznamky-k-vydani/
---

{{% alert color="primary" %}}

Tato stránka obsahuje poznámky k vydání pro [Aspose.PSD pro Python pomocí .NET 24.7](https://pypi.org/project/aspose-psd/)

{{% /alert %}}

| **Klíč**     | **Shrnutí**                                                                                                       | **Kategorie** |
|:-------------|:------------------------------------------------------------------------------------------------------------------|:-------------|
| PSDPYTHON-86 | Výjimka "Načítání obrázku selhalo." při otevírání dokumentu AI                                    | Chyba         |
| PSDPYTHON-87 | Text je nesprávně vykreslen výstupních souborech PDF                                                | Chyba         |
| PSDPYTHON-88 | Oprava výjimky ImageSaveException: Export obrázku selhal u daného souboru na Linuxu               | Chyba         |
| PSDPYTHON-89 | Oprava načítání písma při použití Aspose.Drawing                                                     | Chyba         |
| PSDPYTHON-90 | 'Aritmetická operace způsobila přetečení' při vytváření vrstvy smart objektu pomocí velkého JPEG | Chyba         |
| PSDPYTHON-91 | Soubor AI nelze převést na soubor JPG                                                               | Chyba         |

## **Změny ve veřejném API**
# **Přidaná API:**
- P:Aspose.PSD.FileFormats.Psd.Layers.FillSettings.NoiseGradientFillSettings.ExpansionCount
- M:Aspose.PSD.FileFormats.Psd.PsdImage.AddGradientMapAdjustmentLayer
- T:Aspose.PSD.FileFormats.Psd.Layers.AdjustmentLayers.GradientMapLayer
- P:Aspose.PSD.FileFormats.Psd.Layers.AdjustmentLayers.GradientMapLayer.GradientSettings
- P:Aspose.PSD.FileFormats.Ai.AiImage.XmpData

# **Odstraněná API:**
- Žádná

## **Příklady použití:**

**PSDPYTHON-86. Výjimka "Načítání obrázku selhalo." při otevírání dokumentu AI**
{{< highlight python >}}
        sourceFile = self.GetFileInBaseFolder("[SA]_ID_card_template.ai")
        outputFile = self.GetFileInOutputFolder("[SA]_ID_card_template.png")

        with AiImage.load(sourceFile) as image:
            image.save(outputFile, PngOptions())
{{< /highlight >}}

**PSDPYTHON-87. Text je nesprávně vykreslen výstupních souborech PDF**
{{< highlight python >}}
        src = self.GetFileInBaseFolder("CVFlor.psd")
        output = self.GetFileInOutputFolder("output.pdf")

        with PsdImage.load(src) as psdImage:
            saveOptions = PdfOptions()
            saveOptions.pdf_core_options = PdfCoreOptions()

            psdImage.save(output, saveOptions)
{{< /highlight >}}


**PSDPYTHON-88. Oprava výjimky ImageSaveException: Export obrázku selhal u daného souboru na Linuxu**
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


**PSDPYTHON-89. Oprava načítání písma při použití Aspose.Drawing**
{{< highlight python >}}
        with InstalledFontCollection() as installedFonts:
            print("- Před aktualizací. Počet nainstalovaných písem: " + str(len(installedFonts.families)))
            print("- Obnovte mezipaměť písma pokusem získat jméno písma Adobe pro 'Arial': ")
            FontSettings.get_adobe_font_name("Arial")
            print("- Po aktualizaci. Počet nainstalovaných písem: " + str(len(installedFonts.families)))

            assert len(installedFonts.families) > 1
{{< /highlight >}}


**PSDPYTHON-90. 'Aritmetická operace způsobila přetečení' při vytváření vrstvy smart objektu pomocí velkého JPEG**
{{< highlight python >}}
        # Oprava byla provedena, ale existuje další problém v Aspose.PSD pro Python, který omezuje tuto zkoušku
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


**PSDPYTHON-91. Soubor AI nelze převést na soubor JPG**
{{< highlight python >}}
        sourceFile = self.GetFileInBaseFolder("aaa.ai")
        outputFile = self.GetFileInOutputFolder("aaa.png")

        with AiImage.load(sourceFile) as image:
            image.save(outputFile, PngOptions())
{{< /highlight >}}

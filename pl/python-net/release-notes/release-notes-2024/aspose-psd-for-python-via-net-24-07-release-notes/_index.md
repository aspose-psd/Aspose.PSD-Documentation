---
title: Notatki wydania Aspose.PSD dla Python via .NET 24.7
type: docs
weight: 10
url: /pl/python-net/aspose-psd-dla-python-poprzez-net-24-7-notatki-o-wydaniu/
---

{{% alert color="primary" %}}

Ta strona zawiera notatki wydania dla [Aspose.PSD dla Python via .NET 24.7](https://pypi.org/project/aspose-psd/)

{{% /alert %}}

| **Klucz**      | **Podsumowanie**                                                                                                       | **Kategoria** |
|:-------------|:------------------------------------------------------------------------------------------------------------------|:-------------|
| PSDPYTHON-86 | Wyjątek "Błąd ładowania obrazu" podczas otwierania dokumentu AI                                          | Błąd      |
| PSDPYTHON-87 | Tekst renderowany nieprawidłowo w plikach PDF wyjściowych                                                    | Błąd      |
| PSDPYTHON-88 | Naprawiono ImageSaveException: Niepowodzenie eksportu obrazu dla podanego pliku na systemie Linux            | Błąd      |
| PSDPYTHON-89 | Naprawiono ładowanie czcionek przy użyciu Aspose.Drawing                                                    | Błąd      |
| PSDPYTHON-90 | "Operacja arytmetyczna spowodowała przepełnienie" podczas tworzenia warstwy obiektu inteligentnego z dużym plikiem JPEG | Błąd      |
| PSDPYTHON-91 | Plik AI nie może być przekonwertowany na plik JPG                                                | Błąd      |

## **Zmiany w API publicznym**
# **Dodane API:**
- P:Aspose.PSD.FileFormats.Psd.Layers.FillSettings.NoiseGradientFillSettings.ExpansionCount
- M:Aspose.PSD.FileFormats.Psd.PsdImage.AddGradientMapAdjustmentLayer
- T:Aspose.PSD.FileFormats.Psd.Layers.AdjustmentLayers.GradientMapLayer
- P:Aspose.PSD.FileFormats.Psd.Layers.AdjustmentLayers.GradientMapLayer.GradientSettings
- P:Aspose.PSD.FileFormats.Ai.AiImage.XmpData

# **Usunięte API:**
- Brak

## **Przykłady użycia:**

**PSDPYTHON-86. Wyjątek "Błąd ładowania obrazu" podczas otwierania dokumentu AI**
{{< highlight python >}}
        sourceFile = self.GetFileInBaseFolder("[SA]_ID_card_template.ai")
        outputFile = self.GetFileInOutputFolder("[SA]_ID_card_template.png")

        with AiImage.load(sourceFile) as image:
            image.save(outputFile, PngOptions())
{{< /highlight >}}

**PSDPYTHON-87. Tekst renderowany nieprawidłowo w plikach PDF wyjściowych**
{{< highlight python >}}
        src = self.GetFileInBaseFolder("CVFlor.psd")
        output = self.GetFileInOutputFolder("output.pdf")

        with PsdImage.load(src) as psdImage:
            saveOptions = PdfOptions()
            saveOptions.pdf_core_options = PdfCoreOptions()

            psdImage.save(output, saveOptions)
{{< /highlight >}}


**PSDPYTHON-88. Naprawiono ImageSaveException: Niepowodzenie eksportu obrazu dla podanego pliku na systemie Linux**
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


**PSDPYTHON-89. Naprawiono ładowanie czcionek przy użyciu Aspose.Drawing**
{{< highlight python >}}
        with InstalledFontCollection() as installedFonts:
            print("- Przed aktualizacją. Liczba zainstalowanych czcionek: " + str(len(installedFonts.families)))
            print("- Odśwież pamięć podręczną czcionek, próbując uzyskać nazwę czcionki Adobe dla 'Arial': ")
            FontSettings.get_adobe_font_name("Arial")
            print("- Po aktualizacji. Liczba zainstalowanych czcionek: " + str(len(installedFonts.families)))

            assert len(installedFonts.families) > 1
{{< /highlight >}}


**PSDPYTHON-90. "Operacja arytmetyczna spowodowała przepełnienie" podczas tworzenia warstwy obiektu inteligentnego z dużym plikiem JPEG**
{{< highlight python >}}
        # Poprawka została dokonana, ale istnieje inny problem w Aspose.PSD dla Python, który ogranicza ten test
        #srcFile = self.GetFileInBaseFolder("source.psd")
        #imageJpg = self.GetFileInBaseFolder("test.jpg")

        #loadOpt = PsdLoadOptions()
        #loadOpt.data_recovery_mode = DataRecoveryMode.MAXIMAL_RECOVER
        #with PsdImage.load(srcFile, loadOpt) as image:
            #with open(imageJpg, "rb", buffering=0) as stream:
                #addedLayer = SmartObjectLayer(stream)
                #addedLayer.Name = "Warstwa testowa"
                #image.AddLayer(addedLayer)
{{< /highlight >}}


**PSDPYTHON-91. Plik AI nie może być przekonwertowany na plik JPG**
{{< highlight python >}}
        sourceFile = self.GetFileInBaseFolder("aaa.ai")
        outputFile = self.GetFileInOutputFolder("aaa.png")

        with AiImage.load(sourceFile) as image:
            image.save(outputFile, PngOptions())
{{< /highlight >}}

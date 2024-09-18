---
title: Aspose.PSD for Python via .NET 24.7 - Release Notes
type: docs
weight: 10
url: /python-net/aspose-psd-for-python-via-net-24-7-release-notes/
---

{{% alert color="primary" %}}

This page contains release notes for [Aspose.PSD for Python via .NET 24.7](https://pypi.org/project/aspose-psd/)

{{% /alert %}}

| **Key**      | **Summary**                                                                                                       | **Category** |
|:-------------|:------------------------------------------------------------------------------------------------------------------|:-------------|
| PSDPYTHON-86 | "Image loading failed." exception when open AI document                                          | Bug      |
| PSDPYTHON-87 | Text rendered incorrectly in output PDF files                                                    | Bug      |
| PSDPYTHON-88 | Fix ImageSaveException: Image export failed for the given file on Linux                          | Bug      |
| PSDPYTHON-89 | Fix fonts loading when using Aspose.Drawing                                                      | Bug      |
| PSDPYTHON-90 | 'Arithmetic operation resulted in an overflow' when creating smart object layer using large JPEG | Bug      |
| PSDPYTHON-91 | The AI file can not be converted into a JPG file                                                 | Bug      |

## **Public API Changes**
# **Added APIs:**
- P:Aspose.PSD.FileFormats.Psd.Layers.FillSettings.NoiseGradientFillSettings.ExpansionCount
- M:Aspose.PSD.FileFormats.Psd.PsdImage.AddGradientMapAdjustmentLayer
- T:Aspose.PSD.FileFormats.Psd.Layers.AdjustmentLayers.GradientMapLayer
- P:Aspose.PSD.FileFormats.Psd.Layers.AdjustmentLayers.GradientMapLayer.GradientSettings
- P:Aspose.PSD.FileFormats.Ai.AiImage.XmpData

# **Removed APIs:**
- None

## **Usage examples:**

**PSDPYTHON-86. "Image loading failed." exception when open AI document**
{{< highlight python >}}
        sourceFile = self.GetFileInBaseFolder("[SA]_ID_card_template.ai")
        outputFile = self.GetFileInOutputFolder("[SA]_ID_card_template.png")

        with AiImage.load(sourceFile) as image:
            image.save(outputFile, PngOptions())
{{< /highlight >}}

**PSDPYTHON-87. Text rendered incorrectly in output PDF files**
{{< highlight python >}}
        src = self.GetFileInBaseFolder("CVFlor.psd")
        output = self.GetFileInOutputFolder("output.pdf")

        with PsdImage.load(src) as psdImage:
            saveOptions = PdfOptions()
            saveOptions.pdf_core_options = PdfCoreOptions()

            psdImage.save(output, saveOptions)
{{< /highlight >}}


**PSDPYTHON-88. Fix ImageSaveException: Image export failed for the given file on Linux**
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


**PSDPYTHON-89. Fix fonts loading when using Aspose.Drawing**
{{< highlight python >}}
        with InstalledFontCollection() as installedFonts:
            print("- Before update. Installed fonts count: " + str(len(installedFonts.families)))
            print("- Refresh the font cache by trying to get the Adobe font name for 'Arial': ")
            FontSettings.get_adobe_font_name("Arial")
            print("- After update. Installed fonts count: " + str(len(installedFonts.families)))

            assert len(installedFonts.families) > 1
{{< /highlight >}}


**PSDPYTHON-90. 'Arithmetic operation resulted in an overflow' when creating smart object layer using large JPEG**
{{< highlight python >}}
        # Fix is made, but there is other issue in Aspose.PSD for Python that restricts this test
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


**PSDPYTHON-91. The AI file can not be converted into a JPG file**
{{< highlight python >}}
        sourceFile = self.GetFileInBaseFolder("aaa.ai")
        outputFile = self.GetFileInOutputFolder("aaa.png")

        with AiImage.load(sourceFile) as image:
            image.save(outputFile, PngOptions())
{{< /highlight >}}
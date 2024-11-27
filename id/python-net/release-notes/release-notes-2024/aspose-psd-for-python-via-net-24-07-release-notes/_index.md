---
title: Catatan Rilis Aspose.PSD untuk Python via .NET 24.7
type: docs
weight: 10
url: /id/python-net/aspose-psd-untuk-python-via-net-24-7-catatan-rilis/
---

{{% alert color="primary" %}}

Halaman ini berisi catatan rilis untuk [Aspose.PSD untuk Python via .NET 24.7](https://pypi.org/project/aspose-psd/)

{{% /alert %}}

| **Kunci**      | **Ringkasan**                                                                                                 | **Kategori** |
|:-------------|:--------------------------------------------------------------------------------------------------------------|:-------------|
| PSDPYTHON-86 | Pengecualian "Gagal memuat gambar." saat membuka dokumen AI                       | Bug      |
| PSDPYTHON-87 | Teks dirender dengan tidak benar di file PDF output                               | Bug      |
| PSDPYTHON-88 | Perbaiki ImageSaveException: Ekspor gambar gagal untuk file yang diberikan di Linux | Bug      |
| PSDPYTHON-89 | Perbaiki muatan font saat menggunakan Aspose.Drawing                               | Bug      |
| PSDPYTHON-90 | 'Operasi aritmatika menghasilkan kelebihan' saat membuat lapisan objek pintar menggunakan JPEG besar | Bug      |
| PSDPYTHON-91 | File AI tidak dapat dikonversi menjadi file JPG                                    | Bug      |

## **Perubahan API Publik**
# **API Ditambahkan:**
- P:Aspose.PSD.FileFormats.Psd.Layers.FillSettings.NoiseGradientFillSettings.ExpansionCount
- M:Aspose.PSD.FileFormats.Psd.PsdImage.AddGradientMapAdjustmentLayer
- T:Aspose.PSD.FileFormats.Psd.Layers.AdjustmentLayers.GradientMapLayer
- P:Aspose.PSD.FileFormats.Psd.Layers.AdjustmentLayers.GradientMapLayer.GradientSettings
- P:Aspose.PSD.FileFormats.Ai.AiImage.XmpData

# **API Dihapus:**
- Tidak ada

## **Contoh Penggunaan:**

**PSDPYTHON-86. Pengecualian "Gagal memuat gambar." saat membuka dokumen AI**
{{< highlight python >}}
        sourceFile = self.GetFileInBaseFolder("[SA]_ID_card_template.ai")
        outputFile = self.GetFileInOutputFolder("[SA]_ID_card_template.png")

        with AiImage.load(sourceFile) as image:
            image.save(outputFile, PngOptions())
{{< /highlight >}}

**PSDPYTHON-87. Teks dirender dengan tidak benar di file PDF output**
{{< highlight python >}}
        src = self.GetFileInBaseFolder("CVFlor.psd")
        output = self.GetFileInOutputFolder("output.pdf")

        with PsdImage.load(src) as psdImage:
            saveOptions = PdfOptions()
            saveOptions.pdf_core_options = PdfCoreOptions()

            psdImage.save(output, saveOptions)
{{< /highlight >}}


**PSDPYTHON-88. Perbaiki ImageSaveException: Ekspor gambar gagal untuk file yang diberikan di Linux**
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


**PSDPYTHON-89. Perbaiki muatan font saat menggunakan Aspose.Drawing**
{{< highlight python >}}
        with InstalledFontCollection() as installedFonts:
            print("- Sebelum pembaruan. Jumlah font yang terpasang: " + str(len(installedFonts.families)))
            print("- Segarkan cache font dengan mencoba mendapatkan nama font Adobe untuk 'Arial': ")
            FontSettings.get_adobe_font_name("Arial")
            print("- Setelah pembaruan. Jumlah font yang terpasang: " + str(len(installedFonts.families)))

            assert len(installedFonts.families) > 1
{{< /highlight >}}


**PSDPYTHON-90. 'Operasi aritmatika menghasilkan kelebihan' saat membuat lapisan objek pintar menggunakan JPEG besar**
{{< highlight python >}}
        # Perbaikan dilakukan, tetapi ada masalah lain di Aspose.PSD untuk Python yang membatasi pengujian ini
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


**PSDPYTHON-91. File AI tidak dapat dikonversi menjadi file JPG**
{{< highlight python >}}
        sourceFile = self.GetFileInBaseFolder("aaa.ai")
        outputFile = self.GetFileInOutputFolder("aaa.png")

        with AiImage.load(sourceFile) as image:
            image.save(outputFile, PngOptions())
{{< /highlight >}}

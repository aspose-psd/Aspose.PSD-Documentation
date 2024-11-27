---
title: Catatan Rilis Aspose.PSD untuk Python via .NET 24.1
type: docs
weight: 10
url: /id/net/aspose-psd-untuk-python-via-net-24-1-catatan-rilis/
---

{{% alert color="primary" %}}

Halaman ini berisi catatan rilis untuk [Aspose.PSD untuk Python via .NET 24.1](https://pypi.org/project/aspose-psd/)

{{% /alert %}}

| **Kunci**    | **Ringkasan**                                                                                             | **Kategori** |
|:-------------|:---------------------------------------------------------------------------------------------------------|:------------|
|  PSDPYTHON-19 | [Format AI] Tambah penanganan dasar untuk gambar AI multipage                                              | Fitur       |
|  PSDPYTHON-22 | Efek Teks Distorsi tidak diterapkan pada teks                                                              | Bug         |
|  PSDPYTHON-23 | Pemrosesan masker yang tidak benar dalam file tertentu                                                    | Bug         |
|  PSDPYTHON-24 | NullReferenceException pada Aspose.PSD.FontParsing.OpenType.Serialization.OpenTypeFontInfo..ctor         | Bug         |
|  PSDPYTHON-25 | [Format AI] Memperbaiki penggunaan memori di AiExporterUtils                                              | Bug         |



## **Perubahan API Publik**
# **API Ditambahkan:**
- P:Aspose.PSD.FileFormats.Ai.AiImage.ActivePageIndex

# **API Dihapus:**
- Tidak ada


## **Contoh Penggunaan:**

**PSDPYTHON-19. [Format AI] Tambah penanganan dasar untuk gambar AI multipage**

{{< highlight python >}}
        sourceFile = self.GetFileInBaseFolder("threePages.ai")
        firstPageOutputPng = self.GetFileInOutputFolder("firstPageOutput.png")
        secondPageOutputPng = self.GetFileInOutputFolder("secondPageOutput.png")
        thirdPageOutputPng = self.GetFileInOutputFolder("thirdPageOutput.png")

        # Memuat gambar AI.
        with Image.load(sourceFile) as img:
            image = cast(AiImage, img)
            # Secara default, ActivePageIndex adalah 0.
            # Jadi jika Anda menyimpan gambar AI tanpa mengubah properti ini, halaman pertama akan dirender dan disimpan.
            image.save(firstPageOutputPng, PngOptions())

            # Ubah indeks halaman aktif menjadi halaman kedua.
            image.active_page_index = 1

            # Simpan halaman kedua dari gambar AI sebagai gambar PNG.
            image.save(secondPageOutputPng, PngOptions())

            # Ubah indeks halaman aktif menjadi halaman ketiga.
            image.active_page_index = 2

            # Simpan halaman ketiga dari gambar AI sebagai gambar PNG.
            image.save(thirdPageOutputPng, PngOptions())
{{< /highlight >}}

**PSDPYTHON-22. Efek Teks Distorsi tidak diterapkan pada teks**

{{< highlight python >}}
        sourceFile = self.GetFileInBaseFolder("text_warp.psd")
        outputFile = self.GetFileInOutputFolder("export.png")

        opt = PsdLoadOptions()
        opt.load_effects_resource = True
        opt.allow_warp_repaint = True

        pngOpt = PngOptions()
        pngOpt.compression_level = 9
        pngOpt.color_type = PngColorType.TRUECOLOR_WITH_ALPHA

        with PsdImage.load(sourceFile, opt) as img:
            img.save(outputFile, pngOpt)
{{< /highlight >}}

**PSDPYTHON-23. Pemrosesan masker yang tidak benar dalam file tertentu**

{{< highlight python >}}
        sourceFile1 = self.GetFileInBaseFolder("mask_problem.psd")
        sourceFile2 = self.GetFileInBaseFolder("puh_softLight3_1.psd")
        outputFile1 = self.GetFileInOutputFolder("mask_export.png")
        outputFile2 = self.GetFileInOutputFolder("puh_export.png")

        opt = PsdLoadOptions()
        opt.load_effects_resource = True

        pngOpt = PngOptions()
        pngOpt.compression_level = 9
        pngOpt.color_type = PngColorType.TRUECOLOR_WITH_ALPHA

        with PsdImage.load(sourceFile1, opt) as img:
            img.save(outputFile1, pngOpt)

        with PsdImage.load(sourceFile2, opt) as img:
            img.save(outputFile2, pngOpt)
{{< /highlight >}}

**PSDPYTHON-24. NullReferenceException pada Aspose.PSD.FontParsing.OpenType.Serialization.OpenTypeFontInfo..ctor**

{{< highlight python >}}
        fontsFolder = self.GetFileInBaseFolder("Fonts")
        FontSettings.set_fonts_folders([fontsFolder], True)

        inputFile = self.GetFileInBaseFolder("1.psd")
        outputFile = self.GetFileInOutputFolder("out_1855.png")
        referenceFile = self.GetFileInBaseFolder("out_1855.png")

        with PsdImage.load(inputFile) as psdImage:
            psdImage.save(outputFile, PngOptions())
{{< /highlight >}}

**PSDPYTHON-25. [Format AI] Memperbaiki penggunaan memori di AiExporterUtils**

{{< highlight python >}}
  sourceFile = self.GetFileInBaseFolder("threePages.ai")
        firstPageOutputPng = self.GetFileInOutputFolder("firstPageOutput.png")
        secondPageOutputPng = self.GetFileInOutputFolder("secondPageOutput.png")
        thirdPageOutputPng = self.GetFileInOutputFolder("thirdPageOutput.png")

        # Penggunaan Memori C# adalah 220, tetapi untuk Python kami tidak memiliki akses langsung ke aktivitas GC.
        MemoryLimit = 1500
        process = psutil.Process()
        startMemory = process.memory_info().rss
        pngOpt = PngOptions()
        # Muat gambar AI.
        with Image.load(sourceFile) as img:
            image = cast(AiImage, img)

            # Simpan halaman pertama dari gambar AI sebagai gambar PNG.
            image.save(firstPageOutputPng, pngOpt)

            # Ubah indeks halaman aktif menjadi halaman kedua.
            image.active_page_index = 1

            # Simpan halaman kedua dari gambar AI sebagai gambar PNG.
            image.save(secondPageOutputPng, pngOpt)

            # Ubah indeks halaman aktif menjadi halaman ketiga.
            image.active_page_index = 2

            # Simpan halaman ketiga dari gambar AI sebagai gambar PNG.
            image.save(thirdPageOutputPng, pngOpt)

        endMemory = process.memory_info().rss
        memoryUsed = (endMemory - startMemory) / 1024 / 1024

        if memoryUsed > MemoryLimit:
            raise Exception("Penggunaan memori terlalu besar. {} daripada {:.1f}".format(memoryUsed, MemoryLimit))
{{< /highlight >}}

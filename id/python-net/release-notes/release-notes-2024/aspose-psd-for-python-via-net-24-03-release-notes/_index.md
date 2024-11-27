---
title: Catatan Rilis Aspose.PSD for Python via .NET 24.3
type: docs
weight: 10
url: /id/net/aspose-psd-for-python-via-net-24-3-release-notes/
---

{{% alert color="primary" %}}

Halaman ini berisi catatan rilis untuk [Aspose.PSD for Python via .NET 24.3](https://pypi.org/project/aspose-psd/)

{{% /alert %}}

| **Kunci**      | **Ringkasan**                                                          | **Kategori**|
|:-------------|:---------------------------------------------------------------------|:------------|
| PSDPYTHON-42 | [Format AI] Mengurangi waktu muat gambar AI multipage besar         | Peningkatan |
| PSDPYTHON-45 | File PSD setelah dikonversi dari 8 bit ke 16 bit menjadi tidak dapat dibaca |     Bug     |
| PSDPYTHON-46 | File PSD setelah dikonversi dari 8 bit ke 32 bit menjadi tidak dapat dibaca |     Bug     |
| PSDPYTHON-47 | [Format AI] Perbaiki Rendering Kurva Pendek pada file AI              |     Bug     |



## **Perubahan API Publik**
# **API Ditambahkan:**
- Tidak ada

# **API Dihapus:**
- Tidak ada


## **Contoh Penggunaan:**

**PSDPYTHON-42. [Format AI] Mengurangi waktu muat gambar AI multipage besar**

{{< highlight python >}}
   # Tidak ada sampel
{{< /highlight >}}

**PSDPYTHON-45. File PSD setelah dikonversi dari 8 bit ke 16 bit menjadi tidak dapat dibaca**

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
                # sudah benar
                pass
            else:
                raise Exception("Sumber daya global salah, sumber daya pertama harus Lr16Resource")
{{< /highlight >}}

**PSDPYTHON-46. File PSD setelah dikonversi dari 8 bit ke 32 bit menjadi tidak dapat dibaca**


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
                # sudah benar
                pass
            else:
                raise Exception("Sumber daya global salah, sumber daya pertama harus Lr32Resource")
{{< /highlight >}}

**PSDPYTHON-47. [Format AI] Perbaiki Rendering Kurva Pendek pada file AI**

{{< highlight python >}}
        sourceFile = "shortCurve.ai"
        outputFilePath = "shortCurve.png"

        with AiImage.load(sourceFile) as image:
            image.save(outputFilePath, PngOptions())
{{< /highlight >}}

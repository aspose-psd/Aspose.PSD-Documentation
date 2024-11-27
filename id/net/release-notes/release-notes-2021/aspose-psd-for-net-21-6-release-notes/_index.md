---
title: Catatan Rilis Aspose.PSD untuk .NET 21.6
type: docs
weight: 70
url: /id/net/aspose-psd-untuk-net-21-6-catatan-rilis/
---

{{% alert color="primary" %}}

Halaman ini berisi catatan rilis untuk [Aspose.PSD untuk .NET 21.6](https://www.nuget.org/packages/Aspose.PSD/)

{{% /alert %}}

|**Kunci**|**Ringkasan**|**Kategori**|
| :- | :- | :- |
|PSDNET-546|Сlipping mask for a group does not render correctly|Kesalahan|
|PSDNET-547|Regular or vector mask for a layer group is ignored on rendering|Kesalahan|
|PSDNET-647|PSD image with disabled vector layer masks on saving enables vector masks|Kesalahan|
|PSDNET-786|Exception when creating a TextLayer with text longer than 255 characters|Kesalahan|
|PSDNET-900|Text of the Text layer can not be rendered on Linux|Peningkatan|

## **Perubahan API Publik**
# **API Ditambahkan:**
- None

# **API Dihapus:**
- None

## **Contoh Penggunaan:**

**PSDNET-546. Сlipping mask for a group does not render correctly**

{{< highlight csharp >}}
            string sourceFileName = "AppleClip.psd";
            string outputFileName = "result.png";

            using (PsdImage image = (PsdImage)Image.Load(sourceFileName))
            {
                image.Save(outputFileName, new PngOptions());
            }
{{< /highlight >}}

**PSDNET-547. Regular or vector mask for a layer group is ignored on rendering**

{{< highlight csharp >}}
        string sourceFileName = "Stripes3Mask.psd";
        string outputFileName = "OutputStripes3Mask.png";
        using (PsdImage image = (PsdImage)Image.Load(sourceFileName))
        {
            image.Save(outputFileName, new PngOptions());
        }
{{< /highlight >}}

**PSDNET-647. PSD image with disabled vector layer masks on saving enables vector masks**

{{< highlight csharp >}}
            string sourceFileName = "FourWithMasksVd.psd";
            string outputFileName = "FourWithMasksVdOutput.psd";

            using (PsdImage image = (PsdImage)Image.Load(sourceFileName))
            {
                image.Save(outputFileName);
            }
{{< /highlight >}}

**PSDNET-786. Exception when creating a TextLayer with text longer than 255 characters**

{{< highlight csharp >}}
            string output = "output.psd";

            using (var image = new PsdImage(100, 100))
            {
                string text = new string('a', 256);
                image.AddTextLayer(text, Rectangle.Empty);

                image.Save(output);
            }
{{< /highlight >}}

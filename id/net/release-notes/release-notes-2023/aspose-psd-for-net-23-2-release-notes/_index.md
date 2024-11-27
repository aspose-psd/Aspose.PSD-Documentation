---
title: Catatan Rilis Aspose.PSD untuk .NET 23.2
type: docs
weight: 110
url: /id/net/aspose-psd-untuk-net-23-2-catatan-rilis/
---

{{% alert color="primary" %}}

Halaman ini berisi catatan rilis untuk [Aspose.PSD untuk .NET 23.2](https://www.nuget.org/packages/Aspose.PSD/)

{{% /alert %}}

|**Kunci**|**Ringkasan**|**Kategori**|
| :- | :- | :- |
|PSDNET-1359|Memperbarui tata letak teks untuk meningkatkan penempatan, penggambaran, dan dukungan teks|Peningkatan|
|PSDNET-1270|Menambahkan kemampuan untuk memproses Efek Warp melalui API publik|Fitur|
|PSDNET-1391|Menambahkan dukungan dari modus berpuncak ke berpuncak dan berdasarkan berpuncak dari pengaturan Paragraf|Fitur|
|PSDNET-912|Mengubah Font dan Warna untuk TextLayer PSD|Bug|
|PSDNET-1022|Ekspor teks yang tidak benar pada uji coba TextUpdateTests, teks hilang|Bug|
|PSDNET-1221|Teks ekstra kecil hilang setelah meresize gambar PSD yang lebih besar|Bug|
|PSDNET-1301|Aspose.Psd untuk .NET textLayer.UpdateText() mencetak '-' (dash) sebagai garis bawah secara acak untuk set data yang berbeda|Bug|
|PSDNET-1379|Pengaturan Resolusi tidak berlaku pada ekspor dari PSD ke PDF|Bug|


## **Perubahan API Publik**
# **API Ditambahkan:**
- P:Aspose.PSD.ImageLoadOptions.PsdLoadOptions.AllowWarpRepaint
- P:Aspose.PSD.FileFormats.Psd.Layers.Text.ITextStyle.NoBreak
- T:Aspose.PSD.FileFormats.Psd.Layers.AdjustmentLayers.PosterizeLayer
- P:Aspose.PSD.FileFormats.Psd.Layers.AdjustmentLayers.PosterizeLayer.Levels
- M:Aspose.PSD.FileFormats.Psd.Layers.Layer.Save(System.IO.Stream)
- T:Aspose.PSD.FileFormats.Psd.LeadingType
- F:Aspose.PSD.FileFormats.Psd.LeadingType.BottomToBottom
- F:Aspose.PSD.FileFormats.Psd.LeadingType.TopToTop


# **API Dihapus:**
- T:Aspose.PSD.FileFormats.Psd.LeadingMode
- F:Aspose.PSD.FileFormats.Psd.LeadingMode.Auto
- F:Aspose.PSD.FileFormats.Psd.LeadingMode.Manual


## **Contoh Penggunaan:**

**PSDNET-912. Mengubah Font dan Warna untuk TextLayer PSD**

{{< highlight csharp >}}
string folderFont = "Fonts";
string fileSumber = "M1PDTT26052021001.psd";
string outputPsd = "result.psd";
string outputPng = "result.png";

FontSettings.SetFontsFolder(folderFont);

using (var image = (PsdImage)Image.Load(fileSumber))
{
    TextLayer layerNama = (TextLayer)image.Layers[9];
    var teksBagian = layerNama.TextData.Items[0];

    teksBagian.Text = "MODESTO SR";
    teksBagian.Style.FontName = FontSettings.GetAdobeFontName("Fugaz One");
    teksBagian.Style.FillColor = Color.Red;

    layerNama.TextData.UpdateLayerData();

    image.Save(outputPsd);
    image.Save(outputPng, new PngOptions() { ColorType = PngColorType.TrueColorWithAlpha });
}
{{< /highlight >}}

**PSDNET-1022. Ekspor teks yang tidak benar pada uji coba TextUpdateTests, teks hilang**

{{< highlight csharp >}}
string fileSumber = "ComplexKerningExample.psd";
string outputPsd = "TextUpdateComplexKerningExample_.psd";
string outputPng = "TextUpdateComplexKerningExample_.png";

using (var image = (PsdImage)Image.Load(fileSumber))
{
    for (int i = 0; i < image.Layers.Length; i++)
    {
        var layer = image.Layers[i] as TextLayer;

        if (layer != null)
        {
            layer.UpdateText("Teks diperbarui");
        }
    }

    image.Save(outputPsd);
    image.Save(outputPng, new PngOptions() { ColorType = PngColorType.TrueColorWithAlpha });
}
{{< /highlight >}}

**PSDNET-1221. Teks ekstra kecil hilang setelah resize gambar PSD yang lebih besar**

{{< highlight csharp >}}
string sumber = "textTest.psd";
string output = "output.png";

using (var psdImage = (PsdImage)Image.Load(sumber))
{
    psdImage.Resize(30, 30);

    psdImage.Save(output, new PngOptions());
}
{{< /highlight >}}

**PSDNET-1270. Menambahkan kemampuan untuk memproses Efek Warp melalui API publik**

{{< highlight csharp >}}
string sumberFile = "source.psd";
string pngWarpedExport = "warped.png";
string psdWarpedExport = "warpFile.psd";

var opsiLoadWarp = new PsdLoadOptions() { AllowWarpRepaint = true };

using (var image = (PsdImage)Image.Load(sumberFile, opsiLoadWarp))
{
    image.Save(pngWarpedExport, new PngOptions());
    image.Save(psdWarpedExport, new PsdOptions());
}
{{< /highlight >}}

**PSDNET-1301. Aspose.Psd untuk .NET textLayer.UpdateText() mencetak '-' (dash) sebagai garis bawah secara acak untuk set data yang berbeda**

{{< highlight csharp >}}
string sumber = "TEST_PSD_FILE.PSD";
string output = "OUTPUTIMAGE.jpg";

using (PsdImage psdImage = (PsdImage)Image.Load(sumber))
{
    foreach (var layer in psdImage.Layers.Where(x => x.IsVisible))
    {
        if (layer is TextLayer)
        {
            TextLayer textLayer = layer as TextLayer;
            switch (layer.Name.Trim().ToUpper())
            {
                case "NAMA":
                    textLayer.UpdateText("Tn. JACK SMITH");
                    break;
                case "IDNO":
                    textLayer.UpdateText("OFF-022/GRP - 016");
                    break;
                case "DESIGNASI":
                    textLayer.UpdateText("OFFICER-001");
                    break;
                case "GOLONGANDARAH":
                    textLayer.UpdateText("AB-");
                    break;
                case "ALAMAT":
                    textLayer.UpdateText("BLOCK-A, JALAN-7, NO APPT - 047, SEKTOR-024");
                    break;
                case "ALAMATPERMANEN":
                    textLayer.UpdateText("RUMAH NO - 42, LANE -025, PERMATA PUSAT PANORAMA, SEKTOR - 45");
                    break;
            }
        }
    }

    psdImage.Save(output, new JpegOptions());
}
{{< /highlight >}}

**PSDNET-1379. Pengaturan Resolusi tidak berlaku pada ekspor dari PSD ke PDF**

{{< highlight csharp >}}
string input = "Datensatz 1.psd";
string output = "Datensatz 1.pdf";

using (var image = Image.Load(input, new PsdLoadOptions()))
{
    ResolutionSetting pengaturanResolusi = new ResolutionSetting(300, 300);

    image.Save(output, new PdfOptions()
    {
        ResolutionSettings = pengaturanResolusi
    });
}
{{< /highlight >}}

**PSDNET-1391. Menambahkan dukungan dari modus berpuncak ke berpuncak dan berdasarkan berpuncak dari pengaturan Paragraf**

{{< highlight csharp >}}
string input = "leadingMode.psd";
string output = "output_leadingMode.png";

using (var psdImage = (PsdImage)Image.Load(input, new PsdLoadOptions()))
{
    IText teks1 = ((TextLayer)psdImage.Layers[1]).TextData;
    foreach (var teksBagian in teks1.Items)
    {
        teksBagian.Paragraph.LeadingType = LeadingType.TopToTop; // Mengubah nilai LeadingType   
    }
    teks1.Items[8].Text = "TopToTop";
    teks1.Items[8].Style.FillColor = Color.ForestGreen;
    teks1.UpdateLayerData();

    IText teks2 = ((TextLayer)psdImage.Layers[2]).TextData;
    foreach (var teksBagian in teks2.Items)
    {
        teksBagian.Paragraph.LeadingType = LeadingType.BottomToBottom; // Mengubah nilai LeadingType   
    }
    teks2.Items[8].Text = "BottomToBottom";
    teks2.Items[8].Style.FillColor = Color.ForestGreen;
    teks2.UpdateLayerData();

    psdImage.Save(output, new PngOptions());
}
{{< /highlight >}}

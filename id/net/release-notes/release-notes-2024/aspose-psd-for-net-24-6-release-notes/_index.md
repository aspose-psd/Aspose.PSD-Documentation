---
title: Catatan Rilis Aspose.PSD untuk .NET 24.6
type: docs
weight: 70
url: /id/net/aspose-psd-for-net-24-6-release-notes/
---

{{% alert color="primary" %}}

Halaman ini berisi catatan rilis untuk [Aspose.PSD untuk .NET 24.6] (https://www.nuget.org/packages/Aspose.PSD/)

{{% /alert %}}

| **Kunci**   | **Ringkasan**                                           | **Kategori** |
|:------------|:--------------------------------------------------------|:-------------|
| PSDNET-1450 | Implementasikan dukungan untuk lapisan peta gradien    | Fitur        |
| PSDNET-1670 | [Format AI] Tambahkan dukungan Metadata XPacket ke Format AI  | Fitur        |
| PSDNET-1831 | Implementasikan jenis warp Inflate, Squeeze, dan Twist  | Fitur        |
| PSDNET-1653 | Mode Rgb dan Lab tidak dapat berisi kurang dari 3 saluran dan lebih dari 4 saluran dalam file dengan Lapisan ArtBoard | Bug          |
| PSDNET-1775 | Area pemrosesan atas harus positif. (Parameter 'areaToProcess') pada pemrosesan file tertentu | Bug          |
| PSDNET-2052 | Diperluas di atas gambar kanvas dipotong setelah penyimpanan. Data hilang tetapi Pratinjau terlihat benar | Bug          |

## **Perubahan API Publik**
# **API Ditambahkan:**
- P:Aspose.PSD.FileFormats.Psd.Layers.FillSettings.NoiseGradientFillSettings.ExpansionCount
- M:Aspose.PSD.FileFormats.Psd.PsdImage.AddGradientMapAdjustmentLayer
- T:Aspose.PSD.FileFormats.Psd.Layers.AdjustmentLayers.GradientMapLayer
- P:Aspose.PSD.FileFormats.Psd.Layers.AdjustmentLayers.GradientMapLayer.GradientSettings
- P:Aspose.PSD.FileFormats.Ai.AiImage.XmpData

# **API Dihapus:**
- Tidak Ada

## **Contoh Penggunaan:**

**PSDNET-1450. Implementasikan dukungan untuk lapisan peta gradien**

{{< highlight csharp >}}
string sourceFile = Path.Combine(baseFolder, "gradient_map_src.psd");
string outputFile = Path.Combine(outputFolder, "gradient_map_src_output.psd");

using (PsdImage im = (PsdImage)Image.Load(sourceFile))
{
    // Tambahkan lapisan penyesuaian peta gradien.
    GradientMapLayer layer = im.AddGradientMapAdjustmentLayer();
    layer.GradientSettings.Reverse = true;

    im.Save(outputFile);
}

// Periksa perubahan yang disimpan
using (PsdImage im = (PsdImage)Image.Load(outputFile))
{
    GradientMapLayer gradientMapLayer = im.Layers[1] as GradientMapLayer;
    GradientFillSettings gradientSettings = (GradientFillSettings)gradientMapLayer.GradientSettings;

    AssertAreEqual(0.0, gradientSettings.Angle);
    AssertAreEqual((short)4096, gradientSettings.Interpolation);
    AssertAreEqual(true, gradientSettings.Reverse);
    AssertAreEqual(false, gradientSettings.AlignWithLayer);
    AssertAreEqual(false, gradientSettings.Dither);
    AssertAreEqual(GradientType.Linear, gradientSettings.GradientType);
    AssertAreEqual(100, gradientSettings.Scale);
    AssertAreEqual(0.0, gradientSettings.HorizontalOffset);
    AssertAreEqual(0.0, gradientSettings.VerticalOffset);
    AssertAreEqual("Custom", gradientSettings.GradientName);
}

void AssertAreEqual(object expected, object actual, string message = null)
{
    if (!object.Equals(expected, actual))
    {
        throw new Exception(message ?? "Objek tidak sama.");
    }
}
{{< /highlight >}}

**PSDNET-1670. [Format AI] Tambahkan dukungan Metadata XPacket ke Format AI**

{{< highlight csharp >}}
string sourceFile = Path.Combine(baseFolder, "ai_one.ai");

void AssertAreEqual(object expected, object actual)
{
    if (!object.Equals(expected, actual))
    {
        throw new Exception("Objek tidak sama.");
    }
}

void AssertIsNotNull(object testObject)
{
    if (testObject == null)
    {
        throw new Exception("Objek uji bernilai null.");
    }
}

string creatorToolKey = ":CreatorTool";
string nPagesKey = "xmpTPg:NPages";
string unitKey = "stDim:unit";
string heightKey = "stDim:h";
string widthKey = "stDim:w";

string expectedCreatorTool = "Adobe Illustrator CC 22.1 (Windows)";
string expectedNPages = "1";
string expectedUnit = "Pixels";
double expectedHeight = 768;
double expectedWidth = 1366;

using (AiImage image = (AiImage)Image.Load(sourceFile))
{
    // Metadata Xmp ditambahkan.
    var xmpMetaData = image.XmpData;

    AssertIsNotNull(xmpMetaData);

    // Sekarang kami bisa mengakses Paket Xmp dari file AI.
    var basicPackage = xmpMetaData.GetPackage(Namespaces.XmpBasic) as XmpBasicPackage;
    var package = xmpMetaData.Packages[4];

    // Dan kami memiliki akses ke konten paket-paket ini.
    var creatorTool = basicPackage[creatorToolKey].ToString();
    var nPages = package[nPagesKey];
    var unit = package[unitKey];
    var height = double.Parse(package[heightKey].ToString(), CultureInfo.InvariantCulture);
    var width = double.Parse(package[widthKey].ToString(), CultureInfo.InvariantCulture);

    AssertAreEqual(creatorTool, expectedCreatorTool);
    AssertAreEqual(nPages, expectedNPages);
    AssertAreEqual(unit, expectedUnit);
    AssertAreEqual(height, expectedHeight);
    AssertAreEqual(width, expectedWidth);
}
{{< /highlight >}}

**PSDNET-1831. Implementasikan jenis warp Inflate, Squeeze, dan Twist**

{{< highlight csharp >}}
string[] files = { "Twist", "Squeeze", "Squeeze_vert", "Inflate" };

foreach (string prefix in files)
{
    string sourceFile = Path.Combine(baseFolder, prefix + ".psd");
    string outputFile = Path.Combine(outputFolder, prefix + "_export.png");

    using (var psdImage = (PsdImage)Image.Load(sourceFile, new PsdLoadOptions() { AllowWarpRepaint = true, LoadEffectsResource = true }))
    {
        psdImage.Save(outputFile, new PngOptions
        {
            ColorType = PngColorType.TruecolorWithAlpha
        });
    }
}
{{< /highlight >}}

**PSDNET-1653. Mode Rgb dan Lab tidak dapat berisi kurang dari 3 saluran dan lebih dari 4 saluran dalam file dengan Lapisan ArtBoard**

{{< highlight csharp >}}
string sourceFile = Path.Combine(baseFolder, "Rgb5Channels.psb");
string outputFile = Path.Combine(outputFolder, "Rgb5Channels_output.psd");

using (PsdImage image = (PsdImage)Aspose.PSD.Image.Load(sourceFile))
{
    // Disini seharusnya tidak ada pengecualian
    image.Save(outputFile);
}
{{< /highlight >}}

**PSDNET-1775. Area pemrosesan atas harus positif. (Parameter 'areaToProcess') pada pemrosesan file tertentu**

{{< highlight csharp >}}
string sourceFile = @"BANNERS_2_Intel-Gamer_psak.psd";
string outputFile = @"BANNERS_2_Intel-Gamer_psak_out.psd";
PsdLoadOptions psdLoadOptions = new PsdLoadOptions();
psdLoadOptions.LoadEffectsResource = true;
psdLoadOptions.AllowWarpRepaint = true;
using (PsdImage image = (PsdImage)PsdImage.Load(sourceFile, psdLoadOptions))
{
    image.Save(outputFile);
    // Tidak seharusnya terjadi pengecualian
}
{{< /highlight >}}

**PSDNET-2052. Diperluas di atas gambar kanvas dipotong setelah penyimpanan. Data hilang tetapi Pratinjau terlihat benar**

{{< highlight csharp >}}
string sourceFile = Path.Combine(baseFolder, "bigfile.psd");

string outputFile = Path.Combine(outputFolder, "bigfile_output.psd");
string outputPicture = Path.Combine(outputFolder, "bigfile.png");

PsdLoadOptions loadOptions = new PsdLoadOptions()
{
    LoadEffectsResource = true,
    UseDiskForLoadEffectsResource = true
};

using (var psdImage = (PsdImage)Image.Load(sourceFile, loadOptions))
{
    // Tidak seharusnya terjadi kesalahan disini
    psdImage.Save(outputFile, new PsdOptions { CompressionMethod = CompressionMethod.RLE });
}

using (var psdImage = (PsdImage)Image.Load(outputFile, loadOptions))
{
    psdImage.Resize(psdImage.Width / 10, psdImage.Height / 10);

    // Tidak seharusnya terjadi kesalahan disini
    psdImage.Save(outputPicture, new PngOptions { ColorType = PngColorType.CitraNofTruecolorWitAlpha });
}
{{< /highlight >}}

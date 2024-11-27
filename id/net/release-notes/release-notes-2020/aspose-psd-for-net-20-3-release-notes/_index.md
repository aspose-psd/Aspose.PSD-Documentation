---
title: Catatan Rilis Aspose.PSD untuk .NET 20.3
type: docs
weight: 100
url: /id/net/aspose-psd-for-net-20-3-release-notes/
---

{{% alert color="primary" %}} 

Halaman ini berisi catatan rilis untuk [Aspose.PSD untuk .NET 20.3](https://www.nuget.org/packages/Aspose.PSD/)

{{% /alert %}} 

|**Kunci**|**Ringkasan**|**Kategori**|
| :- | :- | :- |
|PSDNET-188|Dukungan .Net Core|Fitur|
|PSDNET-523|Konversi file Adobe Illustrator menjadi PDF|Fitur|
|PSDNET-212|Tambahkan kemampuan untuk merender gaya berbeda dalam satu lapisan teks|Fitur|
|PSDNET-144|Dukungan untuk Black and White Adjustment Layer|Fitur|
|PSDNET-233|Tambahkan dukungan untuk mengekspor format AI (Versi 8) ke format lain|Fitur|
|PSDNET-540|Dukungan untuk pemrosesan Mode Bauran PassThrough (Digunakan hanya untuk Kelompok Layer).|Fitur|
|PSDNET-539|Exception: Gagal memuat gambar saat memuat gambar dengan Sumber Daya Nama Alpha Unicode kosong|Bug|
|PSDNET-541|Output tidak benar setelah mengubah visibilitas LayerGroup|Bug|
|PSDNET-516|Exception saat memuat gambar PSD: Bagian Warna (Sumber Daya Bayangan Jatuh) harus berisi 3 komponen warna untuk RGB atau 4 komponen warna untuk CMYK|Bug|
|PSDNET-536|Exception jika mencoba menggambar di lapisan yang baru dibuat jika versi Constructor yang sederhana digunakan|Bug|

## **Perubahan API Publik**
# **API Ditambahkan:**
- T:Aspose.PSD.FileFormats.Psd.FontBaseline
- F:Aspose.PSD.FileFormats.Psd.FontBaseline.None
- F:Aspose.PSD.FileFormats.Psd.FontBaseline.Superscript
- F:Aspose.PSD.FileFormats.Psd.FontBaseline.Subscript
- T:Aspose.PSD.FileFormats.Psd.FontCaps
- F:Aspose.PSD.FileFormats.Psd.FontCaps.None
- F:Aspose.PSD.FileFormats.Psd.FontCaps.SmallCaps
- F:Aspose.PSD.FileFormats.Psd.FontCaps.AllCaps
- M:Aspose.PSD.FileFormats.Psd.PsdImage.AddBlackWhiteAdjustmentLayer
- F:Aspose.PSD.FileFormats.Psd.Layers.BlendMode.Absent
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerGroup.BlendModeKey
- P:Aspose.PSD.FileFormats.Psd.Layers.Text.ITextStyle.FauxBold
- P:Aspose.PSD.FileFormats.Psd.Layers.Text.ITextStyle.FauxItalic
- P:Aspose.PSD.FileFormats.Psd.Layers.Text.ITextStyle.Underline
- P:Aspose.PSD.FileFormats.Psd.Layers.Text.ITextStyle.Strikethrough
- P:Aspose.PSD.FileFormats.Psd.Layers.Text.ITextStyle.FontBaseline
- P:Aspose.PSD.FileFormats.Psd.Layers.Text.ITextStyle.BaselineShift
- P:Aspose.PSD.FileFormats.Psd.Layers.Text.ITextStyle.FontCaps
- M:Aspose.PSD.FileFormats.Psd.Layers.Text.IText.ProducePortions(System.String[],Aspose.PSD.FileFormats.Psd.Layers.Text.ITextStyle,Aspose.PSD.FileFormats.Psd.Layers.Text.ITextParagraph)
# **API Dihapus:**
- None

## **Contoh Penggunaan:**
**PSDNET-523. Konversi file Adobe Illustrator menjadi PDF**

{{< highlight java >}}

 string sourceFile = "rect2_color.ai";

using (var aiImage = (AiImage)Image.Load(sourceFile))

{

    aiImage.Save("rect2_color.ai_output.pdf", new PdfOptions());

}

{{< /highlight >}}

**PSDNET-212. Tambahkan kemampuan untuk merender gaya berbeda dalam satu lapisan teks**

{{< highlight java >}}

 string sourceFile = "text212.psd";

string ethalonFile = "Ethalon_text212.psd";

string outputFile = "Output_text212.psd";

using (var img = (PsdImage)Image.Load(sourceFile))

{

    TextLayer textLayer = (TextLayer)img.Layers[1];

    IText textData = textLayer.TextData;

    ITextStyle defaultStyle = textData.ProducePortion().Style;

    ITextParagraph defaultParagraph = textData.ProducePortion().Paragraph;

    defaultStyle.FillColor = Color.DimGray;

    defaultStyle.FontSize = 51;

    textData.Items[1].Style.Strikethrough = true;

    ITextPortion[] newPortions = textData.ProducePortions(new string[] { "E=mc",  "2\r",  "Bold",  "Italic\r",  "Lowercasetext" }, defaultStyle, defaultParagraph);

    newPortions[0].Style.Underline = true; // edit text style "E=mc"

    newPortions[1].Style.FontBaseline = FontBaseline.Superscript; // edit text style "2\r"

    newPortions[2].Style.FauxBold = true; // edit text style "Bold"

    newPortions[3].Style.FauxItalic = true; // edit text style "Italic\r"

    newPortions[3].Style.BaselineShift = -25; // edit text style "Italic\r"

    newPortions[4].Style.FontCaps = FontCaps.SmallCaps; // edit text style "Lowercasetext"

    foreach (var newPortion in newPortions)

    {

        textData.AddPortion(newPortion);

    }

    textData.UpdateLayerData();

    img.Save(outputFile);

}

{{< /highlight >}}

**PSDNET-233. Tambahkan dukungan untuk mengekspor format AI (Versi 8) ke format lain**

{{< highlight java >}}

 // Contoh mengekspor file AI ke format PSD dan PNG

string sourceFileName = "form_8.ai";

string outputFileName = "form_8_export";

using (AiImage image = (AiImage)Image.Load(sourceFileName))

{

    image.Save(outputFileName + ".psd", new PsdOptions());

    image.Save(outputFileName + ".png", new PngOptions() { ColorType = PngColorType.TruecolorWithAlpha });

}

{{< /highlight >}}

**PSDNET-540. Dukungan untuk pemrosesan Mode Bauran PassThrough (Digunakan hanya untuk Kelompok Layer).**

{{< highlight java >}}

 void AssertIsTrue(bool condition, string message)

{

    if (!condition)

    {

        throw new FormatException(message);

    }

}

string sourceFileName = "Apple.psd";

string outputFileName = "Output" + sourceFileName;

using (PsdImage image = (PsdImage)Image.Load(sourceFileName))

{

    AssertIsTrue(image.Layers.Length >= 23, "Tidak ada lapisan ke-23.");

    var layer = image.Layers[23] as LayerGroup;

    AssertIsTrue(layer != null, "Layer ke-23 bukan kelompok layer.");

    AssertIsTrue(layer.Name == "AdjustmentGroup", "Nama layer ke-23 bukan 'AdjustmentGroup'.");

    AssertIsTrue(layer.BlendModeKey == BlendMode.PassThrough, "Layer AdjustmentGroup harus memiliki mode bauran 'pass through'.");

    image.Save(outputFileName, new PsdOptions());

    image.Save("OutputApple.png", new PngOptions() { ColorType = PngColorType.TruecolorWithAlpha });

    layer.BlendModeKey = BlendMode.Normal;

    image.Save("Normal" + outputFileName, new PsdOptions());

    image.Save("NormalOutputApple.png", new PngOptions() { ColorType = PngColorType.TruecolorWithAlpha });

}

{{< /highlight >}}

**SPSDNET-180. Mengubah teks lapisan teks menghasilkan exception**

{{< highlight java >}}

 // Mengubah teks lapisan teks menghasilkan exception

string filePath = "FlipVertical.psd";

string outputPath = "FlipVertical_changed.psd";

var newText = "Test";

using (var image = Image.Load(filePath))

{

    var psdImage = image as PsdImage;

    if (image == null)

    {

        return;

    }

    var layers = psdImage.Layers;

    for (var index = layers.Length - 1; index >= 0; index--)

    {

        var layer = layers[index] as TextLayer;

        if (layer == null)

        {

            continue;

        }

        layer.UpdateText(newText);

    }

    var imageOptions = new PsdOptions(psdImage);

    psdImage.Save(outputPath, imageOptions);

}

{{< /highlight >}}

**PSDNET-182. Menyimpan gambar PSD setelah operasi RotateFlip menghasilkan file yang rusak yang tidak dapat dibuka.**

{{< highlight java >}}

 string sourceFileName = "1.psd";

RotateFlipType flipType = RotateFlipType.Rotate270FlipXY;

string outFileNamePsd = "RotateFlipTest2617.psd";

using (PsdImage image = (PsdImage)Image.Load(sourceFileName))

{

    image.RotateFlip(flipType);

    image.Save(outFileNamePsd);

}

// Harus dieksekusi tanpa exception

using (PsdImage image = (PsdImage)Image.Load(outFileNamePsd)) 

{

    // Tidak melakukan apa-apa

}

{{< /highlight >}}

**PSDNET-539. Exception: Gagal memuat gambar saat memuat gambar dengan Sumber Daya Nama Alpha Unicode kosong**

{{< highlight java >}}

 string sourcePath = "apple.psd";

using (var psdImage = (PsdImage)Image.Load(sourcePath)) // Di sini kita seharusnya tidak mendapatkan exception

{

    // tidak melakukan apa-apa

}

{{< /highlight >}}

**PSDNET-541. Output tidak benar setelah mengubah visibilitas LayerGroup**

{{< highlight java >}}

 string sourceFile = "input.psd";

string outputFile = "output.psd";

// melakukan perubahan pada nama lapisan dan menyimpannya

using (var image = (PsdImage)Image.Load(sourceFile))

{

    for (int i = 0; i < image.Layers.Length; i++)

    {

        var layer = image.Layers[i];

        // Mematikan semua dalam sebuah grup

        if (layer is LayerGroup)

        {

            layer.IsVisible = false;

        }

    }

    image.Save(outputFile);

}

{{< /highlight >}}

**PSDNET-516. Exception saat memuat gambar PSD: Bagian Warna (Sumber Daya Bayangan Jatuh) harus berisi 3 komponen warna untuk RGB atau 4 komponen warna untuk CMYK**

{{< highlight java >}}

 string sourceFile = "sss0136=GUID-SSS0136=1=ar-sa=Low.psd";

using (var img = (PsdImage)Image.Load(sourceFile)) // Di sini kita seharusnya tidak mendapatkan exception

{

    // tidak melakukan apa-apa

}

{{< /highlight >}}

**PSDNET-536. Exception jika mencoba menggambar di lapisan yang baru dibuat jika versi Constructor yang sederhana digunakan**

{{< highlight java >}}

 string outputFile = "output.psd";

int width = 100;

int height = 100;

using (var image = new PsdImage(width, height))

{

    var layer = new Layer();

    layer.Bottom = height;

    layer.Right = width;

    image.AddLayer(layer);

    Graphics graphic = new Graphics(layer);

    graphic.Clear(Color.Yellow);

    // menggambar persegi panjang dengan pena

    graphic.DrawRectangle(new Pen(Color.Red), new Rectangle(30, 10, 40, 80));

    // menggambar persegi panjang lain dengan Sikat Solid berwarna Biru

    graphic.DrawRectangle(new Pen(new SolidBrush(Color.Blue)), new Rectangle(10, 30, 80, 40));

    image.Save(outputFile);

}

{{< /highlight >}}

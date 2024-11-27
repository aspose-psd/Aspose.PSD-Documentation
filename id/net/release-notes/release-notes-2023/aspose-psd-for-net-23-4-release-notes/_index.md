---
title: Catatan Rilis Aspose.PSD untuk .NET 23.4
type: docs
weight: 90
url: /id/net/aspose-psd-for-net-23-4-release-notes/
---

{{% alert color="primary" %}}

Halaman ini berisi catatan rilis untuk [Aspose.PSD untuk .NET 23.4](https://www.nuget.org/packages/Aspose.PSD/)

{{% /alert %}}

|**Kunci**|**Ringkasan**|**Kategori**|
| :- | :- | :- |
|PSDNET-1409|Desain kelas RawColor untuk API publik untuk digunakan dalam API PSD daripada struct Color yang sudah usang|Perbaikan|
|PSDNET-1332|Mengintegrasikan Layer Penyesuaian Peta Gradien dari Probation ke kode utama Aspose.PSD|Fitur|
|PSDNET-1448|Pengeditan teks menggunakan Potongan Teks tidak menyimpan hasil yang benar|Bug|
|PSDNET-1449|Awal dan akhir gaya atau paragraf muncul di tempat yang tidak benar pada pengeditan Lapisan Teks oleh ITextPortion|Bug|
|PSDNET-1509|Pemformatan berpindah saat pengeditan di photoshop|Bug|


## **Perubahan API Publik**
# **API Ditambahkan:**
- T:Aspose.PSD.FileFormats.Psd.Layers.Gradient.GradientKind
- F:Aspose.PSD.FileFormats.Psd.Layers.Gradient.GradientKind.Solid
- F:Aspose.PSD.FileFormats.Psd.Layers.Gradient.GradientKind.Noise
- T:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.GrdmResource
- M:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.GrdmResource.#ctor
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.GrdmResource.Signature
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.GrdmResource.Key
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.GrdmResource.Length
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.GrdmResource.PsdVersion
- M:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.GrdmResource.Save(Aspose.PSD.StreamContainer,System.Int32)
- F:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.GrdmResource.TypeToolKey
- M:Aspose.PSD.FileFormats.Psd.Layers.Layer.Save(System.IO.Stream)
- P:Aspose.PSD.FileFormats.Psd.Layers.FillSettings.GradientColorPoint.ColorMode
- M:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.GrdmResource.SetPsdVersion(System.UInt16)
- T:Aspose.PSD.FileFormats.Psd.Core.RawColor.ColorComponent
- M:Aspose.PSD.FileFormats.Psd.Core.RawColor.ColorComponent.#ctor(System.Byte,System.String)
- P:Aspose.PSD.FileFormats.Psd.Core.RawColor.ColorComponent.PermittedFullNames
- P:Aspose.PSD.FileFormats.Psd.Core.RawColor.ColorComponent.BitDepth
- P:Aspose.PSD.FileFormats.Psd.Core.RawColor.ColorComponent.Value
- P:Aspose.PSD.FileFormats.Psd.Core.RawColor.ColorComponent.Name
- P:Aspose.PSD.FileFormats.Psd.Core.RawColor.ColorComponent.Description
- P:Aspose.PSD.FileFormats.Psd.Core.RawColor.ColorComponent.FullName
- T:Aspose.PSD.FileFormats.Psd.Core.RawColor.RawColor
- M:Aspose.PSD.FileFormats.Psd.Core.RawColor.RawColor.#ctor(Aspose.PSD.FileFormats.Psd.Core.RawColor.ColorComponent[])
- P:Aspose.PSD.FileFormats.Psd.Core.RawColor.RawColor.Components
- M:Aspose.PSD.FileFormats.Psd.Core.RawColor.RawColor.GetColorModeName
- M:Aspose.PSD.FileFormats.Psd.Core.RawColor.RawColor.GetBitDepth
- M:Aspose.PSD.FileFormats.Psd.Core.RawColor.RawColor.GetAsInt
- M:Aspose.PSD.FileFormats.Psd.Core.RawColor.RawColor.SetAsInt(System.Int32)
- M:Aspose.PSD.FileFormats.Psd.Core.RawColor.RawColor.GetAsLong
- M:Aspose.PSD.FileFormats.Psd.Core.RawColor.RawColor.SetAsLong(System.Int64)
- M:Aspose.PSD.FileFormats.Psd.Core.RawColor.RawColor.#ctor(Aspose.PSD.PixelDataFormat,System.Int16)
- P:Aspose.PSD.FileFormats.Psd.Core.RawColor.RawColor.ColorMode
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.GrdmResource.Reverse
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.GrdmResource.Dither
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.GrdmResource.GradientName
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.GrdmResource.ExpansionCount
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.GrdmResource.Interpolation
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.GrdmResource.GradientMode
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.GrdmResource.RndNumberSeed
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.GrdmResource.ShowTransparency
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.GrdmResource.UseVectorColor
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.GrdmResource.Roughness
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.GrdmResource.ColorModel
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.GrdmResource.ColorPoints
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.GrdmResource.TransparencyPoints
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.GrdmResource.MinimumColor
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.GrdmResource.MaximumColor


# **API Dihapus:**
- Tidak ada


## **Contoh Penggunaan:**

**PSDNET-1332. Mengintegrasikan Layer Penyesuaian Peta Gradien dari Probation ke kode utama Aspose.PSD**

{{< highlight csharp >}}
string sourceFile = "gradient_map_default.psd";
string outputFile = "gradient_map_res.psd";

using (var image = (PsdImage)Image.Load(sourceFile, new PsdLoadOptions()))
{
    Layer layer = image.Layers[1];
    GrdmResource grdmResource = (GrdmResource)layer.Resources[0];

    // periksa nilai saat ini
    AssertAreEqual(false, grdmResource.Reverse);
    AssertAreEqual((ulong)65535, grdmResource.ColorPoints[1].RawColor.Components[2].Value);
    AssertAreEqual((ulong)65535, grdmResource.ColorPoints[1].RawColor.Components[3].Value);

    grdmResource.Reverse = true;
    // Warna Merah untuk titik warna gradien kedua
    grdmResource.ColorPoints[1].RawColor.Components[1].Value = ushort.MaxValue;
    grdmResource.ColorPoints[1].RawColor.Components[2].Value = 0;
    grdmResource.ColorPoints[1].RawColor.Components[3].Value = 0;

    image.Save(outputFile, new PsdOptions());
}

using (var image = (PsdImage)Image.Load(outputFile))
{
    Layer layer = image.Layers[1];
    GrdmResource grdmResource = (GrdmResource)layer.Resources[0];

    // periksa nilai yang telah diubah
    AssertAreEqual(true, grdmResource.Reverse);
    AssertAreEqual((ulong)0, grdmResource.ColorPoints[1].RawColor.Components[2].Value);
    AssertAreEqual((ulong)0, grdmResource.ColorPoints[1].RawColor.Components[3].Value);
}

void AssertAreEqual(object expected, object actual, string message = null)
{
    if (!object.Equals(expected, actual))
    {
        throw new Exception(message ?? "Objek tidak sama.");
    }
}
{{< /highlight >}}

**PSDNET-1409. Desain kelas RawColor untuk API publik untuk digunakan dalam API PSD daripada struct Color yang sudah usang**

{{< highlight csharp >}}
void AssertAreEqual(object expected, object actual, string message = null)
{
    if (!object.Equals(expected, actual))
    {
        throw new Exception(message ?? "Objek tidak sama.");
    }
}

var color = new RawColor(PixelDataFormat.Rgba32Bpp);
var oldColor = Color.FromArgb(5, 1, 2, 3);

var argbValue = oldColor.ToArgb();
color.SetAsInt(argbValue);

AssertAreEqual("ARGB", color.GetColorModeName());
AssertAreEqual(32, color.GetBitDepth());
AssertAreEqual("A Alpha", color.Components[0].FullName);
AssertAreEqual(5, (int)color.Components[0].Value);
AssertAreEqual("R Red", color.Components[1].FullName);
AssertAreEqual(1, (int)color.Components[1].Value);
AssertAreEqual("G Green", color.Components[2].FullName);
AssertAreEqual(2, (int)color.Components[2].Value);
AssertAreEqual("B Blue", color.Components[3].FullName);
AssertAreEqual(3, (int)color.Components[3].Value);

AssertAreEqual(argbValue, color.GetAsInt());
{{< /highlight >}}

**PSDNET-1448. Pengeditan teks menggunakan Potongan Teks tidak menyimpan hasil yang benar**

{{< highlight csharp >}}
string sourceFile =  "originalv5.psd";
string psdExportPath =  "export.psd";

using (var imageTestEmail = (PsdImage)Image.Load(sourceFile))
{
    var layers = imageTestEmail.Layers;
    foreach (var layerItem in layers)
    {
        var isTextLayer = layerItem.GetType() == typeof(TextLayer) ? true : false;
        if (isTextLayer)
        {
            var layerTLToUpdateText = (TextLayer)layerItem;

            //Cari teks lsak
            if (layerTLToUpdateText.Text.Contains("lsak"))
            {
                var textDataTL = layerTLToUpdateText.TextData;

                if (textDataTL.Text.Contains("lsak") && textDataTL.Text.Contains("\r"))
                {
                    //Ganti teks
                    replaceLsakText(textDataTL);
                    //Format teks
                    formatStyleText(textDataTL);
                }
            }
        }
    }

    imageTestEmail.Save(psdExportPath, new PsdOptions());
}

string[] texts = new string[]
{
        "Power play.",
        "//Πιο επεκτατικοί κόσμοι. Γρήγοροι χρόνοι φόρτωσης. Υψηλά ποσοστά καρέ και ευρύτερο φάσμα χρωμάτων. Ένας υπολογιστής με Windows ήταν πάντα η καλύτερη πλατφόρμα για παιχνίδια—και στα Windows 11, γίνεται ακόμα καλύτερος./"
};

using (PsdImage psdImage = (PsdImage)Aspose.PSD.Image.Load(psdExportPath))
{
    Txt2Resource txt2OutputResource = (Txt2Resource)psdImage.GlobalLayerResources[1];
    byte[] bytes = txt2OutputResource.Data;
    string txt2Data = "";
    for (int i = 9500; i < bytes.Length; i++)
    {
        if ((char)bytes[i] == '\0')
        {
            txt2Data += "0";
        }
        else
        {
            txt2Data += (char)bytes[i];
        }
    }

    string key0 = @" >> /1 " + texts[0].Length + " >>";       // awalan untuk panjang teks pertama
    string key1 = @" >> /1 " + texts[1].Length + " >>";       // awalan untuk panjang teks kedua

    int index0 = txt2Data.IndexOf(key0);
    int index1 = txt2Data.IndexOf(key1);

    if (index0 < 0)
    {
        throw new Exception("Tidak dapat menemukan panjang gaya teks pertama, harus sama dengan " + texts[0].Length);
    }

    if (index1 < 0)
    {
        throw new Exception("Tidak dapat menemukan panjang gaya teks kedua, harus sama dengan " + texts[1].Length); ;
    }
}


void replaceLsakText(IText textData)
{
    var countPortions = textData.Items.Length;
    ITextStyle defaultStyle = textData.Items[0].Style;
    ITextParagraph defaultParagraph = textData.Items[0].Paragraph;

    var textToReplace = textData.Text;

    //hapus potongan lama
    for (int i = 0; i < (countPortions); i++)

    {
        textData.RemovePortion(0);
    }

    ITextPortion newPortion = textData.ProducePortion();
    newPortion.Paragraph.Apply(defaultParagraph);
    newPortion.Style.Apply(defaultStyle);
    newPortion.Text = ReplaceText(textToReplace);
    textData.AddPortion(newPortion);
    textData.UpdateLayerData();
}

void formatStyleText(IText textData)
{
    //validasi jika memiliki tag
    Regex tagRegex = new Regex(@"<[^>]+>");
    bool hasTags = tagRegex.IsMatch(textData.Text);
    var countPortions = textData.Items.Length;
    ITextStyle defaultStyle = textData.Items[0].Style;
    ITextParagraph defaultParagraph = textData.Items[0].Paragraph;

    if (hasTags)
    {
        var tagRegex2 = @"[^<>]+|<\s*([^ >]+)[^>]*>.*?<\s*/\s*\1\s*>";
        var matchesImgSrc = Regex.Matches(textData.Text, tagRegex2, RegexOptions.IgnoreCase | RegexOptions.Singleline);
        var listlsaks = new List<string>();
        foreach (Match m in matchesImgSrc)
        {
            listlsaks.Add(m.Value);
        }
        string[] textSplit = listlsaks.ToArray();

        for (int i = 0; i < (countPortions); i++)
        {
            textData.RemovePortion(0);
        }

        for (int i = 0; i < textSplit.Length; i++)
        {
            ITextPortion newPortion = textData.ProducePortion();
            newPortion.Paragraph.Apply(defaultParagraph);
            newPortion.Style.Apply(defaultStyle);
            bool hasTagsIsaks = false;
            hasTagsIsaks = tagRegex.IsMatch(textSplit[i]);

            if (hasTagsIsaks)
            {
                if (textSplit[i].Contains("pt"))
                {
                    newPortion.Style.FontSize = 72;
                };

                newPortion.Text = Regex.Replace(textSplit[i], "<.*?>", String.Empty).Replace("br/", "//");
                textData.AddPortion(newPortion);
            }
            else
            {
                newPortion.Text = Regex.Replace(textSplit[i], "<.*?>", String.Empty).Replace("br/", "//");
                textData.AddPortion(newPortion);
            }
        }
    }
    else
    {
        var textToReplace = textData.Text;
        for (int i = 0; i < (countPortions); i++)
        {
            textData.RemovePortion(0);
        }

        ITextPortion newPortion = textData.ProducePortion();
        newPortion.Paragraph.Apply(defaultParagraph);
        newPortion.Style.Apply(defaultStyle);
        newPortion.Text = textToReplace.Replace("\r", "").Replace("br/", "//");
        textData.AddPortion(newPortion);
    }

    textData.UpdateLayerData();

}

string ReplaceText(string lsak)
{
    StringBuilder sb = new StringBuilder(lsak);
    sb.Replace("#lsak_007#", "Power play.");
    sb.Replace("#lsak_008#", "Πιο επεκτατικοί κόσμοι. Γρήγοροι χρόνοι φόρτωσης. Υψηλά ποσοστά καρέ και ευρύτερο φάσμα χρωμάτων. Ένας υπολογιστής με Windows ήταν πάντα η καλύτερη πλατφόρμα για παιχνίδια—και στα Windows 11, γίνεται ακόμα καλύτερος.");
    sb.Replace("#lsak_009#", "Menemukan PC Windows 11 baru di Contoso.com.");
    sb.Replace("#lsak_010#", "Beli sekarang");

    sb.Replace("#lsak_011#", "Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua. Ut enim ad minim veniam, <font:Segoe UI Semibold> quis nostrud exercitation ullamco</font> laboris <font:Segoe UI Semibold>nisi ut aliquip</font> ex ea commodo consequat. <font:Segoe UI Semibold>Duis aute irure dolor in reprehenderit </font>in voluptate velit esse cillum dolore eu fugiat nulla pariatur.  <br/> Excepteur sint occaecat cupidatat non proident, sunt in culpa qui officia deserunt mollit anim id est laborum.");

    sb.Replace("\r", "");
    return sb.ToString();
}
{{< /highlight >}}

**PSDNET-1449. Awal dan akhir gaya atau paragraf muncul di tempat yang tidak benar pada pengeditan Lapisan Teks oleh ITextPortion**

{{< highlight csharp >}}
string sourceFilePSDEmail = "inputv2.psd";
string outputFile = "export.psd";

using (PsdImage image
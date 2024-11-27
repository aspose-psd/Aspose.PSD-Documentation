---
title: Aspose.PSD pro .NET 23.8 - Poznámky k vydání
type: docs
weight: 50
url: /cs/net/aspose-psd-pro-net-23-8-poznamky-k-vydani/
---

{{% alert color="primary" %}}

Tato stránka obsahuje poznámky k vydání pro [Aspose.PSD pro .NET 23.8](https://www.nuget.org/packages/Aspose.PSD/)

{{% /alert %}}

| **Klíč**    | **Souhrn**                                      | **Kategorie** |
|:------------|:----------------------------------------------|:--------|
| PSDNET-1566 | Přidání nového typu deformace (Flag)           | Funkce   |
| PSDNET-1621 | Přidání nových typů deformací: oblouk nahoru, oblouk dolů, sféra | Funkce   |
| PSDNET-1682 | Implementace nové metody PsdImage.AddPosterizeAdjustmentLayer pro přidání nové vrstvy Posterize | Funkce   |
| PSDNET-913  | Ztráta informací v PSD při pouhém otevření a uložení | Chyba  |
| PSDNET-1352 | Chyba při načítání obrázku | Chyba  |
| PSDNET-1553 | Chyba při načítání obrázku: Nelze převést objekt typu UnknownStructure na typ DescriptorStructure | Chyba  |
| PSDNET-1631 | Soubor změněný v knihovně třetí strany poškodí soubor PSD, ale lze ho otevřít v programu Photoshop | Chyba  |


## **Změny ve veřejném API**
# **Přidaná API:**
- M:Aspose.PSD.FileFormats.Psd.PsdImage.AddPosterizeAdjustmentLayer


# **Odebraná API:**
- Žádná


## **Příklady použití:**

**PSDNET-913. Ztráta informací v PSD při pouhém otevření a uložení**

{{< highlight csharp >}}
string src = "Původní soubor.psd";
string outputPsd = "out_Původní soubor.psd";
string outputPng = "out_Původní soubor.png";

using (var psdImage = (PsdImage)Image.Load(src))
{
    psdImage.Save(outputPsd);
    psdImage.Save(outputPng, new PngOptions() { ColorType = PngColorType.TruecolorWithAlpha });
}
{{< /highlight >}}

**PSDNET-1352. Chyba při načítání obrázku**

{{< highlight csharp >}}
string srcFile1 = "test_text.psd";
string srcFile2 = "test_smart_object.psd";

using (PsdImage psdImage = (PsdImage)Aspose.PSD.Image.Load(srcFile1))
{
}

using (PsdImage psdImage = (PsdImage)Aspose.PSD.Image.Load(srcFile2))
{
}
{{< /highlight >}}

**PSDNET-1553. Chyba při načítání obrázku: Nelze převést objekt typu UnknownStructure na typ DescriptorStructure**

{{< highlight csharp >}}
using (PsdImage newPsd = (PsdImage)new PsdImage(10, 10))
{
    newPsd.AddLayer(FillLayer.CreateInstance(FillType.Gradient));

    using (var memStream = new MemoryStream(DescriptorStructure.StructureKey + 1000))
    {
        newPsd.Save(memStream);

        memStream.Seek(DescriptorStructure.StructureKey, System.IO.SeekOrigin.Current);
        memStream.Write(new byte[1]);
        memStream.Position = 0;

        using (PsdImage psdImage = (PsdImage)Image.Load(memStream))
        {
            // Měl by se načíst správně
        }
    }
}
{{< /highlight >}}

**PSDNET-1631. Soubor změněný v knihovně třetí strany poškodí soubor PSD, ale lze ho otevřít v programu Photoshop**

{{< highlight csharp >}}
string sourceFile = "výstup.psd";
string outputFile = "export.png";

using (PsdImage img = (PsdImage)Image.Load(sourceFile, new PsdLoadOptions() { LoadEffectsResource = true }))
{
    img.Save(outputFile, new PngOptions() { CompressionLevel = 9, ColorType = PngColorType.TruecolorWithAlpha });
}
{{< /highlight >}}

**PSDNET-1566. Přidání nového typu deformace (Flag)**

{{< highlight csharp >}}
string sourceFile = "flag_deformace.psd";
string outputFile = "flag_export.png";

using (var psdImage = (PsdImage)Image.Load(sourceFile, new PsdLoadOptions() { AllowWarpRepaint = true, LoadEffectsResource = true }))
{
    psdImage.Save(outputFile, new PngOptions
    {
        ColorType = PngColorType.TruecolorWithAlpha
    });
}
{{< /highlight >}}

**PSDNET-1621. Přidání nových typů deformací: oblouk nahoru, oblouk dolů, sféra**

{{< highlight csharp >}}
string sourceFileArcUpper = "oblouk_nahoru_deformace.psd";
string sourceFileArcLower = "oblouk_dolů_deformace.psd";
string sourceFileBulge =  "nafouknutí_deformace.psd";

string outputFileArcUpper ="ArcNahoru_export.png";
string outputFileArcLower = "ArcDolů_export.png";
string outputFileBulge = "Nafouknutí_export.png";

using (var psdImage = (PsdImage)Image.Load(sourceFileArcUpper, new PsdLoadOptions() { AllowWarpRepaint = true, LoadEffectsResource = true }))
{
    psdImage.Save(outputFileArcUpper, new PngOptions {ColorType = PngColorType.TruecolorWithAlpha});
}

using (var psdImage = (PsdImage)Image.Load(sourceFileArcLower, new PsdLoadOptions() { AllowWarpRepaint = true, LoadEffectsResource = true }))
{
    psdImage.Save(outputFileArcLower, new PngOptions { ColorType = PngColorType.TruecolorWithAlpha });
}

using (var psdImage = (PsdImage)Image.Load(sourceFileBulge, new PsdLoadOptions() { AllowWarpRepaint = true, LoadEffectsResource = true }))
{
    psdImage.Save(outputFileBulge, new PngOptions { ColorType = PngColorType.TruecolorWithAlpha });
}
{{< /highlight >}}

**PSDNET-1682. Implementace nové metody PsdImage.AddPosterizeAdjustmentLayer pro přidání nové vrstvy Posterize**

{{< highlight csharp >}}
string srcFile = "zendeya.psd";
string outFile = "zendeya.psd.out.psd";

using (PsdImage psdImage = (PsdImage)Image.Load(srcFile))
{
    psdImage.AddPosterizeAdjustmentLayer();
    psdImage.Save(outFile);
}

// Ověření uložených změn
using (PsdImage image = (PsdImage)Image.Load(
    outFile,
    new PsdLoadOptions { LoadEffectsResource = true }))
{
    AssertAreEqual(2, image.Layers.Length);

    PosterizeLayer posterizeLayer = (PosterizeLayer)image.Layers[1];

    AssertAreEqual(true, posterizeLayer is PosterizeLayer);
}

void AssertAreEqual(object expected, object actual, string message = null)
{
    if (!object.Equals(expected, actual))
    {
        throw new Exception(message ?? "Objekty se neshodují.");
    }
}
{{< /highlight >}}

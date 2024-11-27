---
title: Aspose.PSD pro .NET 23.9 - Poznámky k vydání
type: docs
weight: 40
url: /cs/net/aspose-psd-pro-net-23-9-poznamky-k-vydani/
---

{{% alert color="primary" %}}

Tato stránka obsahuje poznámky k vydání pro [Aspose.PSD pro .NET 23.9](https://www.nuget.org/packages/Aspose.PSD/)

{{% /alert %}}

| **Klíč**     | **Souhrn**                                                                                                                | **Kategorie** |
|:------------|:---------------------------------------------------------------------------------------------------------------------------|:--------|
| PSDNET-1638 | Implementujte vytváření masky pro nové vrstvy úprav                                                                       | Funkce |
| PSDNET-1654 | Přidejte podporu pro smíchané vrstvy jako možnost skupinového míchání                                                    | Funkce |
| PSDNET-1194 | Soubor PSD s 16bitovým režimem barev nepoužívá masku pro vrstvy úprav                                                      | Chyba     |
| PSDNET-1235 | Nesprávné vykreslování závorek ve vrstvě textu                                                                             | Chyba     |
| PSDNET-1559 | Nelze aktualizovat styly ve vrstvách textu                                                                                 | Chyba     |
| PSDNET-1583 | Po exportu souboru PSD s režimem barev CMYK se barvy v exportovaném PSD rozpadnou                                        | Chyba     |
| PSDNET-1619 | Specifický soubor PSB vyvolává výjimku "Obdélník nemá žádnou společnou zpracovávanou oblast"                              | Chyba     |
| PSDNET-1648 | Chyba při načítání obrázku. Přetečení výpočtu: Výpočet aritmetiky způsobil přetečení                                      | Chyba     |


## **Změny ve veřejném API**
# **Přidaná API:**
- P:Aspose.PSD.FileFormats.Psd.Layers.Layer.BlendClippedElements
- T:Aspose.PSD.CustomFontHandler.CustomFontData
- M:Aspose.PSD.CustomFontHandler.CustomFontData.#ctor(System.String,System.Byte[])
- P:Aspose.PSD.CustomFontHandler.CustomFontData.FontName
- P:Aspose.PSD.CustomFontHandler.CustomFontData.FontData
- P:Aspose.PSD.FontSettings.GetSystemAlternativeFont
- P:Aspose.PSD.Graphics.PaintableImageOptions
- P:Aspose.PSD.Image.UsePalette
- M:Aspose.PSD.Region.Equals(System.Object)
- M:Aspose.PSD.Region.GetHashCode
- P:Aspose.PSD.StringFormat.CustomCharIdent
- M:Aspose.PSD.StringFormat.Equals(System.Object)
- M:Aspose.PSD.StringFormat.GetHashCode
- F:Aspose.PSD.StringFormatFlags.ExactAlignment


# **Odstraněná API:**
- Žádný


## **Příklady použití:**

**PSDNET-1638. Implementujte vytváření masky pro nové vrstvy úprav**

{{< highlight csharp >}}
string zdrojovýSoubor = "zendeya_BW.psd";
string cílovýSoubor = "zendeya_BW_out.psd";

using (var im = (PsdImage)Image.Load(zdrojovýSoubor))
{
    im.AddBlackWhiteAdjustmentLayer();

    im.Save(cílovýSoubor);
}

using (var im = (PsdImage)Image.Load(cílovýSoubor))
{
    Layer vrstva = im.Layers[1];

    AssertAreEqual((ushort)5, vrstva.ChannelsCount);
    AssertAreEqual((short)-2, vrstva.ChannelInformation[4].ChannelID);
}

void AssertAreEqual(object očekávané, object skutečné, string zpráva = null)
{
    if (!object.Equals(očekávané, skutečné))
    {
        throw new Exception(zpráva ?? "Objekty nejsou stejné.");
    }
}
{{< /highlight >}}

**PSDNET-1654. Přidejte podporu pro skupinové míchání vrstev smíšených jako možnost skupinového míchání**

{{< highlight csharp >}}
string zdrojovýSoubor = "příklad_zdroje.psd";
string výstupníPsd = "příklad_výstup.psd";
string výstupníPng = "příklad_výstup.png";

using (var obraz = (PsdImage)Image.Load(zdrojovýSoubor))
{
    obraz.Layers[1].BlendClippedElements = false;
    obraz.Save(výstupníPsd);
    obraz.Save(výstupníPng, new PngOptions());
}
{{< /highlight >}}

**PSDNET-1194. Soubor PSD s 16bitovým režimem barev nepoužívá masku pro vrstvy úprav**

{{< highlight csharp >}}
string zdrojovýSoubor = "zdroj.psd";
string výstupníPng = "aktuální.png";

using (var obraz = (PsdImage)Image.Load(zdrojovýSoubor))
{
    obraz.Save(výstupníPng, new PngOptions());
}
{{< /highlight >}}

**PSDNET-1235. Nesprávné vykreslování závorek ve vrstvě textu**

{{< highlight csharp >}}
string soubor = "soubor1.psd";
string výstup = "výstup_1235.png";

using (var psdObraz = (PsdImage)Image.Load(soubor))
{
    foreach (var vrstva in psdObraz.Layers)
    if (vrstva is TextLayer textováVrstva)
    textováVrstva.TextData.UpdateLayerData();

    var možnostiObrázku = new PsdOptions(psdObraz);
    psdObraz.Save(výstup, možnostiObrázku);
}
{{< /highlight >}}

**PSDNET-1559. Nelze aktualizovat styly ve vrstvách textu**

{{< highlight csharp >}}
string zdrojovýSoubor = "Příklad_VelikostPísma.psd";
string výstupníSoubor = "výstup_Příklad_VelikostPísma.psd";

using (var psdObraz = (PsdImage)Image.Load(zdrojovýSoubor, new PsdLoadOptions() { LoadEffectsResource = true }))
{
    var l1 = (TextLayer)psdObraz.Layers[4];
    var l2 = (TextLayer)psdObraz.Layers[5];

    var textovéPoložky1 = l1.TextData.ProducePortions(new string[] { "text1", "text2" }, l1.TextData.Items[0].Style, l1.TextData.Items[0].Paragraph);

    l1.TextData.RemovePortion(0);
    foreach (var položka in textovéPoložky1)
    {
        l1.TextData.AddPortion(položka);
    }

    var textovéPoložky2 = l2.TextData.ProducePortions(new string[] { "textová vrstva 1", "textová vrstva 22" }, l2.TextData.Items[0].Style, l2.TextData.Items[0].Paragraph);

    foreach (var položka in textovéPoložky2)
    {
        l2.TextData.AddPortion(položka);
    }

    l1.TextData.UpdateLayerData();
    l2.TextData.UpdateLayerData();

    psdObraz.Save(výstupníSoubor);
}
{{< /highlight >}}

**PSDNET-1583. Po exportu souboru PSD s režimem barev CMYK se barvy v exportovaném PSD rozpadnou**

{{< highlight csharp >}}
string zdrojovýSoubor = "kaňon.psd";
string výstupníSouborPng = "výstup_kaňon.png";

using (var výstupní proud = new MemoryStream())
{
    using (var psdObraz = (PsdImage)Image.Load(zdrojovýSoubor))
    {
        psdObraz.Save(výstupní proud);
    }

    výstupní proud.Position = 0;
    using (var psdObraz = (PsdImage)Image.Load(výstupní proud))
    {
        psdObraz.Save(výstupníSouborPng, new PngOptions());
    }
}
{{< /highlight >}}

**PSDNET-1619. Specifický soubor PSB vyvolává výjimku "Obdélník nemá žádnou společnou zpracovávanou oblast"**

{{< highlight csharp >}}
var vstup = "1619_src.psb";
var výstup = "1619_output.png";
using (PsdImage obrázek = (PsdImage)Image.Load(vstup, new PsdLoadOptions() { LoadEffectsResource = true }))
{
    obrázek.Save(výstup,
    new PngOptions() { CompressionLevel = 9, ColorType = PngColorType.TruecolorWithAlpha });
}
{{< /highlight >}}

**PSDNET-1648. Chyba při načítání obrázku. Přetečení výpočt: Výpočet aritmetiky způsobil přetečení**

{{< highlight csharp >}}
string zdrojovýSoubor = "9baa6962-f409-41ee-88da-418ea87bb56f_test_2.psd";

using (PsdImage obr = (PsdImage)PsdImage.Load(zdrojovýSoubor))
{
    Layer vrstva = obr.Layers[28];
    GrdmResource grdmResource = (GrdmResource)vrstva.Resources[0];

    AssertAreEqual("自定", grdmResource.GradientName);
}

void AssertAreEqual(object očekávané, object skutečné, string zpráva = null)
{
    if (!object.Equals(očekávané, skutečné))
    {
        throw new Exception(zpráva ?? "Objekty nejsou stejné.");
    }
}
{{< /highlight >}}

---
title: Aspose.PSD pro .NET 22.6 - Poznámky k vydání
type: docs
weight: 70
url: /cs/net/aspose-psd-pro-net-22-6-poznamky-k-vydani/
---

{{% alert color="primary" %}}

Tato stránka obsahuje poznámky k vydání pro [Aspose.PSD pro .NET 22.6](https://www.nuget.org/packages/Aspose.PSD/)

{{% /alert %}}

|**Klíč**|**Souhrn**|**Kategorie**|
| :- | :- | :- |
|PSDNET-940|Vytvořit API pro získání unikátního hashe pro podobné vrstvy v různých souborech|Vylepšení|
|PSDNET-678|Nesprávné vykreslování vrstvy s plněním vzorem v případě, kdy vzory jsou více než jedno a změnil se pořadí vrstev|Chyba|
|PSDNET-1125|Výjimka při načítání konkrétního souboru PSD s režimem barev CMYK|Chyba|


## **Změny ve veřejném API**
# **Přidaná API:**
- T:Aspose.PSD.FileFormats.Psd.Layers.LayerHashCalculator
- M:Aspose.PSD.FileFormats.Psd.Layers.LayerHashCalculator.#ctor(Aspose.PSD.FileFormats.Psd.Layers.Layer)
- M:Aspose.PSD.FileFormats.Psd.Layers.LayerHashCalculator.GetChannelsHash
- M:Aspose.PSD.FileFormats.Psd.Layers.LayerHashCalculator.GetBlendingHash
- M:Aspose.PSD.FileFormats.Psd.Layers.LayerHashCalculator.GetContentHash


# **Odebraná API:**
- Žádné


## **Příklady použití:**

**PSDNET-678. Nesprávné vykreslování vrstvy s plněním vzorem v případě, kdy vzory jsou více než jeden a změnil se pořadí vrstev**

{{< highlight csharp >}}
string sourceFile = "badPattern.psd";
string outputPng = "out_678.png";

using (var psdImage = (PsdImage)Image.Load(sourceFile))
{
    FillLayer layer1 = (FillLayer)psdImage.Layers[1];
    FillLayer layer2 = (FillLayer)psdImage.Layers[2];

    layer1.Update();
    layer2.Update();

    psdImage.Save(outputPng, new PngOptions());
}
{{< /highlight >}}

**PSDNET-940. Vytvořit API pro získání unikátního hashe pro podobné vrstvy v různých souborech**

{{< highlight csharp >}}
using Aspose.PSD;
using Aspose.PSD.FileFormats.Psd;
using Aspose.PSD.FileFormats.Psd.Layers;
using Aspose.PSD.ImageLoadOptions;

public class Program
{
    ...
}
{{< /highlight >}}

**PSDNET-1125. Výjimka při načítání konkrétního souboru PSD s režimem barev CMYK**

{{< highlight csharp >}}
string sourceFile = "02_alpha-channels.psd";
string outputPng = "out_1125.png";

using (PsdImage image = (PsdImage)Image.Load(sourceFile))
{
    image.Save(outputPng, new PngOptions());
}
{{< /highlight >}}
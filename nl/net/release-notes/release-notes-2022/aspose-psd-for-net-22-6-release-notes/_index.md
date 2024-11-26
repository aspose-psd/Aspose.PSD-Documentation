---
title: Aspose.PSD voor .NET 22.6 - Uitgave-opmerkingen
type: docs
weight: 70
url: /nl/net/aspose-psd-voor-dotnet-22-6-uitgave-opmerkingen/
---

{{% alert color="primary" %}}
Deze pagina bevat de uitgave-opmerkingen voor [Aspose.PSD voor .NET 22.6](https://www.nuget.org/packages/Aspose.PSD/)
{{% /alert %}}

|**Sleutel**|**Samenvatting**|**Categorie**|
| :- | :- | :- |
|PSDNET-940|Maak API om de unieke hash op te halen voor vergelijkbare lagen in verschillende bestanden|Verbetering|
|PSDNET-678|Onjuiste weergave van FillLayer met patroon in het geval dat er meer dan één patroon is en de volgorde van lagen is veranderd|Fout|
|PSDNET-1125|Uitzondering bij laden van specifiek PSD-bestand met CMYK-kleurmodus|Fout|


## **Openbare API-wijzigingen**
# **Toegevoegde API's:**
- T:Aspose.PSD.FileFormats.Psd.Layers.LayerHashCalculator
- M:Aspose.PSD.FileFormats.Psd.Layers.LayerHashCalculator.#ctor(Aspose.PSD.FileFormats.Psd.Layers.Layer)
- M:Aspose.PSD.FileFormats.Psd.Layers.LayerHashCalculator.GetChannelsHash
- M:Aspose.PSD.FileFormats.Psd.Layers.LayerHashCalculator.GetBlendingHash
- M:Aspose.PSD.FileFormats.Psd.Layers.LayerHashCalculator.GetContentHash


# **Verwijderde API's:**
- Geen


## **Gebruik voorbeelden:**

**PSDNET-678. Onjuiste weergave van FillLayer met patroon in het geval dat er meer dan één patroon is en de volgorde van lagen is gewijzigd**

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

**PSDNET-940. Maak API om de unieke hash op te halen voor vergelijkbare lagen in verschillende bestanden**

{{< highlight csharp >}}
using Aspose.PSD;
using Aspose.PSD.FileFormats.Psd;
using Aspose.PSD.FileFormats.Psd.Layers;
using Aspose.PSD.ImageLoadOptions;

public class Program
{
    //...
}
{{< /highlight >}}

**PSDNET-1125. Uitzondering bij laden van specifiek PSD-bestand met CMYK-kleurmodus**

{{< highlight csharp >}}
string sourceFile = "02_alpha-channels.psd";
string outputPng = "out_1125.png";

using (PsdImage image = (PsdImage)Image.Load(sourceFile))
{
    image.Save(outputPng, new PngOptions());
}
{{< /highlight >}}
---
title: Aspose.PSD voor .NET 24.3 - Release-opmerkingen
type: docs
weight: 100
url: /nl/net/aspose-psd-voor-net-24-3-release-opmerkingen/
---

{{% alert color="primary" %}}

Deze pagina bevat release-opmerkingen voor [Aspose.PSD voor .NET 24.3](https://www.nuget.org/packages/Aspose.PSD/)

{{% /alert %}}

| **Sleutel**  | **Samenvatting**                                                      | **Categorie** |
|:------------|:---------------------------------------------------------------------|:------------|
| PSDNET-1914 | [AI-formaat] Verminder laadtijd van grote multipage AI-afbeeldingen  |     Verbetering     |
| PSDNET-1905 | PSD-bestand na omzetting van 8-bits naar 16-bits werd onleesbaar     |     Fout     |
| PSDNET-1906 | PSD-bestand na omzetting van 8-bits naar 32-bits werd onleesbaar     |     Fout     |
| PSDNET-1921 | [AI-formaat] Los het probleem op met de weergave van de korte curve in AI-bestand |     Fout     |

## **Wijzigingen in openbare API**

# **Toegevoegde API's:**
- Geen

# **Verwijderde API's:**
- Geen

## **Gebruik voorbeelden:**

**PSDNET-1905. PSD-bestand na omzetting van 8-bits naar 16-bits werd onleesbaar**

{{< highlight csharp >}}
string sourceFile = Path.Combine(baseFolder, "test_smart_layer.psd");
string outputFile = Path.Combine(outputFolder, "export.psd");

using (var psdImage8 = (PsdImage)Image.Load(sourceFile))
{
    var psdOptions16 = new PsdOptions()
    {
        ChannelBitsCount = 16
    };

    psdImage8.Save(outputFile, psdOptions16);
}

using (var psdImage16 = (PsdImage)Image.Load(outputFile))
{
    if (psdImage16.GlobalLayerResources[0] is Lr16Resource)
    {
        // is ok
    }
    else
    {
        throw new Exception("Verkeerde globale resource, de eerste resource moet Lr16Resource zijn");
    }
}
{{< /highlight >}}

**PSDNET-1906. PSD-bestand na omzetting van 8-bits naar 32-bits werd onleesbaar**

{{< highlight csharp >}}
string sourceFile = Path.Combine(baseFolder, "test_smart_layer.psd");
string outputFile = Path.Combine(outputFolder, "export.psd");

using (var psdImage8 = (PsdImage)Image.Load(sourceFile))
{
    var psdOptions32 = new PsdOptions()
    {
        ChannelBitsCount = 32
    };

    psdImage8.Save(outputFile, psdOptions32);
}

using (var psdImage8 = (PsdImage)Image.Load(outputFile))
{
    if (psdImage8.GlobalLayerResources[0] is Lr32Resource)
    {
        // is ok
    }
    else
    {
        throw new Exception("Verkeerde globale resource, de eerste resource moet Lr32Resource zijn");
    }
}
{{< /highlight >}}

**PSDNET-1921. [AI-formaat] Los het probleem op met de weergave van de korte curve in AI-bestand**

{{< highlight csharp >}}
string sourceFile = Path.Combine(baseFolder, "shortCurve.ai");
string outputFilePath = Path.Combine(outputFolder, "shortCurve.png");

using (AiImage image = (AiImage)Image.Load(sourceFile))
{
    image.Save(outputFilePath, new PngOptions());
}
{{< /highlight >}}

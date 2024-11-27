---
title: Aspose.PSD pro .NET 24.3 - Poznámky k vydání
type: docs
weight: 100
url: /cs/net/aspose-psd-pro-net-24-3-poznamky-k-vydani/
---

{{% alert color="primary" %}}

Tato stránka obsahuje poznámky k vydání pro [Aspose.PSD pro .NET 24.3](https://www.nuget.org/packages/Aspose.PSD/)

{{% /alert %}}

| **Klíč**     | **Souhrn**                                                          | **Kategorie** |
|:------------|:---------------------------------------------------------------------|:------------|
| PSDNET-1914 | [AI Formát] Snížení doby načítání velkých vícestránkových obrazů AI         |     Vylepšení     |
| PSDNET-1905 | PSD soubor po převedení z 8 bitů na 16 bitů se stal nečitelným |     Chyba     |
| PSDNET-1906 | PSD soubor po převedení z 8 bitů na 32 bitů se stal nečitelným |     Chyba     |
| PSDNET-1921 | [AI Formát] Oprava vykreslování krátké křivky v AI souboru                 |     Chyba     |

## **Veřejné změny API**
# **Přidaná API:**
- Žádná

# **Odstraněná API:**
- Žádná

## **Příklady použití:**

**PSDNET-1905. PSD soubor po převedení z 8 bitů na 16 bitů se stal nečitelným**

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
        // je v pořádku
    }
    else
    {
        throw new Exception("Nesprávný globální zdroj, první zdroj by měl být Lr16Resource");
    }
}
{{< /highlight >}}

**PSDNET-1906. PSD soubor po převedení z 8 bitů na 32 bitů se stal nečitelným**

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
        // je v pořádku
    }
    else
    {
        throw new Exception("Nesprávný globální zdroj, první zdroj by měl být Lr32Resource");
    }
}
{{< /highlight >}}

**PSDNET-1921. [AI Formát] Oprava vykreslování krátké křivky v AI souboru**

{{< highlight csharp >}}
string sourceFile = Path.Combine(baseFolder, "shortCurve.ai");
string outputFilePath = Path.Combine(outputFolder, "shortCurve.png");

using (AiImage image = (AiImage)Image.Load(sourceFile))
{
    image.Save(outputFilePath, new PngOptions());
}
{{< /highlight >}}

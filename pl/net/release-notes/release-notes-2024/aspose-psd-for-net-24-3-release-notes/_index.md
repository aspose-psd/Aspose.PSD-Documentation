---
title: Aspose.PSD dla .NET 24.3 - Notatki dotyczące wydania
type: docs
weight: 100
url: /pl/net/aspose-psd-dla-net-24-3-notatki-dotyczace-wydania/
---

{{% alert color="primary" %}}

Ta strona zawiera notatki dotyczące wydania [Aspose.PSD dla .NET 24.3](https://www.nuget.org/packages/Aspose.PSD/)

{{% /alert %}}

| **Klucz**    | **Podsumowanie**                                                      | **Kategoria**  |
|:------------|:---------------------------------------------------------------------|:------------|
| PSDNET-1914 | [Format AI] Zredukowanie czasu ładowania dużych obrazów AI wielostronicowych |     Ulepszenie     |
| PSDNET-1905 | Po konwersji plik PSD z 8 bitów na 16 bitów stał się nieczytelny      |     Błąd     |
| PSDNET-1906 | Po konwersji pliku PSD z 8 bitów na 32 bity stał się nieczytelny      |     Błąd     |
| PSDNET-1921 | [Format AI] Naprawienie renderowania krótkiej krawędzi w pliku AI     |     Błąd     |

## **Zmiany w API publicznym**
# **Dodane interfejsy API:**
- Brak

# **Usunięte interfejsy API:**
- Brak

## **Przykłady użycia:**

**PSDNET-1905. Po konwersji pliku PSD z 8 bitów na 16 bitów stał się nieczytelny**

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
        throw new Exception("Nieprawidłowy zasób globalny, pierwszy zasób powinien być typu Lr16Resource");
    }
}
{{< /highlight >}}

**PSDNET-1906. Po konwersji pliku PSD z 8 bitów na 32 bity stał się nieczytelny**

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
        throw new Exception("Nieprawidłowy zasób globalny, pierwszy zasób powinien być typu Lr32Resource");
    }
}
{{< /highlight >}}

**PSDNET-1921. [Format AI] Naprawienie renderowania krótkiej krawędzi w pliku AI**

{{< highlight csharp >}}
string sourceFile = Path.Combine(baseFolder, "shortCurve.ai");
string outputFilePath = Path.Combine(outputFolder, "shortCurve.png");

using (AiImage image = (AiImage)Image.Load(sourceFile))
{
    image.Save(outputFilePath, new PngOptions());
}
{{< /highlight >}}

---
title: Notatki dotyczące publikacji Aspose.PSD dla Python via .NET 24.3
type: docs
weight: 10
url: /pl/net/aspose-psd-for-python-via-net-24-3-release-notes/
---

{{% alert color="primary" %}}

Ta strona zawiera notatki dotyczące publikacji [Aspose.PSD dla Python via .NET 24.3](https://pypi.org/project/aspose-psd/)

{{% /alert %}}

| **Klucz**     | **Podsumowanie**                                                    | **Kategoria**|
|:------------- |:-------------------------------------------------------------------|:------------|
| PSDPYTHON-42  | [Format AI] Skróć czas wczytywania dużych obrazów AI z wieloma stronami | Poprawki  |
| PSDPYTHON-45  | Po konwersji pliku PSD z 8 bitów na 16 bitów stał się nieczytelny     |     Błąd    |
| PSDPYTHON-46  | Po konwersji pliku PSD z 8 bitów na 32 bity stał się nieczytelny      |     Błąd    |
| PSDPYTHON-47  | [Format AI] Napraw renderowanie krótkiej krzywej w pliku AI           |     Błąd    |



## **Zmiany w API publicznym**
# **Dodane API:**
- Brak

# **Usunięte API:**
- Brak


## **Przykłady użycia:**

**PSDPYTHON-42. [Format AI] Skróć czas wczytywania dużych obrazów AI z wieloma stronami**

{{< highlight python >}}
   # Brak przykładu
{{< /highlight >}}

**PSDPYTHON-45. Po konwersji pliku PSD z 8 bitów na 16 bitów stał się nieczytelny**

{{< highlight python >}}
        sourceFile = "test_smart_layer.psd"
        outputFile = "export.psd"

        with PsdImage.load(sourceFile) as psdImage8:
            psdOptions16 = PsdOptions()
            psdOptions16.channel_bits_count = 16

            psdImage8.save(outputFile, psdOptions16)

        with PsdImage.load(outputFile) as image:
            psdImage16 = cast(PsdImage, image)

            testResource = as_of(psdImage16.global_layer_resources[5], Lr16Resource)
            if testResource is not None:
                # jest ok
                pass
            else:
                raise Exception("Nieprawidłowy zasób globalny, pierwszy zasób powinien być Lr16Resource")
{{< /highlight >}}

**PSDPYTHON-46. Po konwersji pliku PSD z 8 bitów na 32 bity stał się nieczytelny**


{{< highlight python >}}
        sourceFile = "test_smart_layer.psd"
        outputFile = "export.psd"

        with PsdImage.load(sourceFile) as psdImage8:
            psdOptions32 = PsdOptions()
            psdOptions32.channel_bits_count = 32

            psdImage8.save(outputFile, psdOptions32)

        with PsdImage.load(outputFile) as image:
            psdImage32 = cast(PsdImage, image)

            testResource = as_of(psdImage32.global_layer_resources[5], Lr32Resource)
            if testResource is not None:
                # jest ok
                pass
            else:
                raise Exception("Nieprawidłowy zasób globalny, pierwszy zasób powinien być Lr32Resource")
{{< /highlight >}}

**PSDPYTHON-47. [Format AI] Napraw renderowanie krótkiej krzywej w pliku AI**

{{< highlight python >}}
        sourceFile = "shortCurve.ai"
        outputFilePath = "shortCurve.png"

        with AiImage.load(sourceFile) as image:
            image.save(outputFilePath, PngOptions())
{{< /highlight >}}

---
title: Vydání Aspose.PSD pro Python via .NET 24.3 - Poznámky k vydání
type: docs
weight: 10
url: /cs/net/aspose-psd-pro-python-pres-net-24-3-poznamky-k-vydani/
---

{{% alert color="primary" %}}

Tato stránka obsahuje poznámky k vydání pro [Aspose.PSD pro Python via .NET 24.3](https://pypi.org/project/aspose-psd/)

{{% /alert %}}

| **Klíč**      | **Souhrn**                                                          | **Kategorie**|
|:-------------|:---------------------------------------------------------------------|:------------|
| PSDPYTHON-42 | [AI Formát] Snížení času načítání velkých vícestránkových obrázků AI         | Vylepšení |
| PSDPYTHON-45 | Soubor PSD po konverzi z 8 bitů na 16 bitů se stal nečitelným |     Chyba     |
| PSDPYTHON-46 | Soubor PSD po konverzi z 8 bitů na 32 bitů se stal nečitelným |     Chyba     |
| PSDPYTHON-47 | [AI Formát] Oprava renderování Short Curve v souboru AI                 |     Chyba     |



## **Změny v veřejném API**
# **Přidaná API:**
- Žádné

# **Odebraná API:**
- Žádné


## **Příklady použití:**

**PSDPYTHON-42. [AI Formát] Snížení času načítání velkých vícestránkových obrázků AI**

{{< highlight python >}}
   # Žádný vzor
{{< /highlight >}}

**PSDPYTHON-45. Soubor PSD po konverzi z 8 bitů na 16 bitů se stal nečitelným**

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
                # je v pořádku
                pass
            else:
                raise Exception("Nesprávný globální zdroj, první zdroj by měl být Lr16Resource")
{{< /highlight >}}

**PSDPYTHON-46. Soubor PSD po konverzi z 8 bitů na 32 bitů se stal nečitelným**


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
                # je v pořádku
                pass
            else:
                raise Exception("Nesprávný globální zdroj, první zdroj by měl být Lr32Resource")
{{< /highlight >}}

**PSDPYTHON-47. [AI Formát] Oprava renderování Short Curve v souboru AI**

{{< highlight python >}}
        sourceFile = "shortCurve.ai"
        outputFilePath = "shortCurve.png"

        with AiImage.load(sourceFile) as image:
            image.save(outputFilePath, PngOptions())
{{< /highlight >}}

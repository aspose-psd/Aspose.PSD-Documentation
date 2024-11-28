---
title: Aspose.PSD voor Python via .NET 24.3 - Release-opmerkingen
type: docs
weight: 10
url: /nl/net/aspose-psd-voor-python-via-net-24-3-release-opmerkingen/
---

{{% alert color="primary" %}}

Deze pagina bevat release-opmerkingen voor [Aspose.PSD voor Python via .NET 24.3](https://pypi.org/project/aspose-psd/)

{{% /alert %}}

| **Sleutel**   | **Samenvatting**                                                     | **Categorie**|
|:--------------|:---------------------------------------------------------------------|:------------|
| PSDPYTHON-42  | [AI-indeling] Verminder de laadtijd van grote AI-afbeeldingen met meerdere pagina's | Verbetering  |
| PSDPYTHON-45  | PSD-bestand na de conversie van 8-bits naar 16-bits werd onleesbaar | Fout        |
| PSDPYTHON-46  | PSD-bestand na de conversie van 8-bits naar 32-bits werd onleesbaar | Fout        |
| PSDPYTHON-47  | [AI-indeling] Los het probleem met de korte curve-weergave in AI-bestand op | Fout        |



## **Openbare API-wijzigingen**
# **Toegevoegde API's:**
- Geen

# **Verwijderde API's:**
- Geen


## **Gebruik voorbeelden:**

**PSDPYTHON-42. [AI-indeling] Verminder de laadtijd van grote AI-afbeeldingen met meerdere pagina's**

{{< highlight python >}}
   # Geen voorbeeld
{{< /highlight >}}

**PSDPYTHON-45. PSD-bestand na de conversie van 8-bits naar 16-bits werd onleesbaar**

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
                # is ok
                pass
            else:
                raise Exception("Verkeerde globale resource, de eerste resource moet een Lr16Resource zijn")
{{< /highlight >}}

**PSDPYTHON-46. PSD-bestand na de conversie van 8-bits naar 32-bits werd onleesbaar**


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
                # is ok
                pass
            else:
                raise Exception("Verkeerde globale resource, de eerste resource moet een Lr32Resource zijn")
{{< /highlight >}}

**PSDPYTHON-47. [AI-indeling] Los het probleem met de korte curve-weergave in AI-bestand op**

{{< highlight python >}}
        sourceFile = "shortCurve.ai"
        outputFilePath = "shortCurve.png"

        with AiImage.load(sourceFile) as image:
            image.save(outputFilePath, PngOptions())
{{< /highlight >}}

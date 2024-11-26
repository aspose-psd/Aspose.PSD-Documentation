---
title: Aspose.PSD voor .NET 21.6 - Release-opmerkingen
type: docs
weight: 70
url: /nl/net/aspose-psd-voor-net-21-6-release-opmerkingen/
---

{{% alert color="primary" %}}

Deze pagina bevat release-opmerkingen voor [Aspose.PSD voor .NET 21.6](https://www.nuget.org/packages/Aspose.PSD/)

{{% /alert %}}

|**Belangrijk**|**Samenvatting**|**Categorie**|
| :- | :- | :- |
|PSDNET-546|Uitsnijdmasker voor een groep wordt niet correct weergegeven|Fout|
|PSDNET-547|Regulier of vector masker voor een laaggroep wordt genegeerd bij het renderen|Fout|
|PSDNET-647|PSD-afbeelding met uitgeschakelde vectorlaagmaskers bij opslaan activeert vectormaskers|Fout|
|PSDNET-786|Uitzondering bij het maken van een TextLayer met tekst langer dan 255 tekens|Fout|
|PSDNET-900|Tekst van de Text-laag kan niet worden weergegeven op Linux|Verbetering|

## **Wijzigingen in de openbare API**
# **Toegevoegde API's:**
- Geen

# **Verwijderde API's:**
- Geen

## **Gebruik voorbeelden:**

**PSDNET-546. Uitsnijdmasker voor een groep wordt niet correct weergegeven**

{{< highlight csharp >}}
            string sourceFileName = "AppleClip.psd";
            string outputFileName = "result.png";

            using (PsdImage image = (PsdImage)Image.Load(sourceFileName))
            {
                image.Save(outputFileName, new PngOptions());
            }
{{< /highlight >}}

**PSDNET-547. Regulier of vector masker voor een laaggroep wordt genegeerd bij het renderen**

{{< highlight csharp >}}
        string sourceFileName = "Stripes3Mask.psd";
        string outputFileName = "OutputStripes3Mask.png";
        using (PsdImage image = (PsdImage)Image.Load(sourceFileName))
        {
            image.Save(outputFileName, new PngOptions());
        }
{{< /highlight >}}

**PSDNET-647. PSD-afbeelding met uitgeschakelde vectorlaagmaskers bij opslaan activeert vectormaskers**

{{< highlight csharp >}}
            string sourceFileName = "FourWithMasksVd.psd";
            string outputFileName = "FourWithMasksVdOutput.psd";

            using (PsdImage image = (PsdImage)Image.Load(sourceFileName))
            {
                image.Save(outputFileName);
            }
{{< /highlight >}}

**PSDNET-786. Uitzondering bij het maken van een TextLayer met tekst langer dan 255 tekens**

{{< highlight csharp >}}
            string output = "output.psd";

            using (var image = new PsdImage(100, 100))
            {
                string text = new string('a', 256);
                image.AddTextLayer(text, Rectangle.Empty);

                image.Save(output);
            }
{{< /highlight >}}

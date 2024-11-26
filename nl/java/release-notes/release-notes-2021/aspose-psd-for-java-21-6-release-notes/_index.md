---
title: Aspose.PSD voor Java 21.6 - Release-opmerkingen
type: docs
weight: 40
url: /nl/java/aspose-psd-voor-java-21-6-release-opmerkingen/
---

{{% alert color="primary" %}} Deze pagina bevat release-opmerkingen voor [Aspose.PSD voor Java 21.6](https://downloads.aspose.com/psd/java/new-releases/aspose.psd-voor-java-21.6/) {{% /alert %}}

|**Belangrijkste**|**Samenvatting**|**Categorie**|
| :- | :- | :- |
|PSDJAVA-351|Masker voor een groep wordt niet correct weergegeven|Fout|
|PSDJAVA-352|Regulier of vector masker voor een lagen groep wordt genegeerd bij het renderen|Fout|
|PSDJAVA-353|PSD-afbeelding met uitgeschakelde vectorlaagmaskers bij opslaan schakelt vectormaskers in|Fout|
|PSDJAVA-354|Uitzondering bij het maken van een TextLayer met tekst langer dan 255 tekens|Fout|

# **Wijzigingen in openbare API**
# **Toegevoegde API's:**
- Geen

# **Verwijderde API's:**
- Geen

# **Gebruikvoorbeelden:**

**PSDJAVA-351. Masker voor een groep wordt niet correct weergegeven**

{{< highlight java >}}
        String sourceFileName = "AppleClip.psd";
        String outputFileName = "result.png";

        PsdImage image = (PsdImage) Image.load(sourceFileName);
        try
        {
            image.save(outputFileName, new PngOptions());
        }finally {
            image.dispose();
        }
{{< /highlight >}}

**PSDJAVA-352. Regulier of vector masker voor een lagen groep wordt genegeerd bij het renderen**

{{< highlight java >}}
        String sourceFileName = "Stripes3Mask.psd";
        String outputFileName = "OutputStripes3Mask.png";

        PsdImage image = (PsdImage)Image.load(sourceFileName);
        try
        {
            image.save(outputFileName, new PngOptions());
        }finally {
            image.dispose();
        }
{{< /highlight >}}

**PSDJAVA-353. PSD-afbeelding met uitgeschakelde vectorlaagmaskers bij opslaan schakelt vectormaskers in**

{{< highlight java >}}
        String sourceFileName = "FourWithMasksVd.psd";
        String outputFileName = "FourWithMasksVdOutput.psd";

        PsdImage image = (PsdImage) Image.load(sourceFileName);
        try
        {
            image.save(outputFileName);
        }finally {
            image.dispose();
        }
{{< /highlight >}}

**PSDJAVA-354. Uitzondering bij het maken van een TextLayer met tekst langer dan 255 tekens**

{{< highlight java >}}
        String output = "output.psd";

        PsdImage image = new PsdImage(100, 100);
        try
        {
            char[] chars = new char[256];
            Arrays.fill(chars, '*');
            String text = new String(chars);
            image.addTextLayer(text, Rectangle.getEmpty());

            image.save(output);
        }finally {
            image.dispose();
        }
{{< /highlight >}}

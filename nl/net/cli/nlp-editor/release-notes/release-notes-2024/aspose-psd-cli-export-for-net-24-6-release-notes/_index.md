---
title: Aspose.PSD CLI NLP Editor voor .NET 24.6 - Release-opmerkingen
type: docs
weight: 90
url: /nl/net/cli/nlp-editor/aspose-psd-nlp-editor-cli-app-voor-net-24-6-release-opmerkingen/
---
{{% alert color="primary" %}}

Deze pagina bevat release-opmerkingen voor [Aspose.PSD CLI NLP Editor voor .NET 24.6](https://www.nuget.org/packages/Aspose.PSD.CLI.NLP.Editor/)

{{% /alert %}}

| **Sleutel**  | **Samenvatting**                                                                             | **Categorie** |
|:------------|:----------------------------------------------------------------------------------------------|:-------------|
| PSDNET-2110 | Initiële vrijgave van Aspose.PSD CLI-apps: Aspose.PSD.CLI.Export en Aspose.PSD.CLI.NLP.Editor |  Verbetering |


## **Gebruik voorbeelden:**

**PSDNET-2110. Initiële vrijgave van de toepassing Aspose.PSD CLI NLP-editor**

## **Gebruik vanaf de commandoregel:**

{{% alert color="primary" %}}
Installeer eerst deze dotnet-tool:
{{< highlight bash >}}dotnet tool install --global Aspose.PSD.CLI.NLP.Editor --version 24.6.0{{< /highlight >}}

We raden aan om vóór het eerste gebruik de volgende opdracht uit te voeren:
{{< highlight bash >}}Aspose.PSD.CLI.NLP.Editor --setup nlp.cli{{< /highlight >}}
Na deze opdracht kunt u deze toepassing uitvoeren met de verkorte naam nlp.cli in plaats van Aspose.PSD.CLI.NLP.Editor. U kunt uw eigen verkorte naam opgeven.
{{% /alert %}}

**Voorbeelden van gebruik**

1. Met deze opdracht wordt het eerste gevonden bestand (dat kan worden geopend met aspose.psd) in de huidige map geconverteerd en als png-bestand met transparantie opgeslagen. Ook wordt de licentie ingesteld. U hoeft de licentie slechts één keer op te geven. Bij volgende uitvoeringen wordt de licentie van het gespecificeerde pad gebruikt. Deze opdracht geeft het uitgebreide logboek van NLP-verwerking weer, indien beschikbaar.
{{< highlight bash >}}nlp.cli Bestand van deze map naar png-formaat met alpha converteren --license "C:\Aspose\LicenseFile.lic --verbose "{{< /highlight >}}

2. Met deze opdracht wordt het bestand met de meest gelijkaardige naam aan "smth.psd" gezocht. Vervolgens wordt het contrast aangepast en wordt het opgeslagen als jpeg met de beste kwaliteit. De naam van het uitvoerbestand wordt afgedrukt. Het zal smth.jpg zijn.
{{< highlight bash >}}Contrast aanpassen op 10 van laag met de naam ellipse in bestand smth.psd en opslaan als output.jpg met de beste kwaliteit{{< /highlight >}}

3. Met deze opdracht wordt het bestand op het gespecificeerde pad gevonden en wordt de grootte ervan met 25% verkleind. Het uitvoerbestand wordt afgedrukt. Het wordt opgeslagen in de huidige map van de console.
{{< highlight bash >}}Bestand C:\Users\someuser\Desktop\input.psd naar 25% verkleinen{{< /highlight >}}

4. Met deze opdracht wordt het bestand input.psd gevonden in C:\Users\someuser\Desktop\. Vervolgens wordt de laag met index 3 gezocht en wordt deze aangepast naar een breedte van 50px en een hoogte van 100px. Vervolgens wordt deze laag opgeslagen als PDF in C:\Users\someuser\Desktop\output.pdf.
{{< highlight bash >}}Laag met index 3 van C:\Users\someuser\Desktop\input.psd aanpassen naar een breedte van 50 en een hoogte van 100 en opslaan als C:\Users\someuser\Desktop\output.pdf{{< /highlight >}}

 5. Met deze opdracht wordt smth.psd in de huidige map geopend, maar alle effecten worden uitgeschakeld. Vervolgens wordt dit bestand geconverteerd naar BMP-formaat en opgeslagen als output.bmp in de huidige map.
 {{< highlight bash >}}Open smth.psd zonder effecten en opslaan als output.bmp{{< /highlight >}}

**Disclaimer**

Dit is een experimentele toepassing. Probeer het uit en laat feedback achter. Alle feedback wordt zeer gewaardeerd. We streven ernaar om toepassingen zonder code naar een hoger niveau te tillen. Gemakkelijke integratie in elk buildproces of bedrijfsproces is ons doel.

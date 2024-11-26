---
title: Aspose.PSD CLI NLP Editor-applicatie voor .NET
type: docs
weight: 10
url: /nl/net/cli/nlp-editor/
is_root: false
keywords: CLI Photoshop Tool NLP Natural-Language-Processing PSD Console C# Library PSD API
description: Aspose.PSD-gebaseerde NLP Editor CLI-toepassing voor PSD-, PSB- en AI-bestandsindelingen. Geen code CI/CD-automatisering. Ondersteunt natuurlijke taalverwerking voor het bewerken van PSD-bestanden. Schrijf gewoon uw verzoek in natuurlijke taal om verschillende bewerkingen uit te voeren zoals conversie, aanpassing, formaataanpassing en meer. Het vereist geen installatie van Adobe Photoshop of Adobe Illustrator en kan worden uitgevoerd vanuit de console zonder extra code.
---

**![Aspose.PSD voor .NET-productlogo](home_1.png)**

**Welkom bij de Aspose.PSD NLP Editor CLI-toepassing voor .NET**

De Aspose.PSD CLI NLP Editor-applicatie is een lichtgewicht console-hulpprogramma voor het bewerken van PSD-bestanden met behulp van natuurlijke taalopdrachten. Eenvoudige integratie in CI/CD-pijplijnen.

**Disclaimer**

Dit is een experimentele toepassing. Probeer het alstublieft uit en laat feedback achter. Alle feedback wordt zeer op prijs gesteld. We willen de No-Code-toepassing naar een hoger niveau tillen. Gemakkelijke integratie met elk bouwpijplijn of bedrijfsproces is ons doel.

**Belangrijkste functionaliteiten van de Aspose.PSD NLP Editor CLI-toepassing voor .NET**

1. Voer bewerkingen uit op PSD-, PSB- en AI-bestanden met behulp van natuurlijke taalopdrachten.
2. Ondersteunt verschillende bewerkingen zoals conversie, aanpassing, formaataanpassing en meer.
3. Geen-code CI/CD-automatisering.
4. Ondersteunt het schrijven van verzoeken in natuurlijke taal voor het bewerken van PSD-bestanden.

## **Gebruik vanaf de opdrachtregel:**

{{% alert color="primary" %}}
Installeer eerst deze dotnet-tool:
{{< highlight bash >}}dotnet tool install --global Aspose.PSD.CLI.NLP.Editor --version 24.6.0{{< /highlight >}}

We raden aan om vóór het eerste gebruik de volgende opdracht uit te voeren:
{{< highlight bash >}}Aspose.PSD.CLI.NLP.Editor --setup nlp.cli{{< /highlight >}}
Na deze opdracht kunt u deze toepassing uitvoeren met de verkorte naam nlp.cli in plaats van Aspose.PSD.CLI.NLP.Editor. U kunt uw eigen verkorte naam opgeven.
{{% /alert %}}

**Beschikbare parameters voor de Aspose.PSD.CLI.Crop-toepassing**

| **Argument** | **Beschrijving**                       |
|:-------------|:--------------------------------------|
| willekeurige tekst | Vereist. Uw opdracht in natuurlijke taal om een PSD- of PSB-bestand bij te werken |
| licentie     | Pad naar de licentie.                  |
| uitgebreid   | Toon meer informatie over een specifieke opdracht. |
| setup        | Maakt een bat-bestand in de gereedschapsmap voor snelle oproep vanuit de console. Voorbeeld: --setup psd.nlp. Dan kunt u het hulpprogramma oproepen met de opdracht psd.nlp |

**Voorbeelden van gebruik**

1. Met deze opdracht wordt het eerste gevonden bestand (dat kan worden geopend met Aspose.PSD) uit de huidige map geconverteerd en opgeslagen in png-indeling met transparantie. Ook wordt de licentie ingesteld. U hoeft de licentie slechts één keer op te geven. Bij volgende uitvoeringen wordt de licentie gebruikt vanuit het opgegeven pad. Deze opdracht toont het uitgebreide logboek van NLP-verwerking, indien beschikbaar.
{{< highlight bash >}}
  nlp.cli Converteer bestand van deze map naar png-indeling met alpha --license "C:\Aspose\LicenseFile.lic --verbose "
{{< /highlight >}}

2. Deze opdracht zoekt het bestand met de meest soortgelijke naam als "smth.psd". Vervolgens zal het de contrast aanpassen en opslaan in jpeg met de beste kwaliteit. De naam van het uitvoerbestand wordt afgedrukt. Het zal smth.jpg zijn.
{{< highlight bash >}}
Pas het contrast aan op 10 van laag met de naam ellips in bestand smth.psd en sla het op als output.jpg met de beste kwaliteit
{{< /highlight >}}

3. Deze opdracht zal het bestand op het opgegeven pad vinden en de grootte ervan met 25% verminderen. Het uitvoerbestand wordt afgedrukt. Het wordt opgeslagen in de huidige map van de console.
{{< highlight bash >}}
Formaat wijzigen van bestand C:\Gebruikers\someuser\Bureaublad\input.psd naar 25%
{{< /highlight >}}

4. Deze opdracht zal het bestand input.psd vinden in C:\Gebruikers\someuser\Bureaublad\. Vervolgens zal het de laag met index 3 vinden en deze wijzigen naar een breedte van 50px en een hoogte van 100px. Vervolgens wordt deze laag opgeslagen als PDF in C:\Gebruikers\someuser\Bureaublad\output.pdf
{{< highlight bash >}}
Wijzig laag met index 3 van C:\Gebruikers\someuser\Bureaublad\input.psd naar breedte 50 en hoogte 100 en sla op als C:\Gebruikers\someuser\Bureaublad\output.pdf
{{< /highlight >}}

5. Deze opdracht zal smth.psd openen in de huidige map, maar alle effecten worden uitgeschakeld. Vervolgens wordt dit bestand geconverteerd naar BMP-indeling en opgeslagen als output.bmp in de huidige map.
{{< highlight bash >}}
Open smth.psd zonder effecten en sla op als output.bmp
{{< /highlight >}}

**Controleer alstublieft andere [Aspose.PSD CLI-toepassingen](https://docs.aspose.com/psd/net/cli) voor .NET als u ondersteuning nodig heeft voor PSD-, PSB- en AI-indelingen voor uw werkstroom**

1. [Aspose.PSD CLI Converteren](/psd/nl/net/cli/converteren)
2. [Aspose.PSD CLI Bijsnijden](/psd/nl/net/cli/bijsnijden)
3. [Aspose.PSD CLI Formaat wijzigen](/psd/nl/net/cli/formaat-wijzigen)
4. [Aspose.PSD CLI Exporteren](/psd/nl/net/cli/exporteren)
5. [Aspose.PSD CLI NLP Editor](/psd/nl/net/cli/nlp-editor)

**Bekijk ook Aspose.PSD voor .NET of [andere platforms]**

Aspose.PSD CLI-toepassingen is een kant-en-klare oplossing voor populaire bewerkingen. Als u een flexibele oplossing nodig heeft, bekijk dan de volledige versie van Aspose.PSD

1. [Aspose.PSD voor .NET](https://releases.aspose.com/psd/net/)
2. [Aspose.PSD voor Java](https://releases.aspose.com/psd/java/) 
3. [Aspose.PSD voor Python via .NET](https://releases.aspose.com/psd/python-net/)

## **Aspose.PSD voor .NET-bronnen**

Hier zijn de links naar enkele nuttige bronnen die u nodig heeft om uw taken uit te voeren.

- [Aspose.PSD CLI-toepassingen voor .NET Online Documentatie](/psd/nl/net/cli/conversie)
- [Aspose.PSD voor CLI-toepassingen voor .NET Release-opmerkingen](/psd/nl/net/cli/conversie/release-opmerkingen/)
- [Aspose.PSD voor CLI-toepassingen .NET-productpagina](https://products.aspose.com/psd/net/cli)
- [Aspose.PSD voor .NET API Referentiegids](https://reference.aspose.com/net/psd)
- [Voorbeelden downloaden op GitHub Repository](https://github.com/aspose-psd/CLI-Applications)
- [Aspose.PSD voor .NET Gratis ondersteuningsforum](https://forum.aspose.com/c/psd)
- [Aspose.PSD voor .NET Betaalde ondersteunings Helpdesk](https://helpdesk.aspose.com/)

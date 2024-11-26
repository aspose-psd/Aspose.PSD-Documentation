---
title: Licentie
type: docs
weight: 60
url: /nl/java/licentie/
---

## **Beperkingen van de Evaluatieversie**
U kunt een evaluatieversie van Aspose.PSD voor Java downloaden van de [downloadpagina](http://maven.aspose.com/repository/simple/ext-release-local/com/aspose/aspose-psd/). De evaluatieversie biedt dezelfde functies als de volledig gelicentieerde versie van de component, met een paar beperkingen. Wanneer u Aspose.PSD aanschaft, worden eventuele beperkingen van de geïnstalleerde evaluatie verwijderd zodra de licentie wordt toegepast.

De evaluatieversie van Aspose.PSD voor Java biedt volledige productfunctionaliteit, met slechts twee beperkingen:

- **Een watermerk op elk beeld**: Elk beeld dat u opslaat, wijzigt of exporteert, bevat een watermerk met de tekst "Alleen evaluatie. Gemaakt met Aspose.PSD. Copyright 2018-2019 Aspose Pty Ltd.". Bij kleine afbeeldingen, waar het volledige watermerk niet past, worden twee diagonale lijnen over de afbeelding geplaatst in plaats van het watermerk.
- **Geen ondersteuning voor de kernfunctionaliteit van tekenen**: In evaluatiemodus kunnen afbeeldingspixels niet worden geladen of opgeslagen in de afbeelding. Gebruik in plaats daarvan de geavanceerde tekenfunctionaliteit om afbeeldingen te tekenen. Deze beperking heeft invloed op functionaliteiten die afhankelijk zijn van de kernfunctionaliteit van tekenen. Aspose.PSD voor Java stelt u in staat om uw eigen bestandsindeling te registreren. Deze functie is echter afhankelijk van de kernfunctionaliteit van tekenen, dus het heeft geen zin om het in evaluatiemodus te gebruiken omdat u de inhoud van die bestanden niet kunt wijzigen.

{{% alert color="primary" %}}

Als u Aspose.PSD voor Java wilt testen zonder de evaluatiebeperkingen, vraag dan een tijdelijke licentie van 30 dagen aan. Raadpleeg [Hoe krijg ik een tijdelijke licentie?](https://purchase.aspose.com/temporary-license) voor meer informatie.

{{% /alert %}} 

## **Over het Licentiebestand**
Nadat u tevreden bent met uw evaluatie van Aspose.PSD, kunt u een licentie aanschaffen op de [Aspose-website](https://purchase.aspose.com/default.aspx). Maak uzelf bekend met de verschillende aangeboden abonnementstypen. Als u vragen heeft, aarzel dan niet om contact op te nemen met [het verkoopteam van Aspose](https://company.aspose.com/contact).

Elke Aspose-licentie wordt geleverd met een jaarabonnement voor software-upgrades. Vernieuw uw abonnementen na het eerste jaar om de nieuwste functies en fixes te blijven ontvangen. Technische ondersteuning is gratis en onbeperkt en wordt geboden aan zowel gelicentieerde als evaluatiegebruikers via onze [Support-forums](https://forum.aspose.com/).

De licentie is een XML-bestand dat gegevens zoals de productnaam, het aantal gelicentieerde ontwikkelaars, de vervaldatum van het abonnement enzovoort bevat. Het bestand is digitaal ondertekend, wijzig het dus niet: zelfs het per ongeluk toevoegen van een extra regelafbreking maakt het bestand ongeldig.

Na het kopen van Aspose.PSD, moet u de licentie toepassen voordat u afbeeldingen maakt, bewerkt of anderszins manipuleert. Als u vergeet de licentie toe te passen, zullen alle uitvoerafbeeldingen een evaluatiewatermerk krijgen. 
U hoeft de licentie slechts één keer in te stellen per toepassing of proces dat u ontwikkelt.

## **Het Toepassen van de Licentie**
U kunt een evaluatieversie van **Aspose.PSD** voor Java downloaden van [zijn downloadpagina](http://maven.aspose.com/repository/simple/ext-release-local/com/aspose/aspose-psd/). De evaluatieversie biedt absoluut dezelfde mogelijkheden als de gelicentieerde versie van het product. Bovendien wordt de evaluatieversie eenvoudig gelicentieerd wanneer u een licentie aanschaft en een paar regels code toevoegt om de licentie toe te passen.

Als u tevreden bent met uw evaluatie van **Aspose.PSD**, kunt u een [licentie aanschaffen](http://www.aspose.com/Purchase/Components/Default.aspx) op de Aspose-website. Maak uzelf bekend met de verschillende aangeboden abonnementstypen. Als u vragen heeft, aarzel dan niet om contact op te nemen met het verkoopteam van Aspose.

Elke Aspose-licentie heeft een jaarabonnement voor gratis upgrades naar nieuwe versies of fixes die gedurende deze tijd worden uitgebracht. Technische ondersteuning is gratis en onbeperkt en wordt zowel aan gelicentieerde als evaluatiegebruikers geboden.

{{% alert color="primary" %}}

Als u **Aspose.PSD** wilt testen zonder de beperkingen van de evaluatieversie, vraag dan een tijdelijke licentie van 30 dagen aan. Raadpleeg [Hoe krijg ik een tijdelijke licentie?](http://www.aspose.com/corporate/how-to-get-temporary-license.aspx) voor meer informatie.

{{% /alert %}} 

### **Het Instellen van een Licentie**
De licentie is een platte tekst XML-bestand dat gegevens zoals de productnaam, het aantal ontwikkelaars waarvoor het is gelicentieerd, de vervaldatum van het abonnement enzovoort bevat. Het bestand is digitaal ondertekend, wijzig het bestand dus niet; zelfs het per ongeluk toevoegen van een extra regelafbreking zal het ongeldig maken.

U moet een licentie instellen voordat u **Aspose.PSD** gaat gebruiken als u de evaluatiebeperkingen wilt vermijden. U hoeft de licentie slechts één keer in te stellen per applicatie of proces.

De licentie kan worden geladen vanuit een stream of bestand op de volgende locaties:

1. Expliciet pad.
1. De map die de Aspose.PSD.jar bevat.

Gebruik de [License](http://www.aspose.com/api/java/psd/com.aspose.psd/classes/License).setLicense-methode om de component te licenseren. Vaak is de gemakkelijkste manier om een licentie in te stellen om het licentiebestand in dezelfde map als Aspose.PSD.jar te plaatsen en alleen de bestandsnaam zonder pad op te geven zoals getoond in het volgende voorbeeld:
#### **Voorbeeld 1**
In dit voorbeeld zal **Aspose.PSD** proberen het licentiebestand te vinden in de map die de JAR's van uw applicatie bevat.

**Java**

{{< highlight csharp >}}

 com.aspose.psd.License license = new com.aspose.psd.License();

license.setLicense("Aspose.PSD.Java.lic");

{{< /highlight >}}
#### **Voorbeeld 2**
Initialiseert een licentie vanuit een stream.

**Java**

{{< highlight csharp >}}

 com.aspose.psd.License license = new com.aspose.psd.License();

license.setLicense(new java.io.FileInputStream("Aspose.PSD.Java.lic"));

{{< /highlight >}}
### **Valideren van de Licentie**
Het is mogelijk om te controleren of de licentie correct is ingesteld of niet. De klasse License heeft het veld isLicensed dat true zal retourneren als de licentie correct is ingesteld.

**Java**

{{< highlight csharp >}}

 License license = new License();

license.setLicense("Aspose.PSD.Java.lic");

if (License.isLicensed()) {

    System.out.println("Licentie is ingesteld!");

}

{{< /highlight >}}
## **Waar een Licentie Toepassen in Uw Applicatie**
Waar u een licentie toepast, hangt af van het soort applicatie dat u ontwikkelt. Volg deze eenvoudige regels:

- De licentie hoeft slechts één keer per applicatiedomein te worden ingesteld. Het meerdere malen oproepen van License.setLicense is niet schadelijk maar verspilt processortijd.
- Pas de licentie toe voordat u enige klassen van Aspose.PSD aanroept.
- **Java-applicaties**: roep License.SetLicense aan in de opstartcode.
- **Klassebibliotheek**: roep License.setLicense aan vanuit een statische constructor van de klasse die Aspose.PSD gebruikt. De statische constructor voert uit voordat een instantie van uw klasse wordt gemaakt, waardoor de Aspose.PSD-licentie correct wordt ingesteld.

## **Het Gebruik van Meerdere Aspose-Producten**
Als u meer dan één Aspose-product in uw applicatie gebruikt, bijvoorbeeld Aspose.PSD en Aspose.Cells, volgen hier een paar nuttige tips.

- **Pas de licentie afzonderlijk toe voor elk Aspose-product**. Zelfs als u een enkel licentiebestand heeft voor alle componenten, bijvoorbeeld 'Aspose.Total.lic', moet u toch License.setLicense afzonderlijk aanroepen voor elk Aspose-product in uw applicatie.
- **Gebruik een volledig gekwalificeerde licentienaam**. Elk Aspose-product heeft een License-klasse in zijn namespace. Zo heeft Aspose.PSD com.aspose.psd.license.License en Aspose.Cells com.aspose.cells.License. Het gebruik van een volledig gekwalificeerde klassenaam voorkomt verwarring over welke licentie is toegepast op welk product.

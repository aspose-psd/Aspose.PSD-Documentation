---
title: Licenties
type: docs
weight: 70
url: /nl/net/licenties/
description: Evalueer PSD Photoshop C#-bibliotheek van NuGet en pas de licentie toe met behulp van een bestand of stream om eventuele beperkingen van de geïnstalleerde evaluatie te verwijderen.
---

## **Beperkingen van de Evaluatieversie**
U kunt een evaluatieversie van Aspose.PSD voor .NET downloaden vanaf [NuGet](https://www.nuget.org/packages/Aspose.psd/). De evaluatieversie biedt dezelfde functies als de volledig gelicenseerde versie van de component met een paar beperkingen. Wanneer u Aspose.PSD koopt, worden alle beperkingen van de geïnstalleerde evaluatie verwijderd door eenvoudigweg de licentie toe te passen. De evaluatieversie van Aspose.PSD voor .NET biedt volledige functionaliteit van het product, met slechts twee beperkingen:

- **Een watermerk op elk afbeelding**: Elke afbeelding die u opslaat, wijzigt of exporteert heeft een watermerk met de tekst "Alleen voor evaluatie. Gemaakt met Aspose.PSD. Copyright 2010-2018 Aspose Pty Ltd.". Kleine afbeeldingen, waar het volledige watermerk niet past, hebben in plaats daarvan twee diagonale lijnen over de afbeelding.
- **Geen ondersteuning voor kerntekeningfunctionaliteit**: In evaluatiemodus kunnen pixeIs van afbeeldingen niet worden geladen of opgeslagen in de afbeelding. Gebruik in plaats daarvan de geavanceerde tekenfunctionaliteit om afbeeldingen te tekenen. Deze beperking heeft invIoed op functionaliteiten die afhankelijk zijn van de kerntekeningfunctionaliteit. Aspose.PSD voor .NET staat toe dat u uw eigen bestandsindeling registreert. Deze functie is echter afhankelijk van de kerntekeningfunctionaliteit, dus het heeft geen zin om deze in evaluatiemodus te gebruiken omdat u de inhoud van die bestanden niet kunt wijzigen.

Als u Aspose.PSD voor .NET wilt testen zonder de evaluatiebeperkingen, vraag dan een tijdelijke licentie van 30 dagen aan. Raadpleeg [Hoe krijg ik een tijdelijke licentie?](https://purchase.aspose.com/temporary-license) voor meer informatie.
## **Over het Licentiebestand**
Nadat u tevreden bent met uw evaluatie van Aspose.PSD, kunt u een licentie aanschaffen op de [Aspose-website](https://purchase.aspose.com/default.aspx). Maak uzelf vertrouwd met de verschillende aangeboden abonnementstypen. Als u vragen heeft, aarzel dan niet om contact op te nemen met het [verkoopteam van Aspose](https://company.aspose.com/contact). Elke Aspose-licentie wordt geleverd met een abonnement van een jaar voor software-upgrades. Na het eerste jaar kunt u uw abonnementen verlengen om de nieuwste functies en oplossingen te blijven ontvangen. Technische ondersteuning is gratis en onbeperkt en wordt geboden aan zowel gelicentieerde als evaluatiegebruikers via onze [Ondersteuningsforums](https://forum.aspose.com/). Het licentiebestand is een XML-bestand dat gegevens bevat zoals de productnaam, het aantal gelicentieerde ontwikkelaars, de vervaldatum van het abonnement enzovoort. Het bestand is digitaal ondertekend, dus wijzig het niet: zelfs per ongeluk een extra regeIbreek toevoegen maakt het bestand ongeldig. Na de aanschaf van Aspose.PSD moet u de licentie toepassen voordat u afbeeldingen maakt, bewerkt of anderszins manipuleert. Als u vergeet om de licentie toe te passen, zullen alle uitvoerafbeeldingen een evaluatiewatermerk hebben. U hoeft de licentie slechts eenmalig in te stellen per toepassing of proces dat u ontwikkelt.
## **Waar de Licentie toe te passen in uw Applicatie**
Waar u een licentie toepast, hangt af van het type applicatie dat u ontwikkelt. Volg deze eenvoudige regels:

- Pas de licentie slechts eenmaal toe per toepassingsdomein. Het meerdere malen oproepen van License.SetLicense is niet schadelijk maar verspilt processortijd.
- Pas de licentie toe voordat u enige Aspose.PSD voor .NET-klassen oproept.
- **Windows Forms- of Console-applicaties**: roep License.SetLicense aan in de opstartcode, voordat u enige Aspose.PSD voor .NET-klassen gebruikt.
- **ASP.NET-applicaties**: roep License.SetLicense aan vanuit het bestand Global.asax.cs (Global.asax.vb), in de beschermde methode Application_Start. Op deze manier wordt het eenmaal aangeroepen wanneer de applicatie start. Roep License.SetLicense niet aan vanuit de Page_Load-methoden, anders wordt de licentie telkens geladen wanneer een webpagina wordt geladen.
- **Silverlight-applicaties**: roep License.SetLicense aan vanuit het Application_Startup-evenement in het App.xaml.cs (App.xaml.vb)-bestand.
- **Klassenbibliotheek**: roep License.SetLicense aan vanuit een statische constructor van de klasse die Aspose.PSD gebruikt. De statische constructor wordt uitgevoerd voordat een instantie van uw klasse wordt gemaakt, waardoor de Aspose.PSD-licentie correct wordt ingesteld.
## **Licentie toepassen**
U kunt eenvoudig een evaluatieversie van Aspose.PSD downloaden van NuGet [downloadpagina](https://www.nuget.org/packages/Aspose.psd/). De evaluatieversie biedt absoluut dezelfde mogelijkheden als de gelicenseerde versie van Aspose.PSD. Bovendien wordt de evaluatieversie eenvoudig gelicenseerd wanneer u een licentie aanschaft en een paar regels code toevoegt om de licentie toe te passen.
### **Gebruik van een Bestand of een Stream**
Als u wilt vermijden te werken met evaluatiebeperkingen, moet u een licentie instellen voordat u Aspose.PSD gebruikt. U hoeft slechts eenmaal per applicatie (of proces) een licentie in te stellen.
### **Licentie toepassen vanuit een bestand**
De eenvoudigste manier om een licentie toe te passen is door het licentiebestand in dezelfde map als Aspose.PSD.dll te plaatsen. Vervolgens kunt u de bestandsnaam opgeven in de code in plaats van het volledige pad.



{{< highlight java >}}

 // Maak een instantie van de licentie en pas de licentie toe met behulp van het volledige pad

Aspose.PSD.License licentie = nieuw Aspose.PSD.Licentie();

license.SetLicense("Aspose.PSD.lic");



{{< /highlight >}}



Wanneer u de SetLicense-methode aanroept, moet de naam van de licentie hetzelfde zijn als die van uw licentiebestandsnaam. Als u bijvoorbeeld de naam van het licentiebestand wijzigt naar "Aspose.PSD.lic.xml", moet u deze licentienaam voor de SetLicense-methode gebruiken.
### **Licentie toepassen met een stream**
Het is ook mogelijk om een licentie vanuit een stream te laden zoals hieronder gedemonstreerd.



{{< highlight java >}}



// Maak een instantie van de licentie en pas de licentie toe met behulp van een stream

Aspose.PSD.License licentie = nieuw Aspose.PSD.Licentie();

licentie.SetLicense(mijnStream);



{{< /highlight >}}
### **Controleren van de licentiestatus**
De Aspose.PSD.License-klasse heeft de eigenschap IsGelicentieerd die true zal teruggeven als de licentie correct is ingesteld.



{{< highlight java >}}

 Licentie licentie = nieuw Licentie();

license.SetLicense(licentiePad);

if (license.IsGelicentieerd)

{

    Console.WriteLine("Licentie is ingesteld!");

}

{{< /highlight >}}
### **Gebruik van een Ingesloten Hulpbron**
Een praktische manier om de licentie samen met uw applicatie te verpakken en ervoor te zorgen dat deze niet verloren gaat, is om deze op te nemen als een ingesloten hulpbron in een van de assemblies die Aspose.PSD aanroept. Om het licentiebestand op te nemen als een ingesloten hulpbron:

1. In Visual Studio .NET, klik op het **Bestand**-menu en selecteer **Bestaand Item Toevoegen**.
1. Neem het licentiebestand (extensie .lic) op in het project.
1. Selecteer het bestand in de Solution Explorer.
1. Stel in het Eigenschappenvenster **Bouwactie** in op **Ingesloten Hulpbron**.

Het is niet nodig om de methoden GetExecutingAssembly of GetManifestResourceStream van de System.Reflection.Assembly aan te roepen in het Microsoft .NET Framework om toegang te krijgen tot een ingesloten licentie. Integendeel, neem het bestand op als een hulpbron in het project en geef vervolgens de naam van het licentiebestand door aan de SetLicense-methode. De Licentieklasse vindt automatisch het licentiebestand in de ingesloten hulpbronnen. Het onderstaande voorbeeld toont hoe u de licentie als een ingesloten hulpbron kunt opnemen en deze kunt toepassen op uw applicatie.



{{< highlight java >}}

 // Maak een instantie van de Licentieklasse

Aspose.PSD.License licentie = nieuw Aspose.PSD.Licentie();



// Geef de naam van het ingesloten licentiebestand door

licentie.SetLicense("Aspose.PSD.lic");

{{< /highlight >}}


### **Controleren van de licentiestatus**
De Aspose.PSD.License-klasse heeft de eigenschap IsGelicentieerd die true zal teruggeven als de licentie correct is ingesteld.



{{< highlight java >}}

 Licentie licentie = nieuw Licentie();

license.SetLicense(licentiePad);

if (license.IsGelicentieerd)

{

    Console.WriteLine("Licentie is ingesteld!");

}

{{< /highlight >}}

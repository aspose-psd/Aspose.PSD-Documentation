---
title: Hoe de Voorbeelden Uit te Voeren
type: docs
weight: 90
url: /nl/net/how-to-run-the-examples/
description: Leer hoe je de voorbeelden met betrekking tot de bibliotheek voor het PSD-bestandsformaat kunt uitvoeren, die gehost worden op GitHub.
---

## **Software Vereisten**
Zorg ervoor dat je voldoet aan de volgende vereisten voordat je de voorbeelden downloadt en uitvoert.

1. Visual Studio 2010 of hoger
1. NuGet Package Manager geïnstalleerd in Visual Studio. Zorg ervoor dat de nieuwste NuGet API-versie is geïnstalleerd in Visual Studio. Voor details over het installeren van de NuGet-pakketbeheerder, bekijk [http://docs.nuget.org/ndocs/guides/install-nuget](http://docs.nuget.org/ndocs/guides/install-nuget)
1. Ga naar Tools->Options->NuGet Package Manager->Package Sources en zorg ervoor dat de optie **nuget.org** is aangevinkt
1. Het voorbeeldproject maakt gebruik van de automatische NuGet-pakket herstelfunctie, daarom moet je een actieve internetverbinding hebben. Als je geen actieve internetverbinding hebt op de machine waar de voorbeelden worden uitgevoerd, bekijk dan [Installatie](/psd/nl/net/installation/) om een referentie naar Aspose.Imaging.dll toe te voegen in het voorbeeldproject.
  
## **Downloaden van GitHub**
Alle voorbeelden van Aspose.PSD voor .NET worden gehost op [GitHub](https://github.com/aspose-psd/Aspose.PSD-for-.NET).

- Je kunt ofwel het repository klonen met behulp van je favoriete GitHub-client of het ZIP-bestand downloaden van [hier](https://github.com/aspose-psd/Aspose.PSD-for-.NET/archive/master.zip).
- Pak de inhoud van het ZIP-bestand uit naar een willekeurige map op je computer. Alle voorbeelden bevinden zich in de map **Examples**.
- Er is een Visual Studio-oplossingsbestand voor C#.
- De projecten zijn gemaakt in Visual Studio 2013, maar de oplossingsbestanden zijn compatibel met Visual Studio 2010 SP1 en hoger.
- Open het oplossingsbestand in Visual Studio en bouw het project.
- Bij de eerste uitvoering worden de afhankelijkheden automatisch gedownload via NuGet.
- De **Data**-map in de hoofdmap van **Examples** bevat invoerbestanden die door de CSharp-voorbeelden worden gebruikt. Het is verplicht om de **Data**-map samen met het voorbeeldproject te downloaden.
- Open het bestand RunExamples.cs, alle voorbeelden worden hier vanuit opgeroepen.
- Maak opmerkingen van de voorbeelden die je wilt uitvoeren binnen het project.

Aarzel niet om contact met ons op te nemen via onze Forums als je problemen ondervindt bij het opzetten of uitvoeren van de voorbeelden.

## **Bijdragen**
Als je een voorbeeld wilt toevoegen of verbeteren, moedigen we je aan om bij te dragen aan het project. Alle voorbeelden en showcase-projecten in dit repository zijn open source en kunnen vrij worden gebruikt in je eigen applicaties.

Om bij te dragen, kun je het repository forkken, de broncode bewerken en een pull-aanvraag maken. We zullen de wijzigingen bekijken en deze opnemen in het repository indien nuttig.

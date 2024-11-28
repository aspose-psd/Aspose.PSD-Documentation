---
title: Hoe Aspose.PSD in Docker uit te voeren
type: docs
description: "Voer Aspose.PSD uit in een Docker-container voor Linux, Windows Server en elk ander besturingssysteem. "
weight: 90
url: /nl/hoe-aspose-psd-in-docker-te-runnen/
---

## Benodigdheden

- Docker moet geïnstalleerd zijn op uw systeem. Voor informatie over hoe Docker te installeren op Windows of Mac, zie de links in de "Zie Ook" sectie.

- Visual Studio 2022.

- NET 6 SDK wordt gebruikt in het voorbeeld.

- U kunt een volledig werkend voorbeeldproject downloaden op https://github.com/aspose-psd/Aspose.PSD-Docker-Sample


## Hello World Applicatie

In dit voorbeeld maakt u een eenvoudige Hello World-consoletoepassing die een psd-bestand opent, een tekstlaag bijwerkt en tekent met behulp van de Graphics API. De beschreven toepassing kan worden gebouwd en uitgevoerd in Docker.

### Het maken van de Consoletoepassing

Volg de onderstaande stappen om het Hello World-programma te maken:
1. Zorg ervoor dat Docker is geïnstalleerd en gebruikmaakt van Linux-containers (standaard). Selecteer indien nodig de optie Overschakelen naar Linux-containers in het Docker Desktop-menu.
1. Maak in Visual Studio een NET 6-consoletoepassing.<br>
![Een dialoogvenster voor het maken van een NET 6 consoletoepassing](create-a-new-project.png)<br>
1. Installeer de nieuwste versie van Aspose.PSD van NuGet.<br>
![Aspose.PSD op NuGet](nuget-aspose-psd.png)<br>
1. Aangezien de toepassing zal worden uitgevoerd op Linux, moet u mogelijk extra lettertypen installeren. U kunt bijvoorbeeld kiezen voor ttf-mscorefonts-installer.
1. Let op, om tekstrendereigenschappen op Linux te gebruiken, moet je de volgende pakketten toevoegen: apt-transport-https, libgdiplus, libc6-dev. De commando's om ze toe te voegen, staan in het Dockerfile.
1. Wanneer alle benodigde afhankelijkheden zijn toegevoegd, schrijf dan een eenvoudig programma dat het PSD-bestand opent, de tekstlaag bijwerkt en vervolgens iets tekent met behulp van graphics:<br>

{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "Documentation-CSharp-Aspose-Docker-Example-1.cs " >}}

Let op dat voor het bewerken van tekstlagen een licentie nodig is. U kunt een tijdelijke licentie krijgen met behulp van het volgende artikel: https://purchase.aspose.com/temporary-license
 
### Configuratie van een Dockerfile

Het volgende te doen is het maken en configureren van de Dockerfile.

1. Maak de Dockerfile en plaats deze naast het oplossingsbestand van uw toepassing. Houd deze bestandsnaam zonder extensie (de standaardnaam).
1. Specificeer in de Dockerfile:

{{< highlight plain >}}
#Zie https://aka.ms/containerfastmode om te begrijpen hoe Visual Studio deze Dockerfile gebruikt om uw afbeeldingen te bouwen voor sneller debuggen.

FROM mcr.microsoft.com/dotnet/runtime:6.0 AS base
WORKDIR /app

#Voor het gebruik van de mogelijkheid om tekstlagen bij te werken, moet u de volgende pakketten aan uw container toevoegen
RUN apt-get update
RUN yes | apt-get install -y apt-transport-https
RUN yes | apt-get install -y libgdiplus
RUN yes | apt-get install -y libc6-dev

FROM mcr.microsoft.com/dotnet/sdk:6.0 AS build

WORKDIR /src
COPY ["AsposePsdDockerSample/AsposePsdDockerSample.csproj", "AsposePsdDockerSample/"]
RUN dotnet restore "AsposePsdDockerSample/AsposePsdDockerSample.csproj"
COPY . .
WORKDIR "/src/AsposePsdDockerSample"
RUN dotnet build "AsposePsdDockerSample.csproj" -c Release -o /app/build

FROM build AS publish
RUN dotnet publish "AsposePsdDockerSample.csproj" -c Release -o /app/publish

FROM base AS final
WORKDIR /app
COPY --from=publish /app/publish .
ENTRYPOINT ["dotnet", "AsposePsdDockerSample.dll"]
{{< /highlight >}}

Bovenstaand is een eenvoudige Dockerfile, die de volgende instructies bevat:

- Het te gebruiken SDK-beeld. Hier is het Microsoft .Net 6-beeld. Docker zal het downloaden wanneer de build wordt uitgevoerd. De versie van SDK is gespecificeerd als tag.
- Voeg vervolgens de afhankelijkheden toe om de tekst te renderen.
- Mogelijk moet u ook lettertypen installeren, omdat het SDK-beeld zeer weinig lettertypen bevat. Ook kunt u lokale lettertypen gebruiken die zijn gekopieerd naar het Docker-beeld.
- De werkmap, die wordt gespecificeerd in de volgende regel.
- Het commando om alles naar de container te kopiëren, de toepassing te publiceren en het startpunt te specificeren.

### Het Bouwen en Uitvoeren van de Toepassing in Docker

#### Gebruik van Visual Studio
De eenvoudigste manier om Aspose.PSD in Docker te proberen, is door Visual Studio te openen en de app te starten met Docker-ondersteuning
![Voer de voorbeeldapplicatie van Aspose.PSD uit in docker met behulp van Visual Studio](psd/nl-vs-run-using-docker-support.png)

#### Gebruik van Opdrachtprompt
De toepassing kan worden gebouwd en uitgevoerd in Docker via de opdrachtprompt. Open uw favoriete opdrachtprompt, wijzig naar de map met de toepassing (map waar het oplossingsbestand en het Dockerfile zijn geplaatst) en voer het volgende commando uit:

{{< highlight plain >}}
docker build -t asposepsddocker .
{{< /highlight >}}

De eerste keer dat dit commando wordt uitgevoerd, kan het langer duren omdat Docker de vereiste afbeeldingen moet downloaden. Zodra het vorige commando is voltooid, voer het volgende commando uit:

{{< highlight plain >}}
docker run --name asposepsdcontainer asposepsddocker; docker cp asposepsddocker:/app/Output.psd .; docker cp asposepsddocker:/app/Output.png .; docker rm asposepsdcontainer
{{< /highlight >}}

{{% alert color="primary" %}} 

Let op het mountargument, omdat, zoals eerder vermeld, een map op de hostmachine wordt gemonteerd in de map van de container om de resultaten van de toepassingsuitvoering gemakkelijk te kunnen zien. Padnamen in Linux zijn hoofdlettergevoelig.

{{% /alert %}}


## Meer Voorbeelden

Voor meer voorbeelden van hoe u Aspose.PSD in Docker kunt gebruiken, zie de [voorbeelden](https://github.com/aspose-psd/Aspose.PSD-for-.NET).


## Zie Ook

- [Docker-desktop installeren op Windows](https://docs.docker.com/docker-for-windows/install/)
- [Docker-desktop installeren op Mac](https://docs.docker.com/docker-for-mac/install/)
- [Visual Studio 2022, NET 6 SDK](https://docs.microsoft.com/en-us/dotnet/core/install/windows?tabs=net60#dependencies)
- Optie om over te schakelen naar Linux-containers
- Extra informatie over [.NET Core SDK](https://hub.docker.com/_/microsoft-dotnet-sdk)

---
title: Come Eseguire Aspose.PSD in Docker
type: docs
description: "Esegui Aspose.PSD in un contenitore Docker per Linux, Windows Server e qualsiasi altro sistema operativo."
weight: 90
url: /it/net/come-eseguire-aspose-psd-in-docker/
---

## Prerequisiti

- Docker deve essere installato sul tuo sistema. Per informazioni su come installare Docker su Windows o Mac, consulta i link nella sezione "Vedi Anche".

- Visual Studio 2022.

- SDK .NET 6 è utilizzato nell'esempio.

- Puoi scaricare un progetto di esempio completamente funzionante su https://github.com/aspose-psd/Aspose.PSD-Docker-Sample


## Applicazione Hello World

In questo esempio, creerai una semplice applicazione console Hello World che apre un file psd, aggiorna il layer di testo e disegna usando l'API di grafica. L'applicazione descritta può essere compilata ed eseguita in Docker.

### Creazione dell'Applicazione Console

Per creare il programma Hello World, segui i passaggi seguenti:
1. Una volta installato Docker, assicurati che utilizzi Containers Linux (predefinito). Se necessario, seleziona l'opzione Switch to Linux containers dal menu di Docker Desktop.
1. In Visual Studio, crea un'applicazione console .NET 6.<br>
![Dialogo del progetto dell'applicazione console .NET 6](create-a-new-project.png)<br>
1. Installa l'ultima versione di Aspose.PSD da NuGet.<br>
![Aspose.PSD su NuGet](nuget-aspose-psd.png)<br>
1. Poiché l'applicazione verrà eseguita su Linux, potrebbe essere necessario installare caratteri aggiuntivi. Si consiglia di utilizzare ttf-mscorefonts-installer.
1. Si prega di notare, per utilizzare le funzionalità di rendering del testo su Linux è necessario aggiungere i seguenti pacchetti: apt-transport-https, libgdiplus, libc6-dev. I comandi per aggiungerli possono essere trovati nel file Dockerfile.
1. Una volta aggiunte tutte le dipendenze necessarie, scrivi un programma semplice che apre il file PSD, aggiorna il layer di testo e disegna qualcosa utilizzando la grafica:<br>

{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "Documentation-CSharp-Aspose-Docker-Example-1.cs" >}}

Si nota che per modificare i layer di testo è necessario ottenere la licenza. Puoi ottenere una licenza temporanea, utilizzando l'articolo seguente: https://purchase.aspose.com/temporary-license

### Configurazione di un Dockerfile

Il passo successivo è creare e configurare il Dockerfile.

1. Crea il Dockerfile e posizionalo accanto al file di soluzione della tua applicazione. Mantieni il nome di questo file senza estensione (predefinito).
1. Nel Dockerfile, specifica:

{{< highlight plain >}}
#Vedi https://aka.ms/containerfastmode per capire come Visual Studio utilizza questo Dockerfile per creare le tue immagini per un debug più veloce.

FROM mcr.microsoft.com/dotnet/runtime:6.0 AS base
WORKDIR /app

# Per utilizzare la possibilità di aggiornare i layer di testo è necessario aggiungere i seguenti pacchetti al tuo contenitore
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

Il precedente è un semplice Dockerfile che contiene le seguenti istruzioni:

- L'immagine SDK da utilizzare. Qui è utilizzata l'immagine Microsoft .Net 6. Docker la scaricherà durante l'esecuzione della build. La versione dello SDK è specificata come tag.
- Successivamente aggiungi le dipendenze per il rendering del testo.
- Successivamente, potresti dover installare i caratteri poiché l'immagine SDK contiene pochi caratteri. Inoltre, puoi utilizzare caratteri locali copiati nell'immagine Docker.
- La directory di lavoro, specificata nella riga successiva.
- Il comando per copiare tutto nel contenitore, pubblicare l'applicazione e specificare il punto di ingresso.

### Compilazione ed Esecuzione dell'Applicazione in Docker

#### Utilizzando Visual Studio
Il modo più semplice per provare Aspose.PSD in Docker è aprire Visual Studio e avviare l'app utilizzando il supporto di Docker
![Esegui l'app di esempio Aspose.PSD in Docker utilizzando Visual Studio](psd-vs-run-using-docker-support.png)

#### Utilizzando il Prompt dei Comandi
L'applicazione può essere compilata ed eseguita in Docker utilizzando il prompt dei comandi. Apri il tuo prompt dei comandi preferito, cambia la directory alla cartella dell'applicazione (cartella in cui sono posizionati il file di soluzione e il Dockerfile) ed esegui il seguente comando:

{{< highlight plain >}}
docker build -t asposepsddocker .
{{< /highlight >}}

La prima volta che viene eseguito questo comando potrebbe richiedere più tempo, poiché Docker deve scaricare le immagini richieste. Una volta completato il comando precedente, esegui il seguente comando:

{{< highlight plain >}}
docker run --name asposepsdcontainer asposepsddocker; docker cp asposepsddocker:/app/Output.psd .; docker cp asposepsddocker:/app/Output.png .; docker rm asposepsdcontainer
{{< /highlight >}}

{{% alert color="primary" %}}

Fai attenzione all'argomento mount, perché, come già menzionato, una cartella sulla macchina host è montata nella cartella del contenitore, per visualizzare facilmente i risultati dell'esecuzione dell'applicazione. I percorsi in Linux fanno distinzione tra maiuscole e minuscole.

{{% /alert %}}


## Altri Esempi

Per ulteriori esempi su come puoi utilizzare Aspose.PSD in Docker, consulta gli [esempi](https://github.com/aspose-psd/Aspose.PSD-for-.NET).


## Vedi Anche

- [Installare Docker Desktop su Windows](https://docs.docker.com/docker-for-windows/install/)
- [Installare Docker Desktop su Mac](https://docs.docker.com/docker-for-mac/install/)
- [Visual Studio 2022, SDK .NET 6](https://docs.microsoft.com/en-us/dotnet/core/install/windows?tabs=net60#dependencies)
- Opzione per [passare ai container Linux](https://docs.docker.com/docker-for-windows/#switch-between-windows-and-linux-containers)
- Ulteriori informazioni su [.NET Core SDK](https://hub.docker.com/_/microsoft-dotnet-sdk)

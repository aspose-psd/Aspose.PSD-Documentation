---
title: So führen Sie Aspose.PSD in Docker aus
type: docs
description: "Führen Sie Aspose.PSD in einem Docker-Container für Linux, Windows Server und jedes Betriebssystem aus."
weight: 90
url: /de/net/how-to-run-aspose-psd-in-docker/
---

## Voraussetzungen

- Docker muss auf Ihrem System installiert sein. Informationen zur Installation von Docker unter Windows oder Mac finden Sie in den Links im Abschnitt "Siehe auch".

- Visual Studio 2022.

- NET 6 SDK wird im Beispiel verwendet.

- Sie können ein vollständig funktionierendes Beispielprojekt auf https://github.com/aspose-psd/Aspose.PSD-Docker-Sample herunterladen.


## Beispielanwendung Hallo Welt

In diesem Beispiel erstellen Sie eine einfache Hallo-Welt-Konsolenanwendung, die eine psd-Datei öffnet, einen Textlayer aktualisiert und mithilfe der Graphics API zeichnet. Die beschriebene Anwendung kann in Docker erstellt und ausgeführt werden.

### Erstellen der Konsolenanwendung

Folgen Sie den nachstehenden Schritten, um das Hallo-Welt-Programm zu erstellen:
1. Stellen Sie sicher, dass Docker Linux-Container (Standard) verwendet, nachdem Docker installiert wurde. Wählen Sie gegebenenfalls die Option "Zu Linux-Containern wechseln" im Docker-Desktopmenü aus.
1. Erstellen Sie in Visual Studio eine NET 6 Konsolenanwendung.<br>
![Dialogfeld für ein NET 6 Konsolenanwendungsprojekt](create-a-new-project.png)<br>
1. Installieren Sie die neueste Version von Aspose.PSD über NuGet.<br>
![Aspose.PSD auf NuGet](nuget-aspose-psd.png)<br>
1. Da die Anwendung auf Linux ausgeführt wird, sollten zusätzliche Schriftarten installiert werden. Sie könnten ttf-mscorefonts-installer verwenden.
1. Beachten Sie, dass Sie zum Verwenden der Textrendereigenschaften auf Linux die folgenden Pakete hinzufügen müssen: apt-transport-https, libgdiplus, libc6-dev. Die Befehle zum Hinzufügen finden Sie in der Datei "Dockerfile".
1. Wenn alle erforderlichen Abhängigkeiten hinzugefügt sind, schreiben Sie ein einfaches Programm, das die PSD-Datei öffnet, den Textlayer aktualisiert und dann etwas mit der Grafik zeichnet:<br>

{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "Documentation-CSharp-Aspose-Docker-Example-1.cs " >}}

Beachten Sie, dass Sie eine Lizenz benötigen, um Textlayer zu bearbeiten. Sie können eine temporäre Lizenz erhalten, indem Sie den folgenden Artikel verwenden: https://purchase.aspose.com/temporary-license
 
### Konfigurieren eines Dockerfile

Der nächste Schritt besteht darin, ein Dockerfile zu erstellen und zu konfigurieren.

1. Erstellen Sie das Dockerfile und platzieren Sie es neben der Lösungsdatei Ihrer Anwendung. Behalten Sie diesen Dateinamen ohne Erweiterung bei (Standard).
1. Geben Sie im Dockerfile an:

{{< highlight plain >}}
#Siehe https://aka.ms/containerfastmode, um zu verstehen, wie Visual Studio dieses Dockerfile verwendet, um Ihre Images für schnellere Debugging zu erstellen.

FROM mcr.microsoft.com/dotnet/runtime:6.0 AS base
WORKDIR /app

# Um die Fähigkeit zum Aktualisieren der Textlayer zu verwenden, fügen Sie Ihrem Container die folgenden Pakete hinzu
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

Das obige Dockerfile ist ein einfaches Dockerfile, das die folgenden Anweisungen enthält:

- Das SDK-Image, das verwendet werden soll. Hier handelt es sich um das Microsoft .Net 6-Image. Docker lädt es beim Ausführen des Builds herunter. Die Version des SDK wird als Tag angegeben.
- Fügen Sie dann die Abhängigkeiten zum Rendern des Texts hinzu.
- Danach müssen möglicherweise Schriftarten installiert werden, da das SDK-Image nur sehr wenige Schriftarten enthält. Außerdem können Sie lokale Schriftarten kopieren, die im Docker-Image verwendet werden können.
- Das Arbeitsverzeichnis, das in der nächsten Zeile angegeben ist.
- Der Befehl zum Kopieren aller Dateien in den Container, zum Publizieren der Anwendung und zum Festlegen des Einstiegspunkts.

### Erstellen und Ausführen der Anwendung in Docker

#### Verwenden von Visual Studio
Der einfachste Weg, Aspose.PSD in Docker auszuprobieren, besteht darin, Visual Studio zu öffnen und die App mit Docker-Unterstützung zu starten.
![Führen Sie die Aspose.PSD-Beispiel-App in Docker mithilfe von Visual Studio aus](psd-vs-run-using-docker-support.png)

#### Verwenden der Eingabeaufforderung
Die Anwendung kann in Docker mithilfe der Eingabeaufforderung erstellt und ausgeführt werden. Öffnen Sie Ihre bevorzugte Eingabeaufforderung, wechseln Sie zum Ordner mit der Anwendung (dem Ordner, in dem die Lösungsdatei und das Dockerfile platziert sind), und führen Sie den folgenden Befehl aus:

{{< highlight plain >}}
docker build -t asposepsddocker .
{{< /highlight >}}

Bei der ersten Ausführung dieses Befehls kann es etwas länger dauern, da Docker die erforderlichen Images herunterladen muss. Wenn der vorherige Befehl abgeschlossen ist, führen Sie den folgenden Befehl aus:

{{< highlight plain >}}
docker run --name asposepsdcontainer asposepsddocker; docker cp asposepsddocker:/app/Output.psd .; docker cp asposepsddocker:/app/Output.png .; docker rm asposepsdcontainer
{{< /highlight >}}

{{% alert color="primary" %}} 

Beachten Sie das Mount-Argument, denn wie bereits erwähnt, wird ein Ordner auf der Hostmaschine in den Ordner des Containers eingehängt, um die Ergebnisse der Anwendungsausführung leicht zu sehen. Pfade in Linux sind Groß-/Kleinschreibung beachten.

{{% /alert %}}


## Weitere Beispiele

Für weitere Beispiele, wie Sie Aspose.PSD in Docker verwenden können, sehen Sie die [Beispiele](https://github.com/aspose-psd/Aspose.PSD-for-.NET).


## Siehe auch

- [Docker Desktop unter Windows installieren](https://docs.docker.com/docker-for-windows/install/)
- [Docker Desktop unter Mac installieren](https://docs.docker.com/docker-for-mac/install/)
- [Visual Studio 2022, NET 6 SDK](https://docs.microsoft.com/de-de/dotnet/core/install/windows?tabs=net60#dependencies)
- Option "Zu Linux-Containern wechseln" (https://docs.docker.com/docker-for-windows/#switch-between-windows-and-linux-containers)
- Weitere Informationen zum [.NET Core SDK](https://hub.docker.com/_/microsoft-dotnet-sdk)

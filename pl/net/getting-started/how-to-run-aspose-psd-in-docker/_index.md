---
title: Jak uruchomić Aspose.PSD w Dockerze
type: docs
description: "Uruchamianie Aspose.PSD w kontenerze Docker dla systemu Linux, Windows Server i każdego innego systemu operacyjnego."
weight: 90
url: /pl/net/jak-uruchomic-aspose-psd-w-dockerze/
---

## Wymagania

- Docker musi być zainstalowany na Twoim systemie. Aby uzyskać informacje na temat instalacji Dockera na systemach Windows lub Mac, zapoznaj się z linkami w sekcji „Zobacz także”.

- Visual Studio 2022.

- SDK NET 6 jest używany w przykładzie.

- Możesz pobrać w pełni działający przykładowy projekt na https://github.com/aspose-psd/Aspose.PSD-Docker-Sample


## Aplikacja Hello World

W tym przykładzie tworzysz prostą aplikację konsolową Hello World, która otwiera plik psd, aktualizuje warstwę tekstową i rysuje przy użyciu interfejsu API Graphics. Opisana aplikacja może być kompilowana i uruchamiana w Dockerze.

### Tworzenie Aplikacji Konsolowej

Aby utworzyć program Hello World, postępuj zgodnie z poniższymi krokami:
1. Gdy Docker jest zainstalowany, upewnij się, że korzysta z kontenerów Linux (domyślnie). Jeśli to konieczne, wybierz opcję Przełącz na kontenery Linux z menu Dockera Desktop.
1. W programie Visual Studio utwórz aplikację konsolową NET 6.<br>
![Okno dialogowe projektu aplikacji konsolowej NET 6](create-a-new-project.png)<br>
1. Zainstaluj najnowszą wersję Aspose.PSD z NuGet.<br>
![Aspose.PSD na NuGet](nuget-aspose-psd.png)<br>
1. Ponieważ aplikacja będzie uruchamiana w systemie Linux, możesz potrzebować zainstalować dodatkowe czcionki. Możesz preferować ttf-mscorefonts-installer.
1. Zauważ, że aby korzystać z funkcji renderowania tekstu w systemie Linux, musisz dodać następujące pakiety: apt-transport-https, libgdiplus, libc6-dev. Komendy do ich dodania można znaleźć w pliku Dockerfile.
1. Gdy wszystkie wymagane zależności są dodane, napisz prosty program, który otwiera plik PSD, aktualizuje warstwę tekstu, a następnie rysuje coś za pomocą grafiki:<br>

{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "Documentation-CSharp-Aspose-Docker-Example-1.cs " >}}

Zwróć uwagę, że do edycji warstw tekstowych musisz uzyskać licencję. Możesz uzyskać tymczasową licencję, korzystając z artykułu: https://purchase.aspose.com/temporary-license
 
### Konfigurowanie pliku Dockerfile

Następnym krokiem jest utworzenie i skonfigurowanie pliku Dockerfile.

1. Utwórz plik Dockerfile i umieść go obok pliku rozwiązania Twojej aplikacji. Zachowaj nazwę tego pliku bez rozszerzenia (domyślne).
1. W pliku Dockerfile określ:

{{< highlight plain >}}
#Zobacz https://aka.ms/containerfastmode, aby zrozumieć, jak Visual Studio używa tego pliku Dockerfile do budowania obrazów dla szybszego debugowania.

FROM mcr.microsoft.com/dotnet/runtime:6.0 AS base
WORKDIR /app

# Aby korzystać z możliwości aktualizacji warstw tekstowych, musisz dodać następujące pakiety do kontenera
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

Powyższy Dockerfile jest prostym plikiem, który zawiera następujące instrukcje:

- Obraz SDK do użycia. Tutaj jest to obraz Microsoftu .Net 6. Docker go pobierze podczas uruchamiania procesu kompilacji. Wersja SDK jest określona jako etykieta.
- Następnie dodajesz zależności do renderowania tekstu.
- Następnie możesz potrzebować zainstalować czcionki, ponieważ obraz SDK zawiera bardzo niewiele czcionek. Możesz także użyć lokalnych czcionek skopiowanych do obrazu Dockera.
- Katalog roboczy jest określony w następnej linii.
- Polecenie kopii wszystkiego do kontenera, opublikowania aplikacji i określenie punktu wejścia.

### Kompilowanie i Uruchamianie Aplikacji w Dockerze

#### Korzystanie z Visual Studio
Najprostszym sposobem wypróbowania Aspose.PSD w Dockerze jest otwarcie aplikacji w programie Visual Studio i uruchomienie jej z użyciem obsługi Dockera
![Uruchomienie przykładowej aplikacji Aspose.PSD w dockerze za pomocą Visual Studio](psd-vs-run-using-docker-support.png)

#### Korzystanie z Wiersza Poleceń
Aplikację można skompilować i uruchomić w Dockerze, korzystając z wiersza poleceń. Otwórz ulubiony wiersz poleceń, przejdź do folderu z aplikacją (folder, w którym znajdują się plik rozwiązania i plik Dockerfile) i uruchom następujące polecenie:

{{< highlight plain >}}
docker build -t asposepsddocker .
{{< /highlight >}}

Pierwsze wykonanie tego polecenia może zająć trochę czasu, ponieważ Docker musi pobrać wymagane obrazy. Po zakończeniu poprzedniego polecenia uruchom następujące polecenie:

{{< highlight plain >}}
docker run --name asposepsdcontainer asposepsddocker; docker cp asposepsddocker:/app/Output.psd .; docker cp asposepsddocker:/app/Output.png .; docker rm asposepsdcontainer
{{< /highlight >}}

{{% alert color="primary" %}} 

Zwróć uwagę na argument montowania, ponieważ, jak wspomniano wcześniej, folder na maszynie hosta jest montowany do folderu kontenera, aby łatwo zobaczyć wyniki wykonania aplikacji. Ścieżki w systemie Linux są rozróżniane pod względem wielkości liter.

{{% /alert %}}


## Więcej Przykładów

Aby uzyskać więcej przykładów, jak możesz korzystać z Aspose.PSD w Dockerze, zobacz [przykłady](https://github.com/aspose-psd/Aspose.PSD-for-.NET).


## Zobacz także

- [Instalacja Docker Desktop na Windows](https://docs.docker.com/docker-for-windows/install/)
- [Instalacja Docker Desktop na Macu](https://docs.docker.com/docker-for-mac/install/)
- [Visual Studio 2022, SDK NET 6](https://docs.microsoft.com/en-us/dotnet/core/install/windows?tabs=net60#dependencies)
- Opcja [Przełącz na kontenery Linux](https://docs.docker.com/docker-for-windows/#switch-between-windows-and-linux-containers)
- Dodatkowe informacje na temat [.NET Core SDK](https://hub.docker.com/_/microsoft-dotnet-sdk)

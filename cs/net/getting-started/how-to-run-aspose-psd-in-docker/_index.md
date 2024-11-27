---
title: Jak spustit Aspose.PSD v Dockeru
type: docs
description: "Spusťte Aspose.PSD v kontejneru Docker pro Linux, Windows Server a jakýkoli jiný OS."
weight: 90
url: /cs/jak-spustit-aspose-psd-v-dockeru/
---

## Předpoklady

- Docker musí být nainstalován na vašem systému. Pokud chcete informace o instalaci Dockeru na Windows nebo Mac, přejděte na odkazy v sekci „Viz také“.

- Visual Studio 2022.

- NET 6 SDK je použit v příkladu.

- Můžete stáhnout úplně funkční ukázkový projekt na https://github.com/aspose-psd/Aspose.PSD-Docker-Sample


## Aplikace Hello World

V tomto příkladu vytvoříte jednoduchou konzolovou aplikaci Hello World, která otevírá soubor psd, aktualizuje textovou vrstvu a kreslí pomocí API Graphics. Popisovaná aplikace může být sestavena a spuštěna v Dockeru.

### Vytvoření konzolové aplikace

Pro vytvoření programu Hello World postupujte podle následujících kroků:
1. Jakmile je nainstalován Docker, ujistěte se, že používá kontejnery Linux (výchozí). Pokud je to nutné, vyberte možnost Přepnout na Linuxové kontejnery z nabídky Docker Desktop.
1. V programu Visual Studio vytvořte konzolovou aplikaci NET 6.<br>
![Dialog nového projektu konzolové aplikace NET 6](create-a-new-project.png)<br>
1. Nainstalujte nejnovější verzi Aspose.PSD z NuGet.<br>
![Aspose.PSD na NuGetu](nuget-aspose-psd.png)<br>
1. Jelikož bude aplikace spuštěna na Linuxu, mohou být nutné instalovat další písma. Můžete upřednostnit ttf-mscorefonts-installer.
1. Všimněte si, že k použití funkcí vykreslování textu na Linuxu musíte přidat následující balíčky: apt-transport-https, libgdiplus, libc6-dev. Příslušné příkazy k jejich přidání lze nalézt v dockerfile.
1. Jakmile jsou přidány všechny požadované závislosti, napište jednoduchý program, který otevře soubor PSD, aktualizuje textovou vrstvu a pak něco nakreslí pomocí grafiky:<br>

{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "Dokumentace-CSharp-Aspose-Docker-Example-1.cs " >}}

Upozorňujeme, že pro úpravu textových vrstev je třeba získat licenci. Dočasnou licenci můžete získat pomocí následujícího článku: https://purchase.aspose.com/temporary-license
 
### Konfigurace Dockerfile

Dalším krokem je vytvoření a konfigurace souboru Dockerfile.

1. Vytvořte soubor Dockerfile a umístěte jej vedle souboru s řešením vaší aplikace. Zachovejte toto jméno souboru bez přípony (výchozí).
1. V souboru Dockerfile specifikujte:

{{< highlight plain >}}
#Viz https://aka.ms/containerfastmode pro pochopení toho, jak Visual Studio používá tento Dockerfile k sestavení vašich obrazů pro rychlejší ladění.

FROM mcr.microsoft.com/dotnet/runtime:6.0 JAK základ
WORKDIR /app

# Chcete-li používat schopnost aktualizovat textové vrstvy, musíte přidat následující balíčky do vašeho kontejneru
RUN apt-get update
RUN yes | apt-get install -y apt-transport-https
RUN yes | apt-get install -y libgdiplus
RUN yes | apt-get install -y libc6-dev

FROM mcr.microsoft.com/dotnet/sdk:6.0 JAK build

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

Výše je jednoduchý Dockerfile, který obsahuje následující instrukce:

- Obraz SDK, který se má použít. Zde je to obraz Microsoft .Net 6. Docker si jej stáhne při sestavení. Verze SDK je specifikována jako značka.
- Poté přidejte závislosti pro vykreslení textu.
- Následně může být potřeba instalovat písma, protože obraz SDK obsahuje velmi málo písem. Můžete také použít lokální písma zkopírovaná do obrazu Docker.
- Pracovní adresář, který je specifikován v následujícím řádku.
- Příkaz ke kopírování všeho do kontejneru, publikování aplikace a specifikace výchozího bodu.


### Sestavení a spuštění aplikace v Dockeru

#### Použití Visual Studia
Nejjednodušší způsob vyzkoušení Aspose.PSD v Dockeru je otevřít Visual Studio a spustit aplikaci pomocí podpory Dockeru
![Spusťte vzorovou aplikaci Aspose.PSD v docker pomocí Visual Studia](psd-vs-run-using-docker-support.png)

#### Použití příkazového řádku
Aplikace lze sestavit a spustit v Dockeru pomocí příkazového řádku. Otevřete oblíbený příkazový řádek, změňte adresář na složku s aplikací (složka, kde je umístěn soubor s řešením a Dockerfile) a spusťte následující příkaz:

{{< highlight plain >}}
docker build -t asposepsddocker .
{{< /highlight >}}
 
První spuštění tohoto příkazu může trvat déle, protože Docker musí stáhnout požadované obrazy. Jakmile je předchozí příkaz dokončen, spusťte následující příkaz:

{{< highlight plain >}}
docker run --name asposepsdcontainer asposepsddocker; docker cp asposepsddocker:/app/Output.psd .; docker cp asposepsddocker:/app/Output.png .; docker rm asposepsdcontainer
{{< /highlight >}}

{{% alert color="primary" %}} 

Věnujte pozornost argumentu mount, protože, jak bylo zmíněno dříve, složka na hostitelském počítači je mountována do složky kontejneru, aby bylo možné snadno zobrazit výsledky provádění aplikace. Cesty v Linuxu rozlišují velká a malá písmena.

{{% /alert %}}


## Další příklady

Pro více ukázek, jak můžete použít Aspose.PSD v Dockeru, podívejte se na [příklady](https://github.com/aspose-psd/Aspose.PSD-for-.NET).


## Viz také

- [Instalace Docker Desktop na Windows](https://docs.docker.com/docker-for-windows/install/)
- [Instalace Docker Desktop na Macu](https://docs.docker.com/docker-for-mac/install/)
- [Visual Studio 2022, NET 6 SDK](https://docs.microsoft.com/en-us/dotnet/core/install/windows?tabs=net60#dependencies)
- Možnost přepnutí na kontejnery Linuxové [přímo tady](https://docs.docker.com/docker-for-windows/#switch-between-windows-and-linux-containers)
- Další informace o [.NET Core SDK](https://hub.docker.com/_/microsoft-dotnet-sdk)

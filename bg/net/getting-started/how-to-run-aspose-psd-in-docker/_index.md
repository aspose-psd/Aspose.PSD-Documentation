---
title: Как да стартирате Aspose.PSD в Docker
type: docs
description: "Стартиране на Aspose.PSD в контейнер на Docker за Linux, Windows Server и всяка друга операционна система."
weight: 90
url: /bg/net/how-to-run-aspose-psd-in-docker/
---

## Изисквания

- Да бъде инсталиран Docker на вашия компютър. За информация относно инсталирането на Docker на Windows или Mac, вижте линковете в раздела "Вижте също".

- Visual Studio 2022.

- Използва се .NET 6 SDK в примера.

- Можете да изтеглите напълно функциониращ образец на проект от https://github.com/aspose-psd/Aspose.PSD-Docker-Sample


## Приложение Hello World

В този пример се създава проста конзолна програма Hello World, която отваря PSD файл, актуализира текстов слой и рисува използвайки Graphics API. Описаното приложение може да бъде изградено и стартирано в Docker.

### Създаване на конзолното приложение

За създаване на програмата Hello World, следвайте стъпките по-долу:
1. След като Docker е инсталиран, уверете се, че използва Linux контейнери (по подразбиране). При нужда, изберете опцията Превключи към Linux контейнерите от менюто на Docker Desktop.
1. Във Visual Studio създайте конзолно приложение .NET 6.<br>
![Диалогов прозорец за създаване на проект за конзолно приложение .NET 6](create-a-new-project.png)<br>
1. Инсталирайте най-новата версия на Aspose.PSD от NuGet.<br>
![Aspose.PSD в NuGet](nuget-aspose-psd.png)<br>
1. Тъй като приложението ще бъде стартирано върху Linux, може да бъде необходимо да инсталирате допълнителни шрифтове. Можете да предпочетете ttf-mscorefonts-installer.
1. Моля, обърнете внимание, че за използване на функциите за рендиране на текст върху Linux ще трябва да добавите следните пакети: apt-transport-https, libgdiplus, libc6-dev. Командите за тяхното добавяне могат да бъдат намерени във файла dcokerfile.
1. След като всички необходими зависимости са добавени, напишете програма, която отваря PSD файл, актуализира текстов слой и след това рисува нещо, използвайки графиките:<br>

{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "Documentation-CSharp-Aspose-Docker-Example-1.cs " >}}

Отбележете, че за редактиране на текстови слоеве е необходимо да получите лиценз. Можете да получите временна лицензия, използвайки следната статия: https://purchase.aspose.com/temporary-license
 
### Конфигуриране на Dockerfile

Следващата стъпка е да създадете и конфигурирате Dockerfile.

1. Създайте Dockerfile и го поставете до файлът на решението на вашето приложение. Запазете името на този файл без разширение (по подразбиране).
1. В Dockerfile посочете:

{{< highlight plain >}}
# Вижте https://aka.ms/containerfastmode за да разберете как Visual Studio използва този Dockerfile за изграждане на вашите изображения за по-бързо отстраняване на грешки.

FROM mcr.microsoft.com/dotnet/runtime:6.0 AS base
WORKDIR /app

# За да използвате възможността за актуализиране на текстовите слоеве трябва да добавите следните пакети в контейнера си
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

Горепосоченият Dockerfile е опростен, който съдържа следните инструкции:

- Изображението на SDK, което ще бъде използвано. Тук е изображението на Microsoft .Net 6. Docker ще го изтегли при стартирането на сборката. Версията на SDK е указана като таг.
- След това добавете зависимостите за рендиране на текста.
- След това може да трябва да инсталирате шрифтове, защото изображението на SDK съдържа много малко шрифтове. Също така можете да използвате локални шрифтове, копирани в Docker изображението.
- Работната директория, която е посочена в следващия ред.
- Командата за копиране на всичко в контейнера, публикуване на приложението и посочване на входната точка.

### Строене и Стартиране на Приложението в Docker

#### Чрез Visual Studio
Най-простият начин да опитате Aspose.PSD в Docker е да отворите Visual Studio и да стартирате приложението с поддръжка за Docker
![Стартиране на примерно приложение на Aspose.PSD в docker с помощта на Visual Studio](psd-vs-run-using-docker-support.png)

#### Чрез Команден Прозорец
Приложението може да бъде изградено и стартирано в Docker чрез командния прозорец. Отворете вашия любим команден прозорец, променете директорията към папката с приложението (папката, където се намира файлът с решението и Dockerfile) и стартирайте следната команда:

{{< highlight plain >}}
docker build -t asposepsddocker .
{{< /highlight >}}

При първоначално изпълнение на тази команда може да отнеме повече време, тъй като Docker трябва да изтегли необходимите изображения. След като предишната команда приключи, стартирайте следната команда:

{{< highlight plain >}}
docker run --name asposepsdcontainer asposepsddocker; docker cp asposepsddocker:/app/Output.psd .; docker cp asposepsddocker:/app/Output.png .; docker rm asposepsdcontainer
{{< /highlight >}}

{{% alert color="primary" %}} 

Обърнете внимание на аргумента за монтиране, защото, както вече беше споменато, папка на хост машината се монтира в папката на контейнера, за да бъде лесно видно резултатите от изпълнението на приложението. Пътищата в Linux са чувствителни към регистъра.

{{% /alert %}}


## Още Примери

За още примери как можете да използвате Aspose.PSD в Docker, вижте [примерите](https://github.com/aspose-psd/Aspose.PSD-for-.NET).


## Виж Също

- [Инсталиране на Docker Desktop на Windows](https://docs.docker.com/docker-for-windows/install/)
- [Инсталиране на Docker Desktop на Mac](https://docs.docker.com/docker-for-mac/install/)
- [Visual Studio 2022, NET 6 SDK](https://docs.microsoft.com/en-us/dotnet/core/install/windows?tabs=net60#dependencies)
- Опцията за [превключване към Linux контейнери](https://docs.docker.com/docker-for-windows/#switch-between-windows-and-linux-containers)
- Допълнителна информация за [.NET Core SDK](https://hub.docker.com/_/microsoft-dotnet-sdk)
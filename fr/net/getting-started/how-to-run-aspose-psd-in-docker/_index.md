---
title: Comment exécuter Aspose.PSD dans Docker
type: docs
description: "Exécutez Aspose.PSD dans un conteneur Docker pour Linux, Windows Server et tout autre OS."
weight: 90
url: /fr/net/comment-executer-aspose-psd-dans-docker/
---

## Prérequis

- Docker doit être installé sur votre système. Pour des informations sur comment installer Docker sur Windows ou Mac, consultez les liens de la section "Voir aussi".

- Visual Studio 2022.

- SDK NET 6 est utilisé dans l'exemple.

- Vous pouvez télécharger un projet d'exemple entièrement fonctionnel sur https://github.com/aspose-psd/Aspose.PSD-Docker-Sample


## Application Hello World

Dans cet exemple, vous créez une simple application console Hello World qui ouvre un fichier psd, met à jour une couche de texte et dessine en utilisant l'API Graphics. L'application décrite peut être construite et exécutée dans Docker.

### Création de l'Application Console

Pour créer le programme Hello World, suivez les étapes ci-dessous :
1. Une fois Docker installé, assurez-vous qu'il utilise les conteneurs Linux (par défaut). Si nécessaire, sélectionnez l'option Passer à des conteneurs Linux dans le menu Docker Desktop.
1. Dans Visual Studio, créez une application console NET 6.<br>
![Boîte de dialogue du projet d'application console NET 6](create-a-new-project.png)<br>
1. Installez la dernière version d'Aspose.PSD depuis NuGet.<br>
![Aspose.PSD sur NuGet](nuget-aspose-psd.png)<br>
1. Puisque l'application sera exécutée sur Linux, vous pourriez avoir besoin d'installer des polices supplémentaires. Vous pourriez préférer ttf-mscorefonts-installer.
1. Veuillez noter que pour utiliser les fonctionnalités de rendu de texte sur Linux, vous devez ajouter les packages suivants : apt-transport-https, libgdiplus, libc6-dev. Les commandes pour les ajouter se trouvent dans le fichier dockerfile.
1. Une fois que toutes les dépendances requises sont ajoutées, écrivez un programme simple qui ouvre le fichier PSD, met à jour la couche de texte et dessine quelque chose en utilisant des graphiques :<br>

{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "Documentation-CSharp-Aspose-Docker-Example-1.cs " >}}

Notez qu'il est nécessaire d'obtenir une licence pour éditer les couches de texte. Vous pouvez obtenir une licence temporaire en utilisant l'article suivant : https://purchase.aspose.com/temporary-license
 
### Configuration d'un Dockerfile

La prochaine étape est de créer et configurer le Dockerfile.

1. Créez le Dockerfile et placez-le à côté du fichier de solution de votre application. Gardez ce nom de fichier sans extension (par défaut).
1. Dans le Dockerfile, spécifiez :

{{< highlight plain >}}
#Voir https://aka.ms/containerfastmode pour comprendre comment Visual Studio utilise ce Dockerfile pour construire vos images pour un débogage plus rapide.

FROM mcr.microsoft.com/dotnet/runtime:6.0 AS base
WORKDIR /app

# Pour utiliser la capacité de mettre à jour les couches de texte, vous devez ajouter les packages suivants à votre conteneur
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

Le Dockerfile ci-dessus est un fichier simple qui contient les instructions suivantes :

- L'image SDK à utiliser, ici il s'agit de l'image Microsoft .NET 6. Docker la téléchargera lors de l'exécution de la construction. La version du SDK est spécifiée en tant que balise.
- Ensuite, ajoutez les dépendances pour rendre le texte.
- Ensuite, vous devrez peut-être installer des polices car l'image SDK contient très peu de polices. Vous pouvez également utiliser des polices locales copiées dans l'image Docker.
- Le répertoire de travail, qui est spécifié dans la ligne suivante.
- La commande pour copier tout dans le conteneur, publier l'application et spécifier le point d'entrée.

### Construction et Exécution de l'Application dans Docker

#### Utilisation de Visual Studio

La façon la plus simple d'essayer Aspose.PSD dans Docker est d'ouvrir Visual Studio et de lancer l'application en utilisant le support Docker
![Exécuter l'application d'exemple Aspose.PSD dans Docker en utilisant Visual Studio](psd-vs-run-using-docker-support.png)

#### Utilisation de l'invite de commande

L'application peut être construite et exécutée dans Docker en utilisant l'invite de commande. Ouvrez votre invite de commande préférée, changez de répertoire vers le dossier contenant l'application (dossier où se trouvent le fichier de solution et le Dockerfile) et exécutez la commande suivante :

{{< highlight plain >}}
docker build -t asposepsddocker .
{{< /highlight >}}

La première exécution de cette commande peut prendre plus de temps, car Docker doit télécharger les images requises. Une fois que la commande précédente est terminée, exécutez la commande suivante :

{{< highlight plain >}}
docker run --name asposepsdcontainer asposepsddocker; docker cp asposepsddocker:/app/Output.psd .; docker cp asposepsddocker:/app/Output.png .; docker rm asposepsdcontainer
{{< /highlight >}}

{{% alert color="primary" %}} 

Faites attention à l'argument de montage, car, comme mentionné précédemment, un dossier sur la machine hôte est monté dans le dossier du conteneur, pour voir facilement les résultats de l'exécution de l'application. Les chemins sous Linux sont sensibles à la casse.

{{% /alert %}}


## Plus d'Exemples

Pour plus d'exemples sur la façon dont vous pouvez utiliser Aspose.PSD dans Docker, consultez les [exemples](https://github.com/aspose-psd/Aspose.PSD-for-.NET).


## Voir aussi

- [Installer Docker Desktop sur Windows](https://docs.docker.com/docker-for-windows/install/)
- [Installer Docker Desktop sur Mac](https://docs.docker.com/docker-for-mac/install/)
- [Visual Studio 2022, SDK NET 6](https://docs.microsoft.com/en-us/dotnet/core/install/windows?tabs=net60#dependencies)
- Option de [Passer à des conteneurs Linux](https://docs.docker.com/docker-for-windows/#switch-between-windows-and-linux-containers)
- Informations supplémentaires sur [.NET Core SDK](https://hub.docker.com/_/microsoft-dotnet-sdk)

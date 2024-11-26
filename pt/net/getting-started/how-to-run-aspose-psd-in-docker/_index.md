---
title: Como Executar o Aspose.PSD no Docker
type: docs
description: "Execute o Aspose.PSD em um container Docker para Linux, Windows Server e qualquer outro sistema operacional."
weight: 90
url: /pt/como-executar-o-aspose-psd-no-docker/
---

## Pré-requisitos

- O Docker deve estar instalado no seu sistema. Para obter informações sobre como instalar o Docker no Windows ou Mac, consulte os links na seção "Veja também".

- Visual Studio 2022.

- SDK NET 6 é usado no exemplo.

- Você pode baixar um projeto de exemplo completamente funcional em https://github.com/aspose-psd/Aspose.PSD-Docker-Sample


## Aplicação Hello World

Neste exemplo, você irá criar um simples aplicativo de console Hello World que abre um arquivo psd, atualiza uma camada de texto e desenha usando a API Graphics. A aplicação descrita pode ser construída e executada no Docker.

### Criando a Aplicação de Console

Para criar o programa Hello World, siga os passos abaixo:
1. Depois de instalar o Docker, certifique-se de que ele está usando Containers Linux (padrão). Se necessário, selecione a opção "Alterar para contêineres Linux" no menu do Docker Desktop.
1. No Visual Studio, crie uma aplicação de console NET 6.<br>
![Uma caixa de diálogo do projeto de aplicativo de console NET 6](create-a-new-project.png)<br>
1. Instale a versão mais recente do Aspose.PSD do NuGet.<br>
![Aspose.PSD no NuGet](nuget-aspose-psd.png)<br>
1. Como a aplicação será executada no Linux, pode ser necessário instalar fontes adicionais. Você pode preferir o ttf-mscorefonts-installer.
1. Por favor, note que, para usar os recursos de renderização de texto no Linux, você precisa adicionar os seguintes pacotes: apt-transport-https, libgdiplus, libc6-dev. Os comandos para adicioná-los podem ser encontrados no arquivo dcokerfile.
1. Quando todas as dependências necessárias forem adicionadas, escreva um programa simples que abre o arquivo PSD, atualiza a camada de texto e, em seguida, desenha algo usando gráficos:<br>

{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "Documento-CSharp-Aspose-Docker-Exemplo-1.cs" >}}

Observe que, para editar camadas de texto, é necessário obter a licença. Você pode obter uma licença temporária usando o artigo a seguir: https://purchase.aspose.com/temporary-license
 
### Configurando um Dockerfile

O próximo passo é criar e configurar o Dockerfile.

1. Crie o Dockerfile e coloque ao lado do arquivo de solução da sua aplicação. Mantenha o nome deste arquivo sem extensão (o padrão).
1. No Dockerfile, especifique:

{{< highlight plain >}}
#Veja https://aka.ms/containerfastmode para entender como o Visual Studio usa este Dockerfile para construir suas imagens para depuração mais rápida.

FROM mcr.microsoft.com/dotnet/runtime:6.0 AS base
WORKDIR /app

# Para usar a capacidade de atualizar as camadas de texto, você precisa adicionar os seguintes pacotes ao seu contêiner
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

O acima é um Dockerfile simples, que contém as seguintes instruções:

- A imagem do SDK a ser usada. Aqui é a imagem Microsoft .Net 6. O Docker irá fazer o download dela quando a compilação for executada. A versão do SDK é especificada como uma tag.
- Em seguida, você adiciona as dependências para renderizar o texto.
- Depois, pode ser necessário instalar fontes porque a imagem do SDK contém muito poucas fontes. Além disso, você pode usar fontes locais copiadas para a imagem do Docker.
- O diretório de trabalho, que é especificado na linha seguinte.
- O comando para copiar tudo para o contêiner, publicar a aplicação e especificar o ponto de entrada.

### Compilando e Executando a Aplicação no Docker

#### Usando o Visual Studio
A maneira mais simples de experimentar o Aspose.PSD no Docker é abrir o Visual Studio e lançar o aplicativo usando o suporte ao Docker.
![Execute o aplicativo de exemplo do Aspose.PSD no Docker usando o Visual Studio](psd-vs-run-using-docker-support.png)

#### Usando o Prompt de Comando
A aplicação pode ser construída e executada no Docker usando o prompt de comando. Abra o seu prompt de comando favorito, mude o diretório para a pasta com a aplicação (pasta onde o arquivo de solução e o Dockerfile estão localizados) e execute o seguinte comando:

{{< highlight plain >}}
docker build -t asposepsddocker .
{{< /highlight >}}

Na primeira execução deste comando, pode demorar mais tempo, pois o Docker precisa baixar as imagens necessárias. Uma vez que o comando anterior seja concluído, execute o seguinte comando:

{{< highlight plain >}}
docker run --name asposepsdcontainer asposepsddocker; docker cp asposepsddocker:/app/Output.psd .; docker cp asposepsddocker:/app/Output.png .; docker rm asposepsdcontainer
{{< /highlight >}}

{{% alert color="primary" %}} 

Preste atenção ao argumento de montagem, porque, como mencionado anteriormente, uma pasta na máquina hospedeira é montada na pasta do contêiner, para ver facilmente os resultados da execução do aplicativo. Os caminhos no Linux são sensíveis a maiúsculas e minúsculas.

{{% /alert %}}


## Mais Exemplos

Para mais amostras de como você pode usar o Aspose.PSD no Docker, consulte os [exemplos](https://github.com/aspose-psd/Aspose.PSD-for-.NET).


## Veja também

- [Instalar Docker Desktop no Windows](https://docs.docker.com/docker-for-windows/install/)
- [Instalar Docker Desktop no Mac](https://docs.docker.com/docker-for-mac/install/)
- [Visual Studio 2022, NET 6 SDK](https://docs.microsoft.com/en-us/dotnet/core/install/windows?tabs=net60#dependencies)
- Opção de [Alterar para contêineres Linux](https://docs.docker.com/docker-for-windows/#switch-between-windows-and-linux-containers)
- Informações adicionais sobre o [SDK .NET Core](https://hub.docker.com/_/microsoft-dotnet-sdk)


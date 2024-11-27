---
title: Cómo ejecutar Aspose.PSD en Docker
type: docs
description: "Ejecute Aspose.PSD en un contenedor Docker para Linux, Windows Server y cualquier sistema operativo."
weight: 90
url: /es/net/como-ejecutar-aspose-psd-en-docker/
---

## Requisitos previos

- Docker debe estar instalado en su sistema. Para obtener información sobre cómo instalar Docker en Windows o Mac, consulte los enlaces en la sección "Consulte también".

- Visual Studio 2022.

- Se utiliza el SDK de .NET 6 en el ejemplo.

- Puede descargar un proyecto de muestra completamente funcional en https://github.com/aspose-psd/Aspose.PSD-Docker-Sample


## Aplicación Hello World

En este ejemplo, creará una aplicación de consola simple Hello World que abre un archivo psd, actualiza una capa de texto y dibuja usando la API de Gráficos. La aplicación descrita puede ser construida y ejecutada en Docker.

### Creación de la aplicación de consola

Para crear el programa Hello World, siga los pasos que se indican a continuación:
1. Una vez instalado Docker, asegúrese de que esté utilizando Contenedores de Linux (predeterminado). Si es necesario, seleccione la opción Cambiar a contenedores de Linux desde el menú de Docker Desktop.
1. En Visual Studio, cree una aplicación de consola de .NET 6.<br>
![Un cuadro de diálogo de proyecto de aplicación de consola .NET 6](create-a-new-project.png)<br>
1. Instale la última versión de Aspose.PSD desde NuGet.<br>
![Aspose.PSD en NuGet](nuget-aspose-psd.png)<br>
1. Dado que la aplicación se ejecutará en Linux, es posible que necesite instalar fuentes adicionales. Puede preferir ttf-mscorefonts-installer.
1. Tenga en cuenta que, para utilizar las funciones de renderización de texto en Linux, necesitará agregar los siguientes paquetes: apt-transport-https, libgdiplus, libc6-dev. Los comandos para agregarlos se pueden encontrar en el dockerfile.
1. Una vez agregadas todas las dependencias necesarias, escriba un programa sencillo que abra el archivo PSD, actualice la capa de texto y luego dibuje algo utilizando gráficos:<br>

{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "Documentation-CSharp-Aspose-Docker-Example-1.cs" >}}

Tenga en cuenta que para editar capas de texto necesitará obtener la licencia. Puede obtener una licencia temporal utilizando el siguiente artículo: https://purchase.aspose.com/temporary-license
 
### Configuración de un Dockerfile

El siguiente paso es crear y configurar el Dockerfile.

1. Cree el Dockerfile y colóquelo junto al archivo de solución de su aplicación. Mantenga el nombre de este archivo sin extensión (el predeterminado).
1. En el Dockerfile, especifique:

{{< highlight plain >}}
#Consulte https://aka.ms/containerfastmode para comprender cómo Visual Studio utiliza este Dockerfile para compilar sus imágenes para depuración más rápida.

FROM mcr.microsoft.com/dotnet/runtime:6.0 AS base
WORKDIR /app

# Para usar la capacidad de actualizar las capas de texto, es necesario agregar los siguientes paquetes a su contenedor
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

Lo anterior es un Dockerfile simple, que contiene las siguientes instrucciones:

- La imagen del SDK que se utilizará. Aquí es la imagen de Microsoft .Net 6. Docker la descargará cuando se ejecute la compilación. La versión del SDK se especifica como una etiqueta.
- Luego se agregan las dependencias para renderizar el texto.
- Después, es posible que necesite instalar fuentes porque la imagen del SDK contiene muy pocas fuentes. También puede usar fuentes locales copiadas a la imagen de Docker.
- El directorio de trabajo, que se especifica en la línea siguiente.
- El comando para copiar todo en el contenedor, publicar la aplicación y especificar el punto de entrada.

### Construcción y ejecución de la aplicación en Docker

#### Usando Visual Studio
La forma más sencilla de probar Aspose.PSD en Docker es abrir Visual Studio y lanzar la aplicación utilizando el soporte de Docker.
![Ejecute la aplicación de ejemplo de Aspose.PSD en Docker usando Visual Studio](psd-vs-run-using-docker-support.png)

#### Usando el Símbolo del sistema
La aplicación se puede compilar y ejecutar en Docker utilizando el símbolo del sistema. Abra su símbolo del sistema favorito, cambie al directorio con la aplicación (donde se encuentran el archivo de solución y el Dockerfile) y ejecute el siguiente comando:

{{< highlight plain >}}
docker build -t asposepsddocker .
{{< /highlight >}}

La primera vez que se ejecuta este comando, puede tardar más tiempo, ya que Docker necesita descargar las imágenes requeridas. Una vez que el comando anterior se haya completado, ejecute el siguiente comando:

{{< highlight plain >}}
docker run --name asposepsdcontainer asposepsddocker; docker cp asposepsddocker:/app/Output.psd .; docker cp asposepsddocker:/app/Output.png .; docker rm asposepsdcontainer
{{< /highlight >}}

{{% alert color="primary" %}} 

Preste atención al argumento de montaje, porque, como se mencionó anteriormente, se monta una carpeta en la máquina host en la carpeta del contenedor, para ver fácilmente los resultados de la ejecución de la aplicación. Las rutas en Linux distinguen mayúsculas de minúsculas.

{{% /alert %}}


## Más ejemplos

Para obtener más ejemplos de cómo se puede usar Aspose.PSD en Docker, consulte los [ejemplos](https://github.com/aspose-psd/Aspose.PSD-for-.NET).


## Consulte también

- [Instalar Docker Desktop en Windows](https://docs.docker.com/docker-for-windows/install/)
- [Instalar Docker Desktop en Mac](https://docs.docker.com/docker-for-mac/install/)
- [Visual Studio 2022, SDK de .NET 6](https://docs.microsoft.com/es-es/dotnet/core/install/windows?tabs=net60#dependencies)
- Opción Cambiar a contenedores de Linux en [documentación de Docker](https://docs.docker.com/docker-for-windows/#switch-between-windows-and-linux-containers)
- Información adicional sobre [SDK de .NET Core](https://hub.docker.com/_/microsoft-dotnet-sdk)


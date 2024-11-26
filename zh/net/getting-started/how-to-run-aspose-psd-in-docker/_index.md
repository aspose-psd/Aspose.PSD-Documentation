---
title: 如何在Docker中运行Aspose.PSD
type: docs
description: "在Linux、Windows Server和任何操作系统的Docker容器中运行Aspose.PSD。"
weight: 90
url: /zh/net/how-to-run-aspose-psd-in-docker/
---

## 先决条件

- 必须在您的系统上安装Docker。有关如何在Windows或Mac上安装Docker的信息，请参考“参考资料”部分中的链接。

- Visual Studio 2022。

- 示例中使用了.NET 6 SDK。

- 您可以从 https://github.com/aspose-psd/Aspose.PSD-Docker-Sample 下载完全的工作示例项目。


## Hello World 应用程序

在本示例中，您将创建一个简单的Hello World控制台应用程序，该应用程序打开一个psd文件，更新文本层并使用Graphics API进行绘制。所述应用程序可在Docker中构建和运行。

### 创建控制台应用程序

要创建Hello World程序，请按照以下步骤操作：
1. 安装Docker后，请确保它使用Linux容器（默认）。必要时，从Docker Desktops菜单中选择切换到Linux容器选项。
1. 在Visual Studio中创建一个NET 6控制台应用程序。<br>
![NET 6控制台应用程序项目对话框](create-a-new-project.png)<br>
1. 从NuGet安装最新的Aspose.PSD版本。<br>
![NuGet上的Aspose.PSD](nuget-aspose-psd.png)<br>
1. 由于该应用程序将在Linux上运行，您可能需要安装额外的字体。您可以优先选择ttf-mscorefonts-installer。
1. 请注意，在Linux上使用文本渲染功能，您需要添加以下软件包：apt-transport-https、libgdiplus、libc6-dev。可以在dcokerfile中找到添加它们的命令。
1. 当所有所需的依赖项添加完毕后，编写一个简单的程序，打开PSD文件，更新文本层，然后使用Graphics绘制某些内容：<br>

{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "Documentation-CSharp-Aspose-Docker-Example-1.cs " >}}

请注意，要编辑文本层，您需要获取许可证。您可以使用以下文章获取临时许可证：https://purchase.aspose.com/temporary-license
 
### 配置Dockerfile

下一步是创建和配置Dockerfile。

1. 创建Dockerfile，并将其放置在应用程序的解决方案文件旁边。将此文件的名称保持无扩展名（默认）。
1. 在Dockerfile中指定：

{{< highlight plain >}}
#请查看 https://aka.ms/containerfastmode 了解 Visual Studio 如何使用此Dockerfile为您的图像构建供更快调试。

FROM mcr.microsoft.com/dotnet/runtime:6.0 AS base
WORKDIR /app

# 为使用更新文本层功能，您需要将以下软件包添加到您的容器
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

以上是一个简单的Dockerfile，包含以下指令：

- 要使用的SDK镜像。这里是Microsoft .Net 6镜像。Docker将在运行构建时下载该镜像。SDK的版本被指定为一个标签。
- 接着添加渲染文本所需的依赖项。
- 然后，您可能需要安装字体，因为SDK镜像包含的字体非常少。您还可以将本地字体复制到Docker镜像中使用。
- 指定的工作目录，它在下一行中被指定。
- 复制所有内容到容器中、发布应用程序并指定入口点的命令。

### 在Docker中构建和运行应用程序

#### 使用Visual Studio
尝试在Docker中运行Aspose.PSD的最简单方法是打开Visual Studio并使用Docker支持启动应用程序
![使用Visual Studio在Docker中运行Aspose.PSD示例应用程序](psd-vs-run-using-docker-support.png)

#### 使用命令提示符
可以使用命令提示符在Docker中构建和运行应用程序。打开您喜欢的命令提示符，更改到应用程序所在的文件夹（解决方案文件和Dockerfile所在的文件夹）并运行以下命令：

{{< highlight plain >}}
docker build -t asposepsddocker .
{{< /highlight >}}

第一次执行该命令可能需要较长时间，因为Docker需要下载所需的镜像。完成前一个命令后，运行以下命令：

{{< highlight plain >}}
docker run --name asposepsdcontainer asposepsddocker; docker cp asposepsddocker:/app/Output.psd .; docker cp asposepsddocker:/app/Output.png .; docker rm asposepsdcontainer
{{< /highlight >}}

{{% alert color="primary" %}} 

请注意挂载参数，因为如前所述，主机机器上的文件夹被挂载到容器的文件夹中，以便轻松查看应用程序执行结果。在Linux中，路径区分大小写。

{{% /alert %}}


## 更多示例

有关如何在Docker中使用Aspose.PSD的更多示例，请参阅[示例](https://github.com/aspose-psd/Aspose.PSD-for-.NET)。


## 参考资料

- [在Windows上安装Docker Desktop](https://docs.docker.com/docker-for-windows/install/)
- [在Mac上安装Docker Desktop](https://docs.docker.com/docker-for-mac/install/)
- [Visual Studio 2022, NET 6 SDK](https://docs.microsoft.com/en-us/dotnet/core/install/windows?tabs=net60#dependencies)
- [切换到Linux容器](https://docs.docker.com/docker-for-windows/#switch-between-windows-and-linux-containers) 选项
- 有关.NET Core SDK的其他信息，请访问[此处](https://hub.docker.com/_/microsoft-dotnet-sdk)



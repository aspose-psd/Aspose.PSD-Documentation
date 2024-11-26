---
title: Aspose.PSDをDockerで実行する方法
type: docs
description: "Linux、Windows Server、および他のOS用にAspose.PSDをDockerコンテナで実行します。"
weight: 90
url: /ja/net/how-to-run-aspose-psd-in-docker/
---

## 前提条件

- システムにDockerがインストールされている必要があります。WindowsまたはMacにDockerをインストールする方法については、「関連リンク」セクションのリンクを参照してください。

- Visual Studio 2022。

- NET 6 SDK を使用しています。

- https://github.com/aspose-psd/Aspose.PSD-Docker-Sample から完全に動作するサンプルプロジェクトをダウンロードできます。


## Hello Worldアプリケーション

この例では、psdファイルを開き、テキストレイヤーを更新し、Graphics APIを使用して描画するシンプルなHello Worldコンソールアプリケーションを作成します。説明されているアプリケーションはDockerでビルドおよび実行することができます。

### コンソールアプリケーションの作成

Hello Worldプログラムを作成するために、以下の手順に従ってください：
1. Dockerがインストールされていることを確認し、Linuxコンテナを使用していることを確認してください（デフォルトの設定）。必要であれば、Docker Desktopのメニューから "Switch to Linux containers" オプションを選択してください。
1. Visual Studioで、NET 6コンソールアプリケーションを作成します。<br>
 ![NET 6コンソールアプリケーションプロジェクトのダイアログ](create-a-new-project.png)<br>
1. NuGetから最新バージョンのAspose.PSDをインストールします。<br>
 ![NuGet上のAspose.PSD](nuget-aspose-psd.png)<br>
1. アプリケーションはLinuxで実行されるため、追加のフォントをインストールする必要があります。ttf-mscorefonts-installer を使用できます。
1. リンクスライブラリを使用するには、Linuxにて以下のパッケージを追加する必要があります: apt-transport-https、libgdiplus、libc6-dev。これらを追加するコマンドはdockerfile内で見つけることができます。
1. 必要な依存関係がすべて追加されたら、PSDファイルを開き、テキストレイヤーをアップデートし、次に何かを描画する簡単なプログラムを記述します。<br>

{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "Documentation-CSharp-Aspose-Docker-Example-1.cs " >}}

テキストレイヤーを編集するにはライセンスが必要です。一時ライセンスを取得するには、次の記事をご覧ください: https://purchase.aspose.com/temporary-license
 
### Dockerfileの構成

次のステップは、Dockerfileを作成および構成することです。

1. Dockerfileを作成し、アプリケーションのソリューションファイルと同じ場所に配置します。このファイルの拡張子を除いて、デフォルトの名前を保持します。
1. Dockerfileに、以下を指定します：

{{< highlight plain >}}
# Visual Studioが高速デバッグのためにこのDockerfileを使用する方法については、https://aka.ms/containerfastmode を参照してください。

FROM mcr.microsoft.com/dotnet/runtime:6.0 AS base
WORKDIR /app

# テキストレイヤーを更新するための依存関係を追加するために、以下のパッケージをコンテナに追加するための命令
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

上記は、以下の命令を含む簡単なDockerfileです：

- 使用されるSDKイメージ。ここでは Microsoft .Net 6 イメージが使用されています。ビルド時にDockerがこれをダウンロードします。SDKのバージョンはタグとして指定されています。
- 次に、テキストをレンダリングするための依存関係を追加します。
- その後、SDKイメージには非常に少ないフォントしか含まれていないため、フォントをインストールする必要があります。また、Dockerイメージにコピーされたローカルフォントを使用することができます。
- 次の行で指定されている作業ディレクトリ。
- すべてをコンテナにコピーし、アプリケーションを公開し、エントリーポイントを指定するコマンド。

### Dockerでアプリケーションのビルドと実行

#### Visual Studioを使用する
DockerでAspose.PSDを試す最も簡単な方法は、Visual Studioを開いてDockerサポートを使用してアプリを起動することです
![Visual Studioを使用してDockerでAspose.PSDサンプルアプリを実行](psd-vs-run-using-docker-support.png)

#### コマンドプロンプトを使用する
お好きなコマンドプロンプトを開き、コマンドプロンプトでアプリケーションをビルドおよびDockerで実行することができます。アプリケーションのあるフォルダ（ソリューションファイルとDockerfileが配置されているフォルダ）に移動し、次のコマンドを実行します：

{{< highlight plain >}}
docker build -t asposepsddocker .
{{< /highlight >}}

このコマンドを初めて実行すると、必要なイメージをダウンロードする必要があるため、時間がかかる場合があります。前のコマンドが完了したら、次のコマンドを実行してください：

{{< highlight plain >}}
docker run --name asposepsdcontainer asposepsddocker; docker cp asposepsddocker:/app/Output.psd .; docker cp asposepsddocker:/app/Output.png .; docker rm asposepsdcontainer
{{< /highlight >}}

{{% alert color="primary" %}} 

ホストマシンのフォルダがコンテナのフォルダにマウントされているため、アプリケーションの実行結果を簡単に見ることができます。Linuxではパスは大文字と小文字を区別しますので、マウント引数に注意してください。

{{% /alert %}}

## その他の例

DockerでAspose.PSDを使用する方法のさらなるサンプルについては、[examples](https://github.com/aspose-psd/Aspose.PSD-for-.NET)を参照してください。


## 関連リンク

- [WindowsにDocker Desktopをインストールする](https://docs.docker.com/docker-for-windows/install/)
- [MacにDocker Desktopをインストールする](https://docs.docker.com/docker-for-mac/install/)
- [Visual Studio 2022、NET 6 SDK](https://docs.microsoft.com/en-us/dotnet/core/install/windows?tabs=net60#dependencies)
- [WindowsとLinuxコンテナを切り替える](https://docs.docker.com/docker-for-windows/#switch-between-windows-and-linux-containers) オプション
- [.NET Core SDKに関する追加情報](https://hub.docker.com/_/microsoft-dotnet-sdk)


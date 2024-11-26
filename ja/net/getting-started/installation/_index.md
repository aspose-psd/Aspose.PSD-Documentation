---
title: インストール
type: ドキュメント
weight: 50
url: /ja/net/installation/
description: NuGetまたはパッケージマネージャコンソールを使用して、PSDファイル形式ライブラリをインストールします。 
---

## **NuGetを使ってAspose.PSD for .NETをインストールする**
NuGetは、Aspose APIを.NET用にダウンロードしてインストールする最も簡単な方法です。Microsoft Visual Studioを開き、NuGetパッケージマネージャを開きます。"aspose"を検索して、必要なAspose APIを見つけます。"Install"をクリックすると、選択したAPIがダウンロードされ、プロジェクトに参照されます。

![todo:image_alt_text](installation_1.png)

## **パッケージマネージャコンソールを使用してAspose.PSDをインストールまたはアップデートする**
以下の手順に従って、パッケージマネージャコンソールを使用して[Aspose.PSD API](https://www.nuget.org/packages/Aspose.psd/)を参照できます。

1. Visual Studioでソリューション/プロジェクトを開きます。
1. メニューからTools -> Library Package Manager -> Package Manager Consoleを選択して、パッケージマネージャコンソールを開きます。

![todo:image_alt_text](installation_2.png)

コマンド "**Install-Package Aspose.Psd**" と入力し、Enterキーを押して最新のフルリリースをアプリケーションにインストールします。代わりに、最新のリリースとホットフィックスを含むリリースがインストールされるように、コマンドに "**-prerelease**" サフィックスを追加することもできます。

![todo:image_alt_text](installation_3.png)

ウィンドウの下部に **"Aspose.PSDのインストール中"** のメッセージが表示されるのを確認できます。

![todo:image_alt_text](installation_4.png)

ダウンロードが完了すると、次の確認メッセージが表示されます。[Aspose EULA](https://company.aspose.com/legal/eula) に馴染みがない場合は、URLで参照されているライセンスを読むことをお勧めします。

![todo:image_alt_text](installation_5.png)

Aspose.PSDが正常に追加および参照されたことが確認できるはずです。

![todo:image_alt_text](installation_6.png)

パッケージマネージャコンソールでは、コマンド "**Update-Package Aspose.Psd**" と入力し、Enterキーを押してAspose.Psdパッケージのアップデートを確認し、存在する場合はインストールすることができます。最新のリリースを更新する場合は、"-prerelease" サフィックスを追加することもできます。

## **共有サーバー環境で実行する際の考慮事項**
全てのAspose .NETコンポーネントは、フルトラスト権限セットで実行することを推奨しています。これは、Aspose .NETコンポーネントが時には仮想ディレクトリ以外の場所にあるレジストリ設定やファイルにアクセスする必要があるためです（たとえばフォントを読み取る場合など）。さらに、Aspose.NETコンポーネントは、一部の場合にはフルトラスト権限を必要とするコア.NETシステムクラスに基づいています。

異なる企業からの複数のアプリケーションをホストするインターネットサービスプロバイダーは、ほとんどの場合、ミディアムトラストセキュリティレベルを強制します。.NET 2.0の場合、このセキュリティレベルは、Aspose.Wordsが正常に機能する能力に影響を与える可能性がある、以下の制約を設定する可能性があります。

- **RegistryPermission** は利用できません。これにより、文書をレンダリングする際にインストールされたフォントを列挙する必要があるため、レジストリにアクセスできません。
- **FileIOPermission** が制限されています。これにより、アプリケーションの仮想ディレクトリ階層内のファイルにのみアクセスできます。これは、エクスポート中にフォントを読み取ることができない可能性があります。

上記の理由から、Aspose.PSDはフルトラスト権限で実行することをお勧めします。さまざまなタスクを実行する際に、いくつかのライブラリの機能がミディアムトラストで機能する一方、一部の機能が機能しない場合があります（例: レンダリング）これはGDI+画像処理へのコールによるものです。
 
## **MSIパッケージ経由でインストールされた.NET Core DLLを使用する**
**ご注意:** MSIパッケージを介してインストールされた .Net Standard DLL を使用している場合は、.Net Standard バージョンと連携するために必要な依存関係を追加する必要があります。

|**Visual Studio dependencies screenshot**|**CsProj file fragment:**|
| :- | :- |
|![todo:image_alt_text](installation_7.png)|<ItemGroup><p></p><p>`    `<PackageReference Include="System.Drawing.Common" Version="4.5.1" /></p><p>`    `<PackageReference Include="System.Text.Encoding.CodePages" Version="4.5.0" /></p><p></p></ItemGroup>|
## **システム要件**
### **サポートされるオペレーティングシステム:**
- Microsoft Windows 2000 Professional and Server (SP2 推奨)
- Microsoft Windows XP Professional and Home Edition
- Microsoft Windows 2003 Server
- Microsoft Windows Vista
- Microsoft Windows 2008 Server
- Microsoft Windows 2008 Server R2
- Microsoft Windows 7
- Microsoft Windows 8
- Microsoft Windows 10
- Microsoft Windows 11
### **サポートされるプラットフォーム:**
- Window forms
- Web forms
- Visual Studio 2005
- Visual Studio 2008
- Visual Studio 2010
- Visual Studio 2012
- Visual Studio 2013
- Visual Studio 2015
- Visual Studio 2017
- Visual Studio 2019
- Visual Studio 2022

Aspose.PSDは、上記にリストされたオペレーティングシステムのx86およびx64バージョンの両方で動作します。
### **サポートされるフレームワーク:**
Aspose.PSD for .NET は以下の.NETフレームワークをサポートしています。

- .NET Framework バージョン2.0以上
- .NET Standard 2.0

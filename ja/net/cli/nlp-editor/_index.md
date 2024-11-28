---
title: Aspose.PSD CLI NLPエディターアプリケーション for .NET
type: docs
weight: 10
url: /ja/net/cli/nlp-editor/
is_root: false
keywords: CLI Photoshop Tool NLP Natural-Language-Processing PSD Console C# Library PSD API
description: Aspose.PSDベースのNLPエディターCLIアプリケーションは、PSD、PSB、およびAIファイルフォーマットを使用してPSDファイルを編集するためのものです。No-code CI/CD Automationが可能です。PSDファイルの編集には自然言語でリクエストを書くだけで、変換、調整、リサイズなどのさまざまな操作を実行できます。Adobe PhotoshopやAdobe Illustratorのインストールは不要で、追加のコードなしにコンソールから実行できます。
---

**![Aspose.PSD for .NET Product Logo](home_1.png)**

**Aspose.PSD NLPエディターCLIアプリケーション for .NETへようこそ**

Aspose.PSD CLI NLPエディターアプリケーションは、自然言語コマンドを使用してPSDファイルを編集するための軽量なコンソールユーティリティです。CI/CDパイプラインへの簡単な統合が可能です。

**免責事項**

これは実験的なアプリケーションです。お試しください。フィードバックは大変ありがたいです。No-Codeアプリケーションをさらに進化させていきたいと考えています。どんなビルドパイプラインやビジネスプロセスにも簡単に統合できることを目標としています。

**.NET向けAspose.PSD NLPエディターCLIアプリケーションの主な機能**

1. 自然言語コマンドを使用して、PSD、PSB、AIファイルでの操作を実行します。
2. 変換、調整、リサイズなど、さまざまな操作をサポートしています。
3. No-code CI/CD自動化が可能です。
4. PSDファイルの編集のために自然言語でリクエストを書くことができます。

## **コマンドラインからの使用方法:**

{{% alert color="primary" %}}
まず、このdotnetツールをインストールしてください:
{{< highlight bash >}}dotnet tool install --global Aspose.PSD.CLI.NLP.Editor --version 24.6.0{{< /highlight >}}

最初に以下のコマンドを実行してください：
{{< highlight bash >}}Aspose.PSD.CLI.NLP.Editor --setup nlp.cli{{< /highlight >}}
このコマンドを実行すると、短い名前nlp.cliでこのアプリケーションを実行できるようになります。独自の短い名前を指定することも可能です。
{{% /alert %}}

**Aspose.PSD.CLI.Cropアプリケーションの利用可能なパラメータ**

| **引数**    | **説明**                     |
|:-------------|:----------------------------|
| 任意のテキスト | 必須。自然言語でPSDまたはPSBファイルを更新するコマンド      |
| ライセンス     | ライセンスへのパス。               |
| 詳細         | 特定のコマンドの詳細情報を表示します。 |
| セットアップ     | コンソールからのクイックコール用にtoolsフォルダに.batファイルを作成します。例: --setup psd.nlp。その後、psd.nlpコマンドでツールを呼び出すことができます。 |

**使用例**

1. このコマンドは、最初に見つかったファイル（Aspose.PSDで開くことができるもの）をカレントフォルダからpng形式で透過付きで保存します。また、ライセンスを設定します。ライセンスは1度だけ指定する必要があります。次回以降は指定されたパスからライセンスが使用されます。このコマンドは、NLP処理の詳細なログが利用可能な場合には、その処理の詳細を表示します。
{{< highlight bash >}}
  nlp.cli Convert file from this folder to png format with alpha --license "C:\Aspose\LicenseFile.lic --verbose "
{{< /highlight >}}

2. このコマンドは、"smth.psd"に最も類似した名前のファイルを見つけ、コントラストを調整し、最高の品質でjpeg形式で保存します。出力ファイルの名前が表示されます。それはsmth.jpgになります。
{{< highlight bash >}}
Adjust contrast on 10 of layer with name ellipse in file smth.psd and save it to output.jpg with best quality
{{< /highlight >}}

3. このコマンドは、指定されたパスのファイルを開き、サイズを25%に縮小します。出力ファイルが表示されます。ファイルは、コンソールのカレントフォルダに保存されます。
{{< highlight bash >}}
Resize file C:\Users\someuser\Desktop\input.psd to 25%
{{< /highlight >}}

4. このコマンドは、C:\Users\someuser\Desktop\でinput.psdファイルを見つけ、インデックスが3であるレイヤーを見つけ、幅50px、高さ100pxにリサイズします。その後、このレイヤーはC:\Users\someuser\Desktop\output.pdfにPDF形式で保存されます。
{{< highlight bash >}}
 Resize layer with index 3 of C:\Users\someuser\Desktop\input.psd to width 50 and height 100 and save it to C:\Users\someuser\Desktop\output.pdf
 {{< /highlight >}}

 5. このコマンドは、カレントフォルダのsmth.psdを開きますが、すべての効果を無効にします。その後、このファイルはBMP形式に変換され、current folderにoutput.bmpとして保存されます。
 {{< highlight bash >}}
 Open smth.psd without effects and save it to output.bmp
 {{< /highlight >}}

**他の[Aspose.PSD CLI Applications](https://docs.aspose.com/psd/net/cli)を .NETに追加する必要がある場合は、チェックしてください**

1. [Aspose.PSD CLI Convert](/psd/ja/net/cli/convert)
2. [Aspose.PSD CLI Crop](/psd/ja/net/cli/crop)
3. [Aspose.PSD CLI Resize](/psd/ja/net/cli/resize)
4. [Aspose.PSD CLI Export](/psd/ja/net/cli/export)
5. [Aspose.PSD CLI NLP Editor](/psd/ja/net/cli/nlp-editor)

**Aspose.PSD for .NETまたは[他のプラットフォーム]をご確認ください**

Aspose.PSD CLI Applicationsは一般的な操作に対して即座に使用できるソリューションです。柔軟なソリューションが必要な場合は、Aspose.PSDのフルバージョンをチェックしてください。

1. [Aspose.PSD for .NET](https://releases.aspose.com/psd/net/)
2. [Aspose.PSD for Java](https://releases.aspose.com/psd/java/) 
3. [Aspose.PSD for Python via .NET](https://releases.aspose.com/psd/python-net/)

## **Aspose.PSD for .NETリソース**

以下は、作業を完了するために必要ないくつかの便利なリソースへのリンクです。

- [Aspose.PSD CLI Applications for .NETオンラインドキュメント](/psd/ja/net/cli/conversion)
- [Aspose.PSD for CLI Applications for .NETリリースノート](/psd/ja/net/cli/conversion/release-notes/)
- [Aspose.PSD for CLI Applications .NET製品ページ](https://products.aspose.com/psd/net/cli)
- [Aspose.PSD for .NET APIリファレンスガイド](https://reference.aspose.com/net/psd)
- [GitHubリポジトリで例をダウンロード](https://github.com/aspose-psd/CLI-Applications)
- [Aspose.PSD for .NET無料サポートフォーラム](https://forum.aspose.com/c/psd)
- [Aspose.PSD for .NET有料サポートヘルプデスク](https://helpdesk.aspose.com/)


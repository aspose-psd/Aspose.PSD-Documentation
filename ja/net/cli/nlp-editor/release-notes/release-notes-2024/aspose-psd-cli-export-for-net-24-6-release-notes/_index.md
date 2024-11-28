---
title: Aspose.PSD CLI NLP Editor for .NET 24.6 - リリースノート
type: docs
weight: 90
url: /ja/net/cli/nlp-editor/aspose-psd-nlp-editor-cli-app-for-net-24-6-release-notes/
---
{{% alert color="primary" %}}

このページには [Aspose.PSD CLI NLP Editor for .NET 24.6](https://www.nuget.org/packages/Aspose.PSD.CLI.NLP.Editor/) のリリースノートが含まれています。

{{% /alert %}}

| **Key**     | **Summary**                                                                                 | **Category** |
|:------------|:--------------------------------------------------------------------------------------------|:-------------|
| PSDNET-2110 | Aspose.PSD CLI Apps の初版リリース: Aspose.PSD.CLI.Export と Aspose.PSD.CLI.NLP.Editor      |  拡張 |


## **使用例:**

**PSDNET-2110. Aspose.PSD CLI NLP Editor アプリケーションの初版リリース**

## **コマンドラインからの使用:**

{{% alert color="primary" %}}
まず、この dotnet ツールをインストールしてください:
{{< highlight bash >}}dotnet tool install --global Aspose.PSD.CLI.NLP.Editor --version 24.6.0{{< /highlight >}}

最初にこのコマンドを実行することをお勧めします:
{{< highlight bash >}}Aspose.PSD.CLI.NLP.Editor --setup nlp.cli{{< /highlight >}}
このコマンドを実行すると、Aspose.PSD.CLI.NLP.Editor の代わりに短い名前 nlp.cli でこのアプリケーションを実行できるようになります。独自の短い名前を指定することもできます。
{{% /alert %}}

**使用例**

1. このコマンドは、現在のフォルダから最初に見つかったファイル（Aspose.PSD で開けるもの）を png 形式で透過率付きで保存します。また、ライセンスを設定します。ライセンスは一度だけ指定する必要があります。次回以降は指定されたパスからライセンスが使用されます。このコマンドは、NLP処理の詳細なログを表示します。
{{< highlight bash >}}nlp.cli Convert file from this folder to png format with alpha --license "C:\Aspose\LicenseFile.lic --verbose "{{< /highlight >}}

2. このコマンドは、"smth.psd" に最も類似した名前のファイルを見つけます。その後、コントラストを調整して最高品質で jpeg 形式で保存します。出力ファイルの名前が表示されます。それは smth.jpg になります。
{{< highlight bash >}}Adjust contrast on 10 of layer with name ellipse in file smth.psd and save it to output.jpg with best quality{{< /highlight >}}

3. このコマンドは指定されたパスのファイルを解析し、サイズを25%に縮小します。出力ファイルが表示されます。それはコンソールの現在のフォルダに保存されます。
{{< highlight bash >}}Resize file C:\Users\someuser\Desktop\input.psd to 25%{{< /highlight >}}

4. このコマンドは、C:\Users\someuser\Desktop\ にある input.psd ファイルを見つけます。その後、インデックス 3 のレイヤーを見つけ、幅 50px、高さ 100px にリサイズします。その後、このレイヤーを C:\Users\someuser\Desktop\output.pdf に PDF として保存します。
{{< highlight bash >}}Resize layer with index 3 of C:\Users\someuser\Desktop\input.psd to width 50 and height 100 and save it to C:\Users\someuser\Desktop\output.pdf{{< /highlight >}}

5. このコマンドは、現在のフォルダにある smth.psd を開きますが、すべてのエフェクトが無効になります。その後、このファイルを BMP 形式に変換して、output.bmp として現在のフォルダに保存します。
{{< highlight bash >}}Open smth.psd without effects and save it to output.bmp{{< /highlight >}}

**免責事項**

これは実験的なアプリケーションです。お試しください。フィードバックを残していただけると幸いです。NO-Code アプリケーションを次のレベルに引き上げたいと考えています。どんなビルドパイプラインやビジネスプロセスでも簡単に統合できることが私たちの目標です。


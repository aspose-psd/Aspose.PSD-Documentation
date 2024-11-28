---
title: 例を実行する方法
type: ドキュメント
weight: 90
url: /ja/net/how-to-run-the-examples/
description: GitHub にホストされている PSD ファイル形式ライブラリに関連する例を実行する方法を学びます。
---

## **Software Requirements**
以下の要件を満たしてから、例をダウンロードして実行してください。

1. Visual Studio 2010 以上
1. Visual Studio に NuGet パッケージマネージャがインストールされていること。最新の NuGet API バージョンが Visual Studio にインストールされていることを確認してください。NuGet パッケージマネージャのインストール方法の詳細については、[http://docs.nuget.org/ndocs/guides/install-nuget](http://docs.nuget.org/ndocs/guides/install-nuget) をご確認ください。
1. Tools->Options->NuGet Package Manager->Package Sources に移動し、**nuget.org** オプションがチェックされていることを確認してください。
1. 例プロジェクトは NuGet Automatic Package Restore 機能を使用しているため、アクティブなインターネット接続が必要です。例を実行するマシンにアクティブなインターネット接続がない場合は、例プロジェクトに Aspose.Imaging.dll の参照を追加するために[Installation](/psd/ja/net/installation/)をご確認ください。

## **Download from GitHub**
Aspose.PSD for .NET のすべての例は、[GitHub](https://github.com/aspose-psd/Aspose.PSD-for-.NET) にホストされています。

- 好きな GitHub クライアントでリポジトリをクローンするか、[こちら](https://github.com/aspose-psd/Aspose.PSD-for-.NET/archive/master.zip) から ZIP ファイルをダウンロードできます。
- ZIP ファイルの内容をコンピューターの任意のフォルダに展開してください。すべての例は **Examples** フォルダにあります。
- C# 用の Visual Studio ソリューションファイルがあります。
- プロジェクトは Visual Studio 2013 で作成されていますが、ソリューションファイルは Visual Studio 2010 SP1 以上と互換性があります。
- Visual Studio でソリューションファイルを開き、プロジェクトをビルドしてください。
- 初回実行時に依存関係が NuGet 経由で自動的にダウンロードされます。
- **Examples** のルートフォルダにある **Data** フォルダには、C# の例で使用する入力ファイルが含まれています。必ず **Data** フォルダを例プロジェクトと一緒にダウンロードしてください。
- RunExamples.cs ファイルを開き、すべての例はここから呼び出されます。
- プロジェクト内から実行したい例のコメントを外してください。

設定や例の実行に問題がある場合は、フォーラムを使用してお気軽にお問い合わせください。

## **Contribute**
例を追加または改善したい場合は、プロジェクトに貢献することをお勧めします。このリポジトリのすべての例やショーケースプロジェクトはオープンソースであり、自分のアプリケーションで自由に使用できます。

貢献するには、リポジトリをフォークし、ソースコードを編集してプルリクエストを作成してください。変更点を確認し、役立つものであればリポジトリに取り込みます。

---
title: Aspose.PSD Adapters for .NETフルマニュアル
type: docs
weight: 10
url: /ja/net/adapters/full-manual
keywords: アダプターフルマニュアルPSD PSB AI WebP SVG PNG JPEG TIFF GIF BMP クイックスタートガイド
description: Aspose.PSDアダプターフルマニュアル。
---

## 概要

これは、Aspose.PSDアダプターを使用してAspose.PSDの機能を拡張する方法についての詳細なマニュアルです。
アダプターは特別なNugetパッケージで、他のAspose製品とのシームレスな統合を可能にし、追加の統合コードの記述なしに、ファイルをさまざまな未サポート形式にスムーズにエクスポートできるようにします。

## ライセンスの適用

アダプターにライセンスを適用する方法についての詳細は、[ライセンスの適用に関する記事](/psd/ja/net/adapters/license)をご確認ください。

{{% alert color="primary" %}}
アダプターを使用するには、Aspose.PSDとadapteesの両方のライセンスが必要です。
{{% /alert %}}

次のサンプルを使用してライセンスを適用できます。
{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "Aspose-PSD-Adapters-CSharp-License.cs" >}}

プロジェクトの初期化モジュールでライセンスを一度適用することをお勧めします。

## Aspose.PSDアダプターの参照

まず、[Nuget](https://www.nuget.org/aspose.psd.adapters.imaging)からAspose.PSD.Adapters.Imagingを参照するか、[Asposeリリースページ](https://releases.aspose.com/psd/net/)からダウンロードしてください（Adaptersはこの時点でメインリリースアーティファクトに含まれているため、別個のバイナリとして含まれています）。

![必要な参照](references.png)

他の追加パッケージの参照も必要になる可能性があります


## アダプティブのローダーとエクスポーターの有効化

### アダプターの有効化
アダプターを使用する必要がある場合は、次のコードを使用してください：
{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "Adapters-CSharp-Enable-Adapters.cs" >}}


### アダプターの無効化
開発プロセスでアダプターを無効にすべき状況に遭遇するかもしれません。これは、一つのコード部分でAspose.PSDのローダーを使用し、他のコード部分でAdapteesのローダーを使用する必要がある一般的なケースです。この場合、次のコードを使用してください：
{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "Adapters-CSharp-Disable-Adapters.cs " >}}

## アダプターを使用して画像をロードする

アダプターを使用すると、SVGやWebPなどの[Aspose.PSDでサポートされていない一般的な形式をロード]((/ja/net/adapters/load-unsupported-formats))できます。

### 簡単な使用方法
次のコードを使用して読み込むだけです：
{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "Adapters-CSharp-Add-Imaging-Adapters-Loading-Unsupported-Formats.cs" >}}

### 複雑な画像処理のための中間的な使用
Adapteeによって提供される追加のオプションを指定する必要がある場合は、次の例をチェックしてください：
{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "Aspose-PSD-Adapters-CSharp-Full-Manual-Complex-Loading.cs" >}}

すべてのイメージング機能を使用してSVGイメージを操作し、1つのメソッド呼び出しでエクスポートできます。

## アダプターを使用して画像をエクスポートする

Aspose.PSDでは[サポートされていない形式を開く必要がない](/ja/net/adapters/load-unsupported-formats)場合や、[それにエクスポート](/ja/net/adapters/export-to-unsupported-formats)する必要がある場合があります。この場合、エクスポーターを有効にして、次のコードを使用してください：
{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "Adapters-CSharp-Add-Imaging-Adapters-Exporting-to-Unsupported-Formats.cs" >}}

## 結論

Aspose.PSDアダプターを使用してファイルをロードおよびエクスポートすると、開発者にとって画期的な変化となります。これらの強力なNugetパッケージを使用すると、Aspose.PSDを他のAspose製品とシームレスに統合でき、追加の統合コードの書き込みなしにサポートされていないファイル形式を簡単に開いて操作できるようになります。Aspose.PSDアダプターを使用すると、余分なコードや手作業の変換プロセスが不要になり、時間と労力を節約できます。ファイルの読み込みやエクスポートに関係なく、Aspose.PSDアダプターは、プロジェクトに新たな可能性を開く便利で効率的なソリューションを提供します。Aspose.PSDアダプターの力を体験して、開発プロセスを次のレベルに引き上げましょう。

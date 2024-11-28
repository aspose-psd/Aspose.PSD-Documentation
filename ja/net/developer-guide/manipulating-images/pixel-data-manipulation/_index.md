---
title: Pixel Data Manipulation using Aspose.PSD for C#
weight: 100
type: docs
description: 直接かつ迅速にPSD C# APIを使用して生のピクセルデータを更新する方法の例
keywords: [ピクセルの編集, psdの編集, レイヤーの編集, 生データ操作, psdデータの編集, psd api, C#, csharp, コードサンプル]
url: ja/net/pixel-data-manipulation/
---

## Introduction

Aspose.PSDは、C#でAdobe Photoshopファイル（PSD）を操作できる強力なライブラリです。この記事では、Aspose.PSD for C#を使用してPSDファイル内のピクセルデータを操作する方法について探ってみます。

## 概要

提供されるコードは、PSDファイルを作成し、新しいレイヤーを追加し、ピクセルデータを直接操作して変更した画像を保存する方法を示しています。

### ピクセルデータを操作する手順

1. **必要なモジュールのインポート**:
   必要なモジュールをインポートします。Aspose.PSDライブラリから`PsdImage`および`Layer`クラスをインポートする必要があります。

2. **入力および出力ファイルパスを定義**:
   入力および出力ファイルパスを指定します。

3. **入力ファイルをストリームとして開く**:
   読み取りモードで`FileStream`クラスを使用して入力ファイルをストリームとして開きます。ストリームをロードして`PsdImage`オブジェクトを作成します。

4. **新しいPSD画像の作成**:
   `PsdImage`コンストラクタを使用して新しいPSD画像を作成し、レイヤーの幅と高さを引数として提供します。

5. **PSD画像にレイヤーを割り当て**:
   レイヤーをPSD画像の`Layers`プロパティに割り当てます。

6. **ピクセルデータを操作**:
   `LoadArgb32Pixels`メソッドを使用してレイヤーからARGB32ピクセルをロードします。ピクセルの長さに基づいてインデックスの範囲を定義し、必要に応じてピクセル値を変更します。

7. **変更されたピクセルデータを保存**:
   `SaveArgb32Pixels`メソッドを使用して変更されたピクセルデータをレイヤーに保存します。

8. **PSD画像を保存**:
   `Save`メソッドを使用してPSD画像を出力ファイルに保存します。

### 例

以下は、Aspose.PSD for C#を使用してピクセルデータを操作する方法を示すコードサンプルです:

{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "PixelDataManipulation-PixelDataManipulation.cs" >}}

### 要約

Aspose.PSD for C#は、PSDファイル内のピクセルデータを操作するための強力な機能セットを提供します。特定の条件に基づいてピクセルを修正する必要がある場合や複雑なパターンを作成する場合でも、Aspose.PSDはこれらのタスクを簡単かつ効率的に行うことができます。

詳細な情報や例については、[Aspose.PSD for C#のドキュメント](https://docs.aspose.com/psd/net/)をご覧ください。

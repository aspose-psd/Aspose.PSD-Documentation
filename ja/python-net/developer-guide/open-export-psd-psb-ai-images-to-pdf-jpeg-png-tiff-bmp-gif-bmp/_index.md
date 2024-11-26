---
title: PSD、PSB、AIファイルを開き、PDF、PNG、TIFF、GIF、BMP、JPEGにエクスポートする
weight: 100
type: docs
description: 他の形式へのPSD、PSB、AIファイルのエクスポートの例
keywords: [psdを開く、aiを開く、psbを開く、pngにエクスポート、pdfにエクスポート、jpegにエクスポート、tiffにエクスポート、psd api, python, コードサンプル]
url: ja/python-net/open-export-psd-psb-ai-images-to-pdf-jpeg-png-tiff-bmp-gif-bmp/
---

## **概要**
PSD、PSB、AIファイルを異なる形式に変換するには、PythonでAspose.PSDライブラリを使用することができます。このライブラリは、変換プロセスをカスタマイズするためのさまざまなオプションと設定を提供します。

まず、Aspose.PSDライブラリから必要なクラスとモジュールをインポートする必要があります。コードを実行する前にライブラリをインストールしていることを確認してください。

このコードでは、PNG、PDF、TIFF、JPEG、BMP、JPEG2000、GIF、PSB、PSDなどのさまざまな形式のために様々なオプションを定義しています。これらのオプションにより、出力ファイルを要件に応じてカスタマイズすることができます。

次に、ファイル拡張子をそれぞれの保存オプションにマッピングするformatsという辞書を定義します。

PSDファイルを他の形式に変換するには、PsdImage.load()を使用してPSDファイルをロードし、formatsの順に繰り返します。各形式に対して、出力ファイル名を指定し、image.save()メソッドを使って画像を保存します。

同様に、AIファイルを他の形式に変換するには、AiImage.load()を使用してAIファイルをロードし、formatsの順に繰り返します。出力ファイル名を指定し、image.save()メソッドを使って画像を保存します。

ソースのPSDファイルとAIファイルに正しいファイルパスを指定してください。

以上です！このコードを使用して、PythonのAspose.PSDを使用してPSD、PSB、AIファイルをさまざまな形式に変換できます。

フル例をご確認ください。

## **例**
{{< gist "aspose-com-gists" "04e945e867d0b7f39bb3eab63074d04c" "Documentation-Python-Aspose-Psd-open-export-psd-psb-ai-images-to-pdf-jpeg-png-tiff-bmp-gif-bmp.py" >}}

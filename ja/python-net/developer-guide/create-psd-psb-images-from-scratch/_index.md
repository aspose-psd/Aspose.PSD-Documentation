---
title: Pythonを使用してゼロからPSDまたはPSB画像を作成する
weight: 100
type: docs
description: PythonでAspose.PSDを使用してPsdイメージをゼロから作成する方法の例
keywords: [psd作成, psb作成, 新規作成, レイヤー作成, テキストレイヤー作成, psd api, python, コードサンプル]
url: ja/python-net/create-psd-psb-images-from-scratch/
---

## **概要**
PythonでAspose.PSDを使用してゼロからPSDまたはPSBファイルを作成するには、以下の手順に従うことができます：

Aspose.PSDライブラリから必要なモジュールとクラスをインポートします：
```python 
from aspose.psd import Graphics, Pen, Color, Rectangle
from aspose.psd.brushes import LinearGradientBrush
from aspose.psd.fileformats.psd import PsdImage
```

出力ファイルの名前とパスを指定します：

```python 
outputFile = "CreateFileFromScratchExample.psd"
```

所定の寸法でPSDイメージを作成します：

```python 
with PsdImage(500, 500) as img:
```

通常のPSDレイヤーを追加し、グラフィックAPIを使用してそれを更新します：

```python 
regularLayer = img.add_regular_layer()
graphics = Graphics(regularLayer)
pen = Pen(Color.alice_blue)
brush = LinearGradientBrush(Rectangle(250, 250, 150, 100), Color.red, Color.aquamarine, 45)
graphics.draw_ellipse(pen, Rectangle(100, 100, 200, 200))
graphics.fill_ellipse(brush, Rectangle(250, 250, 150, 100))
```

テキストレイヤーを作成します：
```python 
textLayer = img.add_text_layer("Sample Text", Rectangle(200, 200, 100, 100))
```

テキストレイヤーにドロップシャドウエフェクトを追加します：
```python 
dropShadowEffect = textLayer.blending_options.add_drop_shadow()
dropShadowEffect.distance = 0
dropShadowEffect.size = 8
dropShadowEffect.color = Color.blue
```

PSDファイルを保存します：
```python 
img.save(outputFile)
```

このコードは、500x500ピクセルの寸法を持つPSD画像を作成します。通常のレイヤーを追加し、ペンとブラシを使用してその上に楕円を描画します。そして、「Sample Text」というテキストを持つテキストレイヤーを追加し、それにドロップシャドウエフェクトを適用します。最後に、指定した出力ファイル名でPSDファイルを保存します。

このコードが機能するには、Python環境にAspose.PSDライブラリを正しくインストールおよび設定している必要があります。ライブラリのインストール方法や使用方法については、公式Aspose.PSDドキュメントを参照してください。

完全な例をご確認ください。

## **例**
{{< gist "aspose-com-gists" "04e945e867d0b7f39bb3eab63074d04c" "Documentation-Python-Aspose-Psd-create-psd-psb-images-from-scratch.py" >}}

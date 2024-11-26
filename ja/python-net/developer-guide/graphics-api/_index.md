---
title: PSDファイルでレイヤーを編集するためにGraphics APIを使用する
weight: 100
type: docs
description: PythonのAspose.PSDでGraphics APIを使用する例
keywords: [レイヤーを更新, 円を描く, 楕円を描く, 塗りつぶされた円を描く, グラフィックス, psd api, python, コードサンプル]
url: ja/python-net/graphics-api/
---

## **概要**
まず、Image.load()メソッドを使用してPSDファイルを読み込むか、ゼロからPsd Imageを作成する必要があります。この例では、inputFile変数はPSDファイルへのパスを表し、loadOptはロードオプションを表します（ある場合）。

```python 
with Image.load(inputFile, loadOpt) as image:
    psdImage = cast(PsdImage, image)
```
次に、psdImage.layers[0]構文を使用してPSD画像の最初のレイヤーにアクセスできます。これにより、操作できるレイヤーオブジェクトへの参照が得られます。

```python 
layer = psdImage.layers[0]
```
レイヤーを編集するには、グラフィックスオブジェクトを作成する必要があります。これには、レイヤーをパラメーターとして渡します。このオブジェクトには、図形の描画やブラシの適用に関するさまざまなメソッドが用意されています。

```python 
graphics = Graphics(layer)
```
コード例では、Penオブジェクトを作成して楕円形の輪郭の色と太さを定義します。Color.alice_blue定数は色を表し、必要に応じて太さを調整できます。

```python 
pen = Pen(Color.alice_blue)
```
同様に、LinearGradientBrushオブジェクトを作成して楕円形の塗りつぶし色を定義します。Rectangle(250, 250, 150, 100)は楕円形の位置とサイズを表し、Color.redとColor.aquamarineはグラデーションの開始色と終了色を表します。

```python 
brush = LinearGradientBrush(Rectangle(250, 250, 150, 100), Color.red, Color.aquamarine, 45)
```
レイヤーに楕円形を描画するには、graphics.draw_ellipse()メソッドを使用します。Rectangle(100, 100, 200, 200)は楕円形の位置とサイズを表します。

```python 
graphics.draw_ellipse(pen, Rectangle(100, 100, 200, 200))
```
グラデーションブラシで楕円形を塗りつぶすには、graphics.fill_ellipse()メソッドを使用します。Rectangle(250, 250, 150, 100)は楕円形の位置とサイズを表します。

```python 
graphics.fill_ellipse(brush, Rectangle(250, 250, 150, 100))
```
レイヤーを編集した後、変更したPSD画像をpsdImage.save()メソッドを使用して保存できます。この例では、psdName変数が変更したPSDファイルを保存するパスを表します。

```python 
psdImage.save(psdName)
```
追加で、PngOptionsクラスを使用してPNGなど、他の形式で変更した画像を保存することもできます。pngName変数はPNGファイルを保存するパスを表します。

```python 
psdImage.save(pngName, PngOptions())
```
以上です！PythonのAspose.PSDのGraphics APIを使用してPSDファイルのレイヤーを編集する方法を正常に学びました。Aspose.PSDライブラリのさらなる機能や機能を探索して、画像編集の能力を向上させてください。

フルな例を確認してください。

## **例**
{{< gist "aspose-com-gists" "04e945e867d0b7f39bb3eab63074d04c" "Documentation-Python-Aspose-Psd-graphics-api.py " >}}

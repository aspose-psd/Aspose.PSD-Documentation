---
title: Aspose.PSD for .NET 22.12 - リリースノート
type: docs
weight: 10
url: /ja/net/aspose-psd-for-net-22-12-release-notes/
---

{{% alert color="primary" %}}

このページには、[Aspose.PSD for .NET 22.12](https://www.nuget.org/packages/Aspose.PSD/) のリリースノートが含まれています。

{{% /alert %}}

{{% alert color="success" %}}

- このリリースでは、16ビットエクスポートのリグレッションが修正されました。

{{% /alert %}}

|**キー**|**概要**|**カテゴリ**|
| :- | :- | :- |
|PSDNET-1336|IText インターフェースに編集可能な TextOrientation プロパティを追加|機能|
|PSDNET-725|レイヤーマスクを使用した指定された PSD ファイルのリサイズが正しくないマスクを生成する|バグ|
|PSDNET-1277|16個の画像のマスクを保存およびロードする機能を追加|バグ|
|PSDNET-1281|16ビット画像を16または8ビット画像への保存時の不正確な透過|バグ|
|PSDNET-1375|16ビットカラーでの CMYK の修正|バグ|


## **パブリック API の変更**
# **追加された API:**
- T:Aspose.PSD.FileFormats.Psd.TextOrientation
- F:Aspose.PSD.FileFormats.Psd.TextOrientation.Horizontal
- F:Aspose.PSD.FileFormats.Psd.TextOrientation.Vertical
- P:Aspose.PSD.FileFormats.Psd.Layers.Text.IText.TextOrientation


# **削除された API:**
- なし


## **使用例:**

**PSDNET-725. レイヤーマスクを使用した指定された PSD ファイルのリサイズが正しくないマスクを生成する**

{{< highlight csharp >}}
string sourceFile = "source.psd";
string psdExportPath = "output.psd";
string pngExportPath = "output.png";

// ソース PSD ファイルを開きます
using (PsdImage image = (PsdImage)Image.Load(sourceFile))
{
    const int Scale = 4;

    int newWidth = image.Width * Scale;
    int newHeight = image.Height * Scale;

    // リサイズを実行します
    image.Resize(newWidth, newHeight);
    image.Save(psdExportPath, new PsdOptions(image));
}

// リサイズされた PSD ファイルを開きます
using (PsdImage image = (PsdImage)Image.Load(psdExportPath))
{
    // PNG にレンダリングします
    image.Save(pngExportPath, new PngOptions());
}
{{< /highlight >}}

**PSDNET-1277. 16個の画像のマスクを保存およびロードする機能を追加**

{{< highlight csharp >}}
string source8bitPsdFile = @"input_8bitColor.psd";
string output16bitPsdFile = @"output_16bitColor.psd";

using (var image = (PsdImage)Image.Load(source8bitPsdFile))
{
    // 16ビットカラーを保存するオプション
    PsdOptions options16 = new PsdOptions { ChannelBitsCount = 16, ColorMode = ColorModes.Rgb};

    // PSD ファイルを透過で保存します
    image.Save(output16bitPsdFile, options16);
}
{{< /highlight >}}

**PSDNET-1281. 16ビット画像を16または8ビット画像への保存時の不正確な透過**

{{< highlight csharp >}}
string sourceFile = @"Example_16bit.psd";
string resavedFile = @"Resave_16bit.psd";
string imageFile = @"TotalImage_16bit.png";

// 16ビットカラー PSD ファイル（透過あり）を開き、16ビットカラーに保存します
using (var image = (PsdImage)Image.Load(sourceFile))
{
    PsdOptions options16 = new PsdOptions() { ChannelBitsCount = 16, ColorMode = ColorModes.Rgb };
    image.Save(resavedFile, options16);
}

// 16ビットカラー PSD ファイルを PNG ファイルに透過でレンダリングします
using (var image = (PsdImage)Image.Load(resavedFile))
{
    image.Save(imageFile, new PngOptions() { ColorType = Aspose.PSD.FileFormats.Png.PngColorType.TruecolorWithAlpha });
}
{{< /highlight >}}

**PSDNET-1336. IText インターフェースに編集可能な TextOrientation プロパティを追加**

{{< highlight csharp >}}
// 以下のコードは、新しい TextOrientation プロパティを編集する機能を示しています。
// これは現時点ではレンダリングには影響しませんが、プロパティ値を編集するだけであることに注意してください。

string src = "1336test.psd";
string output = "out_1336test.psd";

using (var image = (PsdImage)Image.Load(src))
{
    var textLayer = image.Layers[1] as TextLayer;
    if (textLayer.TextData.TextOrientation == TextOrientation.Vertical)
    {
        // 正しい読み込み
    }
    else
    {
        throw new Exception("TextOrientation プロパティ値の読み込みが正しくありません");
    }

    textLayer.TextData.TextOrientation = TextOrientation.Horizontal;
    textLayer.TextData.UpdateLayerData();

    image.Save(output);
}

using (var image = (PsdImage)Image.Load(output))
{
    var textLayer = image.Layers[1] as TextLayer;
    if (textLayer.TextData.TextOrientation == TextOrientation.Horizontal)
    {
        // 正しい読み込み
    }
    else
    {
        throw new Exception("TextOrientation プロパティ値の読み込みが正しくありません");
    }
}
{{< /highlight >}}

**PSDNET-1375. 16ビットカラーでの CMYK の修正**

{{< highlight csharp >}}
string srcFile = @"ClippingMaskRegular.psd";
string exportPath = @"export.psd";
string pngExportPath = @"export.png";

// 変換オプションの設定
PsdOptions psdOptions = new PsdOptions()
{
    ColorMode = ColorModes.Cmyk,
    ChannelBitsCount = 16,
    ChannelsCount = 5,
    CompressionMethod = CompressionMethod.Raw
};

// 変換して保存
using (var image = (PsdImage)Image.Load(srcFile))
{
    image.Convert(psdOptions);
    image.Save(exportPath);
}

// 変換されたファイルを開き、PNG にレンダリングする
using (PsdImage image = (PsdImage)Image.Load(exportPath))
{
    image.Save(pngExportPath, new PngOptions() { ColorType = PngColorType.TruecolorWithAlpha });
}
{{< /highlight >}}

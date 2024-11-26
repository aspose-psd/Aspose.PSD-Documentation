---
title: Aspose.PSD for .NET 22.11 - リリースノート
type: docs
weight: 20
url: /ja/net/aspose-psd-for-net-22-11-release-notes/
---

{{% alert color="primary" %}}

このページには、[Aspose.PSD for .NET 22.11](https://www.nuget.org/packages/Aspose.PSD/) のリリースノートが含まれています。

{{% /alert %}}

{{% alert color="warning" %}}

- このリリースでは、16ビットエクスポートの場合にリグレッションがありますので、この機能を使用する際には注意してください。
16ビットの画像処理が主な機能である場合、Aspose.PSD を 22.9-22.11 に更新しないでください。

これらの問題への対処に取り組んでいます。

{{% /alert %}}

|**キー**|**サマリー**|**カテゴリ**|
| :- | :- | :- |
|PSDNET-1320|非常に大きな PSB ファイルをエクスポートできません|強化|
|PSDNET-659|放射グラデーションの中心を移動可能にする|機能|
|PSDNET-1330|特定のファイルのための ZipWithoutPrediction 圧縮メソッドをサポートしていません|機能|
|PSDNET-735|レイヤーのための変換メソッドを使用した後に、保存されたレイヤーの境界ボックスが正しくありません|バグ|
|PSDNET-1234|パターンを持つ PSD 画像の読み込み時に例外が発生|バグ|
|PSDNET-1244|中国語の記号を含む PSD ファイルを保存する際に画像のエクスポートが失敗 (IndexOutOfRangeException)|バグ|
|PSDNET-1303|TimeLine ActiveFrame が誤って適用される|バグ|
|PSDNET-1307|リグレッション 22.7: アラビア文字を含むテキストのレンダリングが不正確|バグ|
|PSDNET-1321|グループレイヤー上のベクトルマスクの動作が不正確です。最終画像には黒い穴がありますが、そうではありません|バグ|


## **パブリック API の変更**
# **追加された API:**
- M:Aspose.PSD.FileFormats.Psd.Layers.TextLayer.Resize(System.Int32,System.Int32,Aspose.PSD.ResizeType)


# **削除された API:**
- なし


## **使用例:**

**PSDNET-659. 放射グラデーションの中心を移動可能にする**

{{< highlight csharp >}}
string sourceFile = "psdnet659.psd";
string outputFile = "output.png";

using (var psdImage = (PsdImage)Image.Load(sourceFile))
{
    FillLayer radialLayer = (FillLayer)psdImage.Layers[5];
    GradientFillSettings settings = (GradientFillSettings)radialLayer.FillSettings;

    // オフセットポイントを更新
    settings.HorizontalOffset = 10;
    settings.VerticalOffset = -25;

    psdImage.Save(outputFile, new PngOptions());
}
{{< /highlight >}}

**PSDNET-735. レイヤーのための変換メソッドを使用した後に、保存されたレイヤーの境界ボックスが正しくありません**

{{< highlight csharp >}}
string sourceFileName = @"TextLayer.psd";
string outputFile = "TextLayerResized_output.psd";

using (PsdImage image = (PsdImage)Image.Load(sourceFileName, new PsdLoadOptions()))
{
    TextLayer textLayer = (TextLayer)image.Layers[1];

    // テキストレイヤーの新しいサイズを設定する
    const int NewWidth = 250;
    const int NewHeight = 250;

    // リサイズ関数がレイヤーをどのようにリサイズするかのメカニズムを設定する（デフォルト値）
    ResizeType resizeType = ResizeType.NearestNeighbourResample;

    // ここでテキストレイヤーのリサイズを行う
    // レイヤーだけでなく、テキストレイヤーの変換行列も変更されます
    textLayer.Resize(NewWidth, NewHeight, resizeType);

    image.Save(outputFile, new PsdOptions(image));
}

using (PsdImage image = (PsdImage)Image.Load(outputFile, new PsdLoadOptions()))
{
    TextLayer txtLayer = (TextLayer)image.Layers[1];

    // デフォルトのフォントが異なるため、デルタの理由が異なります
    if (txtLayer.TransformMatrix[4] >= 65 
        && txtLayer.TransformMatrix[4] <= 67
        && txtLayer.TransformMatrix[5] >= 234
        && txtLayer.TransformMatrix[5] <= 237)
    {
        // 問題ありません
    }
    else
    {
        throw new Exception("位置ポイントが間違っています");
    }
}
{{< /highlight >}}

**PSDNET-1234. パターンを持つ PSD 画像の読み込み時に例外が発生**

{{< highlight csharp >}}
string srcFile = "test.psd";
string output = "output1234.png";

using (PsdImage psdImage = (PsdImage)PsdImage.Load(srcFile,
new PsdLoadOptions() { LoadEffectsResource = true }))
{
    PngOptions pngOptions = new PngOptions() { ColorType = PngColorType.TruecolorWithAlpha };
    psdImage.Save(output, pngOptions);
}
{{< /highlight >}}

**PSDNET-1244. 中国語の記号を含む PSD ファイルを保存する際に画像のエクスポートが失敗**

{{< highlight csharp >}}
string sourceFile = "input.psd";
string outputPath = "output.psd";

var loadOptions = new PsdLoadOptions
{
    LoadEffectsResource = true,
    UseDiskForLoadEffectsResource = true
};

using (var image = (PsdImage)Image.Load(sourceFile, loadOptions))
{
    foreach (var layer in image.Layers)
    {
        if (layer.Name == "1")
        {
            var txtLayer = (TextLayer)layer;

            txtLayer.UpdateText("测试测试");
        }
    }

    // ここで例外が発生してはいけません。
    image.Save(outputPath, new PsdOptions() { CompressionMethod = CompressionMethod.RLE, ColorMode = ColorModes.Rgb });
}
{{< /highlight >}}

**PSDNET-1303. TimeLine ActiveFrame が誤って適用**

{{< highlight csharp >}}
string src = "timeline1303.psd";
string output = "out_timeline.psd";

using (var psdImage = (PsdImage)Image.Load(src))
{
    TimeLine timeLine = TimeLine.InitializeFrom(psdImage);

    timeLine.ActiveFrame = 2;
    timeLine.ApplyTo(psdImage);

    psdImage.Save(output);
}
{{< /highlight >}}

**PSDNET-1307. リグレッション 22.7: アラビア文字を含むテキストのレンダリングが不正確**

{{< highlight csharp >}}
string testFontsFolder = "Fonts";
FontSettings.SetFontsFolder(testFontsFolder);
FontSettings.UpdateFonts();

string sourceFilePath = "sarbarg.fin12.psd";
string outputFilePath = "result.tiff";

using (var psdImage = (PsdImage)Image.Load(sourceFilePath))
{
    psdImage.Save(outputFilePath, new Aspose.PSD.ImageOptions.TiffOptions(TiffExpectedFormat.TiffLzwRgb));
}
{{< /highlight >}}

**PSDNET-1320. 非常に大きな PSB ファイルをエクスポートできません**

{{< highlight csharp >}}
string sourceFile = "hf-mim-liman-han-guc-art-kuvvet.psb";
string psdExportPath = "hf-mim-liman-han-guc-art-kuvvet.png";

using (var image = (PsdImage)Image.Load(sourceFile, new PsdLoadOptions() { ReadOnlyMode = true }))
{
    image.Save(psdExportPath, new PngOptions() { ColorType =  PngColorType.TruecolorWithAlpha });
}
{{< /highlight >}}

**PSDNET-1321. グループレイヤー上のベクトルマスクの動作が不正確。最終画像には黒い穴がありますが、そうではありません**

{{< highlight csharp >}}
string srcFile = "demo.psd";
string output = "demo_net.png";

using (PsdImage im = (PsdImage)PsdImage.Load(srcFile))
{
    PngOptions pngOptions = new PngOptions() { ColorType = PngColorType.TruecolorWithAlpha };
    im.Save(output, pngOptions);
}
{{< /highlight >}}

**PSDNET-1330. 特定のファイルのための ZipWithoutPrediction 圧縮メソッドをサポートしていません**

{{< highlight csharp >}}
string sourceFile = "20221017_220706_0000.psd";
string outputFile = "20221017_220706_0000.jpg";

using (var image = (PsdImage)Image.Load(sourceFile, new PsdLoadOptions() { LoadEffectsResource = true }))
{
    ImageOptionsBase optionsBase = new JpegOptions() { Quality = 80 };
    image.Save(outputFile, optionsBase);
}
{{< /highlight >}}

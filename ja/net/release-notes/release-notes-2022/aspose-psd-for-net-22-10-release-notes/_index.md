---
title: Aspose.PSD for .NET 22.10 - リリースノート
type: docs
weight: 30
url: /ja/net/aspose-psd-for-net-22-10-release-notes/
---

{{% alert color="primary" %}}

このページには、[Aspose.PSD for .NET 22.10](https://www.nuget.org/packages/Aspose.PSD/) のリリースノートが含まれています。

{{% /alert %}}

{{% alert color="warning" %}}

- このリリースでは、16ビットエクスポートの場合にリグレッションが発生しているため、この機能を使用する際は注意を払うことをお勧めします。
16ビット画像処理が主な機能である場合は、Aspose.PSD を 22.9〜22.10 にアップデートしないでください。

これらの問題に対する解決策を開発中です。

{{% /alert %}}

|**キー**|**概要**|**カテゴリ**|
| :- | :- | :- |
|PSDNET-1287|Lfx2Resource における旧式のプロパティを削除|強化|
|PSDNET-1071|ZipWithoutPrediction 圧縮を使用して PSD (RGB/16ビット) を開けない|バグ|
|PSDNET-1257|タイムライン効果が消えて奇妙な方法で表示される（Photoshop内）|バグ|
|PSDNET-1278|内部位置にストローク効果の透過性が機能していない|バグ|
|PSDNET-1279|リグレッション：PSD ファイルのオープン時エラー|バグ|
|PSDNET-1284|一部のアジアのシンボルでテキスト更新が失敗。特定のシンボルのパースエラー|バグ|
|PSDNET-1291|一部のアジアのシンボルでテキスト更新に失敗。特定のシンボルのレンダリングエラー|バグ|
|PSDNET-1292|特定のアジアのシンボルを保存した後に Photoshop で書き出したファイルを開く際にエラー|バグ|


## **パブリック API 変更**
# **追加された API:**
- なし


# **削除された API:**
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.Lfx2Resource.Data
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.Lfx2Resource.BlendMode
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.Lfx2Resource.EffectColor
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.Lfx2Resource.Opacity


## **使用例:**

**PSDNET-1071. Aspose.PSD が ZipWithoutPrediction 圧縮を使用した PSD (RGB/16ビット) を開けない場合**

{{< highlight csharp >}}
string src = "237708.psd";
string output = "out_237708.psd";

using (var psdImage = (PsdImage)Image.Load(src))
{
    psdImage.Save(output);
}
{{< /highlight >}}

**PSDNET-1257. タイムライン効果が消えて奇妙な方法で表示される（Photoshop内）**

{{< highlight csharp >}}
string sourceFile = "clearFile.psd";
string outputFile = "output_not_clearFile.psd";

using (var psdImage = (PsdImage)Image.Load(sourceFile))
{
    // いくつかのフレームを持つタイムラインを作成します。
    TimeLine timeLine = TimeLine.InitializeFrom(psdImage);
    var layerIds = timeLine.LayerIds;

    List<Frame> frames = new List<Frame>(timeLine.Frames);
    for (int i = 0; i < 3; i++)
    {
        frames.Add(new Frame(timeLine));
    }
    timeLine.Frames = frames.ToArray();

    timeLine.Frames[1].LayerStates[layerIds[1]].StateEffects.AddColorOverlay();

    timeLine.Frames[2].LayerStates[layerIds[1]].StateEffects.AddGradientOverlay();
    timeLine.Frames[2].LayerStates[layerIds[1]].StateEffects.IsVisible = false;

    timeLine.ApplyTo(psdImage);

    psdImage.Save(outputFile);
}
{{< /highlight >}}

**PSDNET-1278. 内部位置にストローク効果の透過性が機能していない**

{{< highlight csharp >}}
string sourceFile = "psdnet1278.psd";
string output = "out_1278.png";

using (var image = (PsdImage)Image.Load(sourceFile, new PsdLoadOptions() { LoadEffectsResource = true }))
{
    image.Save(output, new PngOptions());
}
{{< /highlight >}}

**PSDNET-1279. リグレッション：PSD ファイルのオープン時エラー**

{{< highlight csharp >}}
string sourceFile = "AllTypesLayerPsd.psd";
string outputPsd = "out_1279.psd";

using (var image = (PsdImage) Image.Load(sourceFile))
{
    image.Save(outputPsd);
}
{{< /highlight >}}

**PSDNET-1284. 一部のアジアのシンボルでテキスト更新が失敗。特定のシンボルのパースエラー**

{{< highlight csharp >}}
string testData = @"尐少尒尓尔尕尖尗尘尙尚尛尜尝尞尟尠尡尢尣尤尥尦尧尨尩尪尫尬尭尮尯尰就尲尳尴尵尶尷尸尹尺尻尼尽尾尿局屁层屃屄居屆屇屈屉届屋屌屍屎屏";

testData = testData.Substring(25, 1); // 問題のシンボルを選択

string srcFile = "TestFileForAsianCharsBig.psd";
string output = "output.psd";

using (var image = (PsdImage)Image.Load(srcFile))
{
    var layer = (TextLayer)image.Layers[0];
    layer.UpdateText(testData);
    image.Save(output);
}
{{< /highlight >}}

**PSDNET-1287. Lfx2Resource における旧式のプロパティを削除**

{{< highlight csharp >}}
string src = "fileWithEffects.psd";
string output = "output.psd";

using (var psdImage = (PsdImage)Image.Load(src, new PsdLoadOptions() { LoadEffectsResource = true }))
{
    var layer = psdImage.Layers[1];
    var effect = layer.BlendingOptions.Effects[0];

    // エフェクトの BlendMode オプションを更新
    effect.BlendMode = BlendMode.Darken;

    // エフェクトの Opacity オプションを更新
    effect.Opacity = 128; // 50%

    // ストローク効果の塗りつぶし色オプションを更新
    var strokeSettings = (IColorFillSettings)((StrokeEffect)effect).FillSettings;
    strokeSettings.Color = Color.DarkRed;

    psdImage.Save(output);
}
{{< /highlight >}}

**PSDNET-1291. 一部のアジアのシンボルでテキスト更新に失敗。特定のシンボルのレンダリングエラー**

{{< highlight csharp >}}
string testData = @"咐咑咒咓咔咕咖咗咘咙咚咛咜咝咞咟咠咡咢咣咤咥咦咧咨咩咪咫咬咭咮咯咰咱咲咳咴咵咶咷咸咹咺咻咼咽咾咿
哀品哂哃哄哅哆哇哈哉哊哋哌响哎哏";

testData = testData.Substring(40, 25); // 問題のシンボルを選択

string srcFile = "TestFileForAsianCharsBig 2.psd";
string output = "output.psd";

using (var image = (PsdImage)Image.Load(srcFile))
{
    var layer = (TextLayer)image.Layers[0];
    layer.UpdateText(testData);
    image.Save(output);
}
{{< /highlight >}}

**PSDNET-1292. 特定のアジアのシンボルを保存した後に Photoshop で書き出したファイルを開く際にエラー**

{{< highlight csharp >}}
string testData = @"尐少尒尓尔尕尖尗尘尙尚尛尜尝尞尟尠尡尢尣尤尥尦尧尨尩尪尫尬尭尮尯尰就尲尳尴尵尶尷尸尹尺尻尼尽尾尿局屁层屃屄居屆屇屈屉届屋屌屍屎屏";

string srcFile = "TestFileForAsianCharsBig 2.psd";
string outFile = "output.psd";

using (var image = (PsdImage)Image.Load(srcFile))
{
    var layer = (TextLayer)image.Layers[0];
    layer.UpdateText(testData);

    image.Save(outFile);
}
{{< /highlight >}}

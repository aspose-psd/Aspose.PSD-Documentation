---
title: Aspose.PSD for .NET 22.4 - リリースノート
type: docs
weight: 90
url: /ja/net/aspose-psd-for-net-22-4-release-notes/
---

{{% alert color="primary" %}}

このページには、[Aspose.PSD for .NET 22.4](https://www.nuget.org/packages/Aspose.PSD/) のリリースノートが含まれています。

{{% /alert %}}

|**キー**|**概要**|**カテゴリ**|
| :- | :- | :- |
|PSDNET-261|Outer Glow レイヤーエフェクトのレンダリング|機能|
|PSDNET-1123|Sha256 ライセンスのサポートを追加|強化|
|PSDNET-1107|複数行テキストの配置が Photoshop の結果と一致しない|バグ|
|PSDNET-1113|テキストリソースデータの解析中に PSD ファイルの読み込みに関する問題|バグ|
|PSDNET-1129|PSD として保存した後のカスタムパターンの位置が不正確|バグ|


## **公開 API 変更**
# **追加された API:**
- T:Aspose.PSD.FileFormats.Psd.JustificationMode
- F:Aspose.PSD.FileFormats.Psd.JustificationMode.Left
- F:Aspose.PSD.FileFormats.Psd.JustificationMode.Right
- F:Aspose.PSD.FileFormats.Psd.JustificationMode.Center
- M:Aspose.PSD.FileFormats.Psd.Layers.LayerEffects.BlendingOptions.AddOuterGlow
- T:Aspose.PSD.FileFormats.Psd.Layers.LayerEffects.OuterGlowEffect
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerEffects.OuterGlowEffect.FillColor
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerEffects.OuterGlowEffect.BlendMode
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerEffects.OuterGlowEffect.IsVisible
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerEffects.OuterGlowEffect.Opacity
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerEffects.OuterGlowEffect.Intensity
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerEffects.OuterGlowEffect.IsAntiAliasing
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerEffects.OuterGlowEffect.Spread
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerEffects.OuterGlowEffect.Size
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerEffects.OuterGlowEffect.Noise
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerEffects.OuterGlowEffect.IsSoftBlend
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerEffects.OuterGlowEffect.Range
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerEffects.OuterGlowEffect.Jitter


# **削除された API:**
- なし


## **使用例:**

**PSDNET-261. Outer Glow レイヤーエフェクトのレンダリング**
{{< highlight csharp >}}
string src = "GreenLayer.psd";
string output = "output261.png";

using (var image = (PsdImage)Image.Load(src))
{
    OuterGlowEffect effect = image.Layers[1].BlendingOptions.AddOuterGlow();
    effect.Range = 10;
    effect.Spread = 10;
    ((IColorFillSettings)effect.FillColor).Color = Color.Red;
    effect.Opacity = 128;
    effect.BlendMode = BlendMode.Normal;

    image.Save(output, new PngOptions());
}
{{< /highlight >}}


**PSDNET-1107. 複数行テキストの配置が Photoshop の結果と一致しない**

{{< highlight csharp >}}
string src = "source1107.psd";
string outputPsd = "output.psd";
string outputPng = "output.png";

using (var image = (PsdImage)Image.Load(src))
{ 
   var txtLayer = image.AddTextLayer("Text line1\rText line2\rText line3", new Rectangle(200, 200, 500, 500));
   var portions = txtLayer.TextData.Items;

   portions[0].Paragraph.Justification = JustificationMode.Left;
   portions[1].Paragraph.Justification = JustificationMode.Right;
   portions[2].Paragraph.Justification = JustificationMode.Center;

   txtLayer.TextData.UpdateLayerData();

   image.Save(outputPsd);
   image.Save(outputPng, new PngOptions());
}
{{< /highlight >}}


**PSDNET-1113. テキストリソースデータの解析中に PSD ファイルの読み込みに関する問題**

{{< highlight csharp >}}
string sourceFile = "input.psd";

using (PsdImage image = (PsdImage) Image.Load(sourceFile))
{
    // 正常に読み込みました。
}
{{< /highlight >}}


**PSDNET-1129. PSD として保存した後のカスタムパターンの位置が不正確**

{{< highlight csharp >}}
string sourceFile = "input_1129.psd";
string outputPsd = "out_psdnet1129.psd";
string outputPng = "out_psdnet1129.png";

using (PsdImage image = (PsdImage) Image.Load(sourceFile))
{
    image.Save(outputPsd);
    image.Save(outputPng, new PngOptions());
}
{{< /highlight >}}

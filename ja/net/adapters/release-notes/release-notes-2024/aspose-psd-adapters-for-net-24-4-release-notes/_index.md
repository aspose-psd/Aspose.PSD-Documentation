---
title: Aspose.PSDアダプター for .NET 24.4 - リリースノート
type: docs
weight: 100
url: /ja/net/adapters/aspose-psd-adapters-for-net-24-4-release-notes/
---

{{% alert color="primary" %}}

このページには、[Aspose.PSDアダプター for .NET 24.4](https://www.nuget.org/packages/Aspose.PSD.Adapters.Imaging/)のリリースノートが含まれています。

{{% /alert %}}

| **キー**     | **概要**                                                          | **カテゴリ** |
|:------------|:-----------------------------------------------------------------|:------------|
| PSDNET-1985 | NugetへのAspose.PSD.Adapters.Imagingの最初の公開              | 拡張 |


## **公開APIの変更**
# **追加されたAPI:**
- なし

# **削除されたAPI:**
- なし

## **使用例:**

[Aspose.PSDアダプターのドキュメントページ](/psd/ja/net/adapters)をご覧ください。

**PSDNET-1985. Aspose.PSDアダプターの使用例の最も完全な例**

{{< highlight csharp >}}
// 初期設定でのアダプターの有効化を追加
Aspose.PSD.Adapters.Imaging.EnableLoaders(
   FileFormat.Bmp,
   FileFormat.Gif,
   FileFormat.Jpeg2000,
   FileFormat.Jpeg,
   FileFormat.Png,
   FileFormat.Svg,
   FileFormat.Tiff,
   FileFormat.Webp);
            
// さらにExporterを有効にする
Aspose.PSD.Adapters.Imaging.EnableExporters();

// アダプターを使用するためには、Aspose.PSDとadapteeのライセンスの両方が必要です
// Aspose.PSDライセンスの適用方法はこちら
var license = new Aspose.PSD.License();
license.SetLicense(@"Aspose.PSD.NET.lic");

// こちらはAspose.ImagingのAdapteeライセンスの適用例
var licImaging = new Aspose.Imaging.License();
licImaging.SetLicense(@"Aspose.Imaging.NET.lic");
// その後、アダプターまたはPSDまたはImagingライブラリの任意のコードを実行できます

// この後、これらのファイルはAspose.PSDで追加のコードなしに開くことができます
using (var img = Aspose.PSD.Image.Load("SomeFile.Webp")) 
{
    // このコードの実行後、WEBPから作成されたPSDファイルを取得し、Aspose.PSDのフィルター、レイヤー、ワープ変換を含む任意のAspose.PSDの調整を適用できます
}

// AdapteeのイメージをPSD形式にエクスポートすることもできます
using (WebPImage webp = new WebPImage(300, 300, null))
{
    // Imaging固有の機能を使用してWEBPファイルを編集します
    var gr = new Aspose.Imaging.Graphics(webp);             
    gr.Clear(Aspose.Imaging.Color.Wheat);

    gr.DrawArc(
        new Aspose.Imaging.Pen(Aspose.Imaging.Color.Black, 5),
        new Aspose.Imaging.Rectangle(50, 50, 200, 200), 
        0, 
        270);

    // その後、ToPsdImage()メソッドを使用してファイルを編集し、Photoshopのような機能、レイヤー、スマートフィルター、スマートオブジェクトを含めたPSDファイルを作成できます
    using (var psdImage = webp.ToPsdImage())
    {                   
        psdImage.AddTextLayer("Some text", new Rectangle(100, 100, 100, 50));
        var hue = psdImage.AddHueSaturationAdjustmentLayer();
        hue.Hue = 130;

        // Aspose.PSDを使用して最終的なPSDファイルを保存します
        psdImage.Save("output.psd");
    }
}

// Adaptersが提供するLoadersやExportersを使用する必要がない場合は、それらを無効にします
Adapters.Imaging.DisableLoaders();
Adapters.Imaging.DisableExporters();		
		
{{< /highlight >}}

---
title: Aspose.PSD for .NET 24.7 - リリースノート
type: docs
weight: 60
url: /ja/net/aspose-psd-for-net-24-7-release-notes/
---

{{% alert color="primary" %}}

このページには、[Aspose.PSD for .NET 24.7](https://www.nuget.org/packages/Aspose.PSD/) のリリースノートが含まれています。

{{% /alert %}}

| **キー**     | **概要**                                                                                   | **カテゴリ** |
|:------------|:-------------------------------------------------------------------------------------------|:-------------|
| PSDNET-1029 | AI ドキュメントを開く際の "Image loading failed." 例外                                   | バグ      |
| PSDNET-2022 | 出力された PDF ファイル内のテキストが不正確にレンダリングされる                             | バグ      |
| PSDNET-2061 | Linux 上で指定されたファイルの画像エクスポートに失敗する ImageSaveException の修正     | バグ      |
| PSDNET-2080 | Aspose.Drawing を使用してフォントを読み込む際の修正                                         | バグ      |
| PSDNET-2085 | 大きな JPEG を使用してスマートオブジェクトレイヤーを作成する際の 'Arithmetic operation resulted in an overflow' の修正 | バグ      |
| PSDNET-2100 | AI ファイルを JPG ファイルに変換できない                                                  | バグ      |

## **パブリック API 変更**
# **追加された API:**
- なし

# **削除された API:**
- なし

## **使用例:**

**PSDNET-1029. AI ドキュメントを開く際の "Image loading failed." 例外**

{{< highlight csharp >}}
string sourceFile = Path.Combine(baseFolder, "[SA]_ID_card_template.ai");
string outputFile = Path.Combine(outputFolder, "[SA]_ID_card_template.png");

using (AiImage image = (AiImage)Image.Load(sourceFile))
{
    image.Save(outputFile, new PngOptions());
}
{{< /highlight >}}

**PSDNET-2022. 出力された PDF ファイル内のテキストが不正確にレンダリングされる**

{{< highlight csharp >}}
string src = Path.Combine(baseFolder, "CVFlor.psd");
string output = Path.Combine(outputFolder, "output.pdf");

using (var psdImage = (PsdImage)Image.Load(src))
{
    PdfOptions saveOptions = new PdfOptions();
    saveOptions.PdfCoreOptions = new PdfCoreOptions();

    psdImage.Save(output, saveOptions);
}
{{< /highlight >}}

**PSDNET-2061. Linux 上で指定されたファイルの画像エクスポートに失敗する ImageSaveException の修正**

{{< highlight csharp >}}
string sourceFile = Path.Combine(baseFolder, "Bed_Roll-Sticker4_1.psd");
string outputFile = Path.Combine(outputFolder, "output.jpg");

using (var psdImage = (PsdImage)Image.Load(sourceFile, new PsdLoadOptions() { LoadEffectsResource = true }))
{
    var saveOptions = new JpegOptions() { Quality = 70 };
    psdImage.Save(outputFile, saveOptions);
}
{{< /highlight >}}

**PSDNET-2080. Aspose.Drawing を使用してフォントを読み込む際の修正**

{{< highlight csharp >}}
using (var installedFonts = new System.Drawing.Text.InstalledFontCollection())
{
    Console.WriteLine("- 更新前。インストールされたフォントの数: " + installedFonts.Families.Length);
    Console.WriteLine("- プラットフォーム: " + Environment.OSVersion.Platform.ToString());
    Console.WriteLine("- 'Arial' の Adobe フォント名を取得してフォントキャッシュをリフレッシュする: "
    FontSettings.GetAdobeFontName("Arial"));

    Console.WriteLine("- 更新後。インストールされたフォントの数: " + installedFonts.Families.Length);

    Assert.Greater(installedFonts.Families.Length, 1);
}
{{< /highlight >}}

**PSDNET-2085. 大きな JPEG を使用してスマートオブジェクトレイヤーを作成する際の 'Arithmetic operation resulted in an overflow' の修正**

{{< highlight csharp >}}
string srcFile = Path.Combine(baseFolder, "source.psd");
string imageJpg = Path.Combine(baseFolder, "test.jpg");

using (var image = (PsdImage)Image.Load(srcFile, new PsdLoadOptions { DataRecoveryMode = DataRecoveryMode.MaximalRecover }))
{
    using (var stream = new FileStream(imageJpg, FileMode.Open))
    {
        var addedLayer = new SmartObjectLayer(stream);
        addedLayer.Name = "Test Layer";
        image.AddLayer(addedLayer);
    }
}
{{< /highlight >}}

**PSDNET-2100. AI ファイルを JPG ファイルに変換できない**

{{< highlight csharp >}}
string sourceFile = Path.Combine(baseFolder, "aaa.ai");
string outputFile = Path.Combine(outputFolder, "aaa.png");

using (AiImage image = (AiImage)Image.Load(sourceFile))
{
    image.Save(outputFile, new PngOptions());
}
{{< /highlight >}} 

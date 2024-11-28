---
title: Aspose.PSD for .NET 24.1 - リリースノート
type: docs
weight: 120
url: /ja/net/aspose-psd-for-net-24-1-release-notes/
---

{{% alert color="primary" %}}

このページには、[Aspose.PSD for .NET 24.1](https://www.nuget.org/packages/Aspose.PSD/) のリリースノートが含まれています。

{{% /alert %}}

| **Key**     | **Summary**                                                                                       | **Category** |
|:------------|:--------------------------------------------------------------------------------------------------|:------------|
| PSDNET-1835 | [AI フォーマット]マルチページ AI 画像の基本的なハンドリングを追加                                      |   機能       |
| PSDNET-718  | ワープテキストエフェクトがテキストに適用されない                                                      |     バグ     |
| PSDNET-1620 | 特定のファイルでマスクのレンダリングが正しくない                                                    |     バグ     |
| PSDNET-1855 | Aspose.PSD.FontParsing.OpenType.Serialization.OpenTypeFontInfo..ctor における NullReferenceException  |     バグ     |
| PSDNET-1883 | [AI フォーマット]AiExporterUtils におけるメモリ使用量の修正                                           |     バグ     |



## **パブリック API 変更**
# **追加された API:**
- P:Aspose.PSD.FileFormats.Ai.AiImage.ActivePageIndex

# **削除された API:**
- なし


## **使用例:**

**PSDNET-718. ワープテキストエフェクトがテキストに適用されない**

{{< highlight csharp >}}
string sourceFile = Path.Combine(baseFolder, "text_warp.psd");
string outputFile = Path.Combine(outputFolder, "export.png");

var opt = new PsdLoadOptions()
{
    LoadEffectsResource = true,
    AllowWarpRepaint = true
};

using (PsdImage img = (PsdImage)Image.Load(sourceFile, opt))
{
    img.Save(outputFile, new PngOptions() { CompressionLevel = 9, ColorType = PngColorType.TruecolorWithAlpha });
}
{{< /highlight >}}

**PSDNET-1620. 特定のファイルでマスクのレンダリングが正しくない**

{{< highlight csharp >}}
string sourceFile1 = Path.Combine(baseFolder, "mask_problem.psd");
string sourceFile2 = Path.Combine(baseFolder, "puh_softLight3_1.psd");
string outputFile1 = Path.Combine(outputFolder, "mask_export.png");
string outputFile2 = Path.Combine(outputFolder, "puh_export.png");

var opt = new PsdLoadOptions()
{
    LoadEffectsResource = true,
};

using (PsdImage img = (PsdImage)Image.Load(sourceFile1, opt))
{
    img.Save(outputFile1, new PngOptions() { CompressionLevel = 9, ColorType = PngColorType.TruecolorWithAlpha }); ;                
}

using (PsdImage img = (PsdImage)Image.Load(sourceFile2, opt))
{
    img.Save(outputFile2, new PngOptions() { CompressionLevel = 9, ColorType = PngColorType.TruecolorWithAlpha }); ;
}
{{< /highlight >}}

**PSDNET-1835. [AI フォーマット]マルチページ AI 画像の基本的なハンドリングを追加**

{{< highlight csharp >}}
string sourceFile = Path.Combine(baseFolder, "threePages.ai");
string firstPageOutputPng = Path.Combine(outputFolder, "firstPageOutput.png");
string secondPageOutputPng = Path.Combine(outputFolder, "secondPageOutput.png");
string thirdPageOutputPng = Path.Combine(outputFolder, "thirdPageOutput.png");

// AI 画像を読み込む
using (AiImage image = (AiImage)Image.Load(sourceFile))
{
    // ActivePageIndex はデフォルトで 0 です。
    // したがって、このプロパティを変更せずに AI 画像を保存すると、最初のページがレンダリングされて保存されます。
    image.Save(firstPageOutputPng, new PngOptions());

    // ActivePageIndex を 1 に変更
    // AI 画像の 2 番目のページを PNG 画像として保存します。
    image.ActivePageIndex = 1;
    image.Save(secondPageOutputPng, new PngOptions());

    // ActivePageIndex を 2 に変更
    // AI 画像の 3 番目のページを PNG 画像として保存します。
    image.ActivePageIndex = 2;
    image.Save(thirdPageOutputPng, new PngOptions());
}
{{< /highlight >}}

**PSDNET-1855. Aspose.PSD.FontParsing.OpenType.Serialization.OpenTypeFontInfo..ctor における NullReferenceException**

{{< highlight csharp >}}
string fontsFolder = Path.Combine(baseFolder, "Fonts");
FontSettings.SetFontsFolders(new string[] { fontsFolder }, true);

string inputFile = Path.Combine(baseFolder, "1.psd");
string outputFile = Path.Combine(outputFolder, "out_1855.png");
using (var psdImage = (PsdImage)Image.Load(inputFile))
{
    psdImage.Save(outputFile, new PngOptions());
}
{{< /highlight >}}

**PSDNET-1883. [AI フォーマット]AiExporterUtils におけるメモリ使用量の修正**

{{< highlight csharp >}}
string sourceFile = Path.Combine(baseFolder, "threePages.ai");
string firstPageOutputPng = Path.Combine(outputFolder, "firstPageOutput.png");
string secondPageOutputPng = Path.Combine(outputFolder, "secondPageOutput.png");
string thirdPageOutputPng = Path.Combine(outputFolder, "thirdPageOutput.png");

const double MemoryLimit = 220;
double memoryUsed = double.MaxValue;

// AI 画像を読み込む
using (AiImage image = (AiImage)Image.Load(sourceFile))
{
    // AI 画像の最初のページを PNG 画像として保存します。
    image.Save(firstPageOutputPng, new PngOptions());

    // ActivePageIndex を 1 に変更
    // AI 画像の 2 番目のページを PNG 画像として保存します。
    image.ActivePageIndex = 1;
    image.Save(secondPageOutputPng, new PngOptions());

    // ActivePageIndex を 2 に変更
    // AI 画像の 3 番目のページを PNG 画像として保存します。
    image.ActivePageIndex = 2;
    image.Save(thirdPageOutputPng, new PngOptions());
}

GC.Collect();

memoryUsed = (GC.GetTotalMemory(false) / 1024.0) / 1024.0;

if (memoryUsed > MemoryLimit)
{
    throw new Exception("メモリ使用量が大きすぎます。" + memoryUsed + " です。" + MemoryLimit.ToString("F1") + " を超えています。");
}
{{< /highlight >}}

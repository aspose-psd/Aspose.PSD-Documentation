---
title: Aspose.PSD for .NET 24.3 - リリースノート
type: docs
weight: 100
url: /ja/net/aspose-psd-for-net-24-3-release-notes/
---

{{% alert color="primary" %}}

このページには、[Aspose.PSD for .NET 24.3](https://www.nuget.org/packages/Aspose.PSD/) のリリースノートが含まれています。

{{% /alert %}}

| **Key**     | **Summary**                                                          | **Category** |
|:------------|:---------------------------------------------------------------------|:------------|
| PSDNET-1914 | [AI フォーマット] 大規模な複数ページの AI 画像の読み込み時間を短縮する         |     改善     |
| PSDNET-1905 | 8 ビットから 16 ビットに変換した PSD ファイルが読めなくなる     |     バグ     |
| PSDNET-1906 | 8 ビットから 32 ビットに変換した PSD ファイルが読めなくなる     |     バグ     |
| PSDNET-1921 | [AI フォーマット] AI ファイルでのショート カーブのレンダリングを修正する    |     バグ     |

## **公開 API 変更**
# **追加された API:**
- なし

# **削除された API:**
- なし

## **使用例:**

**PSDNET-1905. 8 ビットから 16 ビットに変換した PSD ファイルが読めなくなる**

{{< highlight csharp >}}
string sourceFile = Path.Combine(baseFolder, "test_smart_layer.psd");
string outputFile = Path.Combine(outputFolder, "export.psd");

using (var psdImage8 = (PsdImage)Image.Load(sourceFile))
{
    var psdOptions16 = new PsdOptions()
    {
        ChannelBitsCount = 16
    };

    psdImage8.Save(outputFile, psdOptions16);
}

using (var psdImage16 = (PsdImage)Image.Load(outputFile))
{
    if (psdImage16.GlobalLayerResources[0] is Lr16Resource)
    {
        // 正常
    }
    else
    {
        throw new Exception("誤ったグローバル リソース、最初のリソースは Lr16Resource である必要があります");
    }
}
{{< /highlight >}}

**PSDNET-1906. 8 ビットから 32 ビットに変換した PSD ファイルが読めなくなる**

{{< highlight csharp >}}
string sourceFile = Path.Combine(baseFolder, "test_smart_layer.psd");
string outputFile = Path.Combine(outputFolder, "export.psd");

using (var psdImage8 = (PsdImage)Image.Load(sourceFile))
{
    var psdOptions32 = new PsdOptions()
    {
        ChannelBitsCount = 32
    };

    psdImage8.Save(outputFile, psdOptions32);
}

using (var psdImage8 = (PsdImage)Image.Load(outputFile))
{
    if (psdImage8.GlobalLayerResources[0] is Lr32Resource)
    {
        // 正常
    }
    else
    {
        throw new Exception("誤ったグローバル リソース、最初のリソースは Lr32Resource である必要があります");
    }
}
{{< /highlight >}}

**PSDNET-1921. [AI フォーマット] AI ファイルでのショート カーブのレンダリングを修正する**

{{< highlight csharp >}}
string sourceFile = Path.Combine(baseFolder, "shortCurve.ai");
string outputFilePath = Path.Combine(outputFolder, "shortCurve.png");

using (AiImage image = (AiImage)Image.Load(sourceFile))
{
    image.Save(outputFilePath, new PngOptions());
}
{{< /highlight >}}

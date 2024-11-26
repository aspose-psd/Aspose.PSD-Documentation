---
title: Aspose.PSD for Python via .NET 24.3 - リリースノート
type: ドキュメント
weight: 10
url: /ja/net/aspose-psd-for-python-via-net-24-3-release-notes/
---

{{% alert color="primary" %}}

このページには、[Aspose.PSD for Python via .NET 24.3](https://pypi.org/project/aspose-psd/) のリリースノートが含まれています。

{{% /alert %}}

| **キー**      | **概要**                                                          | **カテゴリ**|
|:-------------|:--------------------------------------------------------------------|:------------|
| PSDPYTHON-42 | [AI フォーマット] 大きな複数ページの AI 画像の読み込み時間を短縮       | 機能追加 |
| PSDPYTHON-45 | 8 ビットから 16 ビットに変換した PSD ファイルが読み込めなくなる問題       |     バグ     |
| PSDPYTHON-46 | 8 ビットから 32 ビットに変換した PSD ファイルが読み込めなくなる問題       |     バグ     |
| PSDPYTHON-47 | [AI フォーマット] AI ファイルでのショートカーブのレンダリングを修正       |     バグ     |



## **パブリック API の変更**
# **追加された API:**
- なし

# **削除された API:**
- なし


## **使用例:**

**PSDPYTHON-42. [AI フォーマット] 大きな複数ページの AI 画像の読み込み時間を短縮**

{{< highlight python >}}
   # サンプルなし
{{< /highlight >}}

**PSDPYTHON-45. 8 ビットから 16 ビットに変換した PSD ファイルが読み込めなくなる問題**

{{< highlight python >}}
        sourceFile = "test_smart_layer.psd"
        outputFile = "export.psd"

        with PsdImage.load(sourceFile) as psdImage8:
            psdOptions16 = PsdOptions()
            psdOptions16.channel_bits_count = 16

            psdImage8.save(outputFile, psdOptions16)

        with PsdImage.load(outputFile) as image:
            psdImage16 = cast(PsdImage, image)

            testResource = as_of(psdImage16.global_layer_resources[5], Lr16Resource)
            if testResource is not None:
                # 問題なし
                pass
            else:
                raise Exception("誤ったグローバルリソースです。最初のリソースは Lr16Resource である必要があります。")
{{< /highlight >}}

**PSDPYTHON-46. 8 ビットから 32 ビットに変換した PSD ファイルが読み込めなくなる問題**

{{< highlight python >}}
        sourceFile = "test_smart_layer.psd"
        outputFile = "export.psd"

        with PsdImage.load(sourceFile) as psdImage8:
            psdOptions32 = PsdOptions()
            psdOptions32.channel_bits_count = 32

            psdImage8.save(outputFile, psdOptions32)

        with PsdImage.load(outputFile) as image:
            psdImage32 = cast(PsdImage, image)

            testResource = as_of(psdImage32.global_layer_resources[5], Lr32Resource)
            if testResource is not None:
                # 問題なし
                pass
            else:
                raise Exception("誤ったグローバルリソースです。最初のリソースは Lr32Resource である必要があります。")
{{< /highlight >}}

**PSDPYTHON-47. [AI フォーマット] AI ファイルでのショートカーブのレンダリングを修正**

{{< highlight python >}}
        sourceFile = "shortCurve.ai"
        outputFilePath = "shortCurve.png"

        with AiImage.load(sourceFile) as image:
            image.save(outputFilePath, PngOptions())
{{< /highlight >}}

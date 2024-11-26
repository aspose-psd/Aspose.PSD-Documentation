---
title: Aspose.PSD for Python via .NET 24.7 - リリースノート
type: docs
weight: 10
url: /ja/python-net/aspose-psd-for-python-via-net-24-7-release-notes/
---

{{% alert color="primary" %}}

このページには、[Aspose.PSD for Python via .NET 24.7](https://pypi.org/project/aspose-psd/) のリリースノートが含まれています。

{{% /alert %}}

| **キー**      | **概要**                                                                                                       | **カテゴリ** |
|:-------------|:------------------------------------------------------------------------------------------------------------------|:-------------|
| PSDPYTHON-86 | AI ドキュメントを開く際の "画像の読み込みに失敗しました。" 例外                              | バグ      |
| PSDPYTHON-87 | テキストが出力された PDF ファイルに正しくレンダリングされない                                   | バグ      |
| PSDPYTHON-88 | Linux 上で指定されたファイルの画像エクスポートに失敗する場合の ImageSaveException の修正        | バグ      |
| PSDPYTHON-89 | Aspose.Drawing を使用してフォントの読み込みを修正する                                              | バグ      |
| PSDPYTHON-90 | 大きな JPEG を使用してスマートオブジェクトレイヤーを作成する際の '算術演算でオーバーフローが発生しました。' エラー | バグ      |
| PSDPYTHON-91 | AI ファイルを JPG ファイルに変換できない                                                           | バグ      |

## **パブリック API 変更**
# **追加された API:**
- P:Aspose.PSD.FileFormats.Psd.Layers.FillSettings.NoiseGradientFillSettings.ExpansionCount
- M:Aspose.PSD.FileFormats.Psd.PsdImage.AddGradientMapAdjustmentLayer
- T:Aspose.PSD.FileFormats.Psd.Layers.AdjustmentLayers.GradientMapLayer
- P:Aspose.PSD.FileFormats.Psd.Layers.AdjustmentLayers.GradientMapLayer.GradientSettings
- P:Aspose.PSD.FileFormats.Ai.AiImage.XmpData

# **削除された API:**
- なし

## **使用例**

**PSDPYTHON-86. AI ドキュメントを開く際の "画像の読み込みに失敗しました。" 例外**
{{< highlight python >}}
        sourceFile = self.GetFileInBaseFolder("[SA]_ID_card_template.ai")
        outputFile = self.GetFileInOutputFolder("[SA]_ID_card_template.png")

        with AiImage.load(sourceFile) as image:
            image.save(outputFile, PngOptions())
{{< /highlight >}}

**PSDPYTHON-87. テキストが出力された PDF ファイルに正しくレンダリングされない**
{{< highlight python >}}
        src = self.GetFileInBaseFolder("CVFlor.psd")
        output = self.GetFileInOutputFolder("output.pdf")

        with PsdImage.load(src) as psdImage:
            saveOptions = PdfOptions()
            saveOptions.pdf_core_options = PdfCoreOptions()

            psdImage.save(output, saveOptions)
{{< /highlight >}}


**PSDPYTHON-88. Linux 上で指定されたファイルの画像エクスポートに失敗する場合の ImageSaveException の修正**
{{< highlight python >}}
        sourceFile = self.GetFileInBaseFolder("Bed_Roll-Sticker4_1.psd")
        outputFile = self.GetFileInOutputFolder("output.jpg")

        loadOpt = PsdLoadOptions()
        loadOpt.load_effects_resource = True
        saveOpt = JpegOptions()
        saveOpt.quality = 70
        with PsdImage.load(sourceFile, loadOpt) as psdImage:
            psdImage.save(outputFile, saveOpt)
{{< /highlight >}}


**PSDPYTHON-89. Aspose.Drawing を使用してフォントの読み込みを修正する**
{{< highlight python >}}
        with InstalledFontCollection() as installedFonts:
            print("- 更新前のインストール済みフォント数: " + str(len(installedFonts.families)))
            print("- 'Arial' の Adobe フォント名を取得することによりフォントキャッシュをリフレッシュ: ")
            FontSettings.get_adobe_font_name("Arial")
            print("- 更新後のインストール済みフォント数: " + str(len(installedFonts.families))

            assert len(installedFonts.families) > 1
{{< /highlight >}}


**PSDPYTHON-90. 大きな JPEG を使用してスマートオブジェクトレイヤーを作成する際の '算術演算でオーバーフローが発生しました。' エラー**
{{< highlight python >}}
        # 修正は行われましたが、Aspose.PSD for Python に制限事項があるためこのテストは他の問題があります
        #srcFile = self.GetFileInBaseFolder("source.psd")
        #imageJpg = self.GetFileInBaseFolder("test.jpg")

        #loadOpt = PsdLoadOptions()
        #loadOpt.data_recovery_mode = DataRecoveryMode.MAXIMAL_RECOVER
        #with PsdImage.load(srcFile, loadOpt) as image:
            #with open(imageJpg, "rb", buffering=0) as stream:
                #addedLayer = SmartObjectLayer(stream)
                #addedLayer.Name = "Test Layer"
                #image.AddLayer(addedLayer)
{{< /highlight >}}


**PSDPYTHON-91. AI ファイルを JPG ファイルに変換できない**
{{< highlight python >}}
        sourceFile = self.GetFileInBaseFolder("aaa.ai")
        outputFile = self.GetFileInOutputFolder("aaa.png")

        with AiImage.load(sourceFile) as image:
            image.save(outputFile, PngOptions())
{{< /highlight >}}

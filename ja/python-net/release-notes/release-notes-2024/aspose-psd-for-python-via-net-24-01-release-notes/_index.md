---
title: Aspose.PSD for Python via .NET 24.1 - リリースノート
type: ドキュメント
weight: 10
url: /ja/net/aspose-psd-for-python-via-net-24-1-release-notes/
---

{{% alert color="primary" %}}

このページには、[Aspose.PSD for Python via .NET 24.1](https://pypi.org/project/aspose-psd/) のリリースノートが含まれています。

{{% /alert %}}

| **キー**       | **概要**                                                                             | **カテゴリ** |
|:----------------|:--------------------------------------------------------------------------------------|:------------|
|  PSDPYTHON-19   | [AI フォーマット] 複数ページのAIイメージに対する基本的な処理を追加                    |   機能      |
|  PSDPYTHON-22   | ワープテキストエフェクトがテキストに適用されない                                       |     バグ    |
|  PSDPYTHON-23   | 特定のファイル内のマスクの描画が不正                                                        |     バグ    |
|  PSDPYTHON-24   | Aspose.PSD.FontParsing.OpenType.Serialization.OpenTypeFontInfo..ctor における NullReferenceException |     バグ    |
|  PSDPYTHON-25   | [AI フォーマット] AiExporterUtils におけるメモリ使用量の修正                               |     バグ    |



## **Public API の変更**
# **追加されたAPI:**
- P:Aspose.PSD.FileFormats.Ai.AiImage.ActivePageIndex

# **削除されたAPI:**
- なし


## **使用例:**

**PSDPYTHON-19. [AI フォーマット] 複数ページのAIイメージに対する基本的な処理を追加**

{{< highlight python >}}
        sourceFile = self.GetFileInBaseFolder("threePages.ai")
        firstPageOutputPng = self.GetFileInOutputFolder("firstPageOutput.png")
        secondPageOutputPng = self.GetFileInOutputFolder("secondPageOutput.png")
        thirdPageOutputPng = self.GetFileInOutputFolder("thirdPageOutput.png")

        # AI イメージをロードします。
        with Image.load(sourceFile) as img:
            image = cast(AiImage, img)
            # デフォルトでは、ActivePageIndex は 0 です。
            # このプロパティを変更せずに AI イメージを保存すると、最初のページがレンダリングされて保存されます。
            image.save(firstPageOutputPng, PngOptions())

            # ActivePageIndex を 1 に変更します。
            image.active_page_index = 1

            # AI イメージの2番目のページを PNG イメージとして保存します。
            image.save(secondPageOutputPng, PngOptions())

            # ActivePageIndex を 2 に変更します。
            image.active_page_index = 2

            # AI イメージの3番目のページを PNG イメージとして保存します。
            image.save(thirdPageOutputPng, PngOptions())
{{< /highlight >}}

**PSDPYTHON-22. ワープテキストエフェクトがテキストに適用されない**

{{< highlight python >}}
        sourceFile = self.GetFileInBaseFolder("text_warp.psd")
        outputFile = self.GetFileInOutputFolder("export.png")

        opt = PsdLoadOptions()
        opt.load_effects_resource = True
        opt.allow_warp_repaint = True

        pngOpt = PngOptions()
        pngOpt.compression_level = 9
        pngOpt.color_type = PngColorType.TRUECOLOR_WITH_ALPHA

        with PsdImage.load(sourceFile, opt) as img:
            img.save(outputFile, pngOpt)
{{< /highlight >}}

**PSDPYTHON-23. 特定のファイル内のマスクの描画が不正**

{{< highlight python >}}
        sourceFile1 = self.GetFileInBaseFolder("mask_problem.psd")
        sourceFile2 = self.GetFileInBaseFolder("puh_softLight3_1.psd")
        outputFile1 = self.GetFileInOutputFolder("mask_export.png")
        outputFile2 = self.GetFileInOutputFolder("puh_export.png")

        opt = PsdLoadOptions()
        opt.load_effects_resource = True

        pngOpt = PngOptions()
        pngOpt.compression_level = 9
        pngOpt.color_type = PngColorType.TRUECOLOR_WITH_ALPHA

        with PsdImage.load(sourceFile1, opt) as img:
            img.save(outputFile1, pngOpt)

        with PsdImage.load(sourceFile2, opt) as img:
            img.save(outputFile2, pngOpt)
{{< /highlight >}}

**PSDPYTHON-24. Aspose.PSD.FontParsing.OpenType.Serialization.OpenTypeFontInfo..ctor における NullReferenceException**

{{< highlight python >}}
        fontsFolder = self.GetFileInBaseFolder("Fonts")
        FontSettings.set_fonts_folders([fontsFolder], True)


        inputFile = self.GetFileInBaseFolder("1.psd")
        outputFile = self.GetFileInOutputFolder("out_1855.png")
        referenceFile = self.GetFileInBaseFolder("out_1855.png")

        with PsdImage.load(inputFile) as psdImage:
            psdImage.save(outputFile, PngOptions())
{{< /highlight >}}

**PSDPYTHON-25. [AI フォーマット] AiExporterUtils におけるメモリ使用量の修正**

{{< highlight python >}}
sourceFile = self.GetFileInBaseFolder("threePages.ai")
        firstPageOutputPng = self.GetFileInOutputFolder("firstPageOutput.png")
        secondPageOutputPng = self.GetFileInOutputFolder("secondPageOutput.png")
        thirdPageOutputPng = self.GetFileInOutputFolder("thirdPageOutput.png")

        # C# のメモリ使用量は 220 ですが、Python では GC のアクティビティには直接アクセスできません。
        MemoryLimit = 1500
        process = psutil.Process()
        startMemory = process.memory_info().rss
        pngOpt = PngOptions()
        # AI イメージをロードします。
        with Image.load(sourceFile) as img:
            image = cast(AiImage, img)

            # AI イメージの最初のページを PNG イメージとして保存します。
            image.save(firstPageOutputPng, pngOpt)

            # ActivePageIndex を 1 に変更します。
            image.active_page_index = 1

            # AI イメージの2番目のページを PNG イメージとして保存します。
            image.save(secondPageOutputPng, pngOpt)

            # ActivePageIndex を 2 に変更します。
            image.active_page_index = 2

            # AI イメージの3番目のページを PNG イメージとして保存します。
            image.save(thirdPageOutputPng, pngOpt)

        endMemory = process.memory_info().rss

        memoryUsed = (endMemory - startMemory) / 1024 / 1024

        if memoryUsed > MemoryLimit:
            raise Exception("メモリの使用量が大きすぎます。 {:.1f} の代わりに {}".format(memoryUsed, MemoryLimit))
{{< /highlight >}}


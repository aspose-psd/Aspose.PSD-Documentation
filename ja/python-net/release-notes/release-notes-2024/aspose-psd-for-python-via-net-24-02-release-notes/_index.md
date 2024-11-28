---
title: Aspose.PSD for Python via .NET 24.2 - リリースノート
type: docs
weight: 10
url: /ja/net/aspose-psd-for-python-via-net-24-2-release-notes/
---

{{% alert color="primary" %}}

このページには、[Aspose.PSD for Python via .NET 24.2](https://pypi.org/project/aspose-psd/)のリリースノートが含まれています。

{{% /alert %}}

| **Key**     | **Summary**                                                                  | **Category** |
|:-------------|:-----------------------------------------------------------------------------|:------------|
| PSDPYTHON-28 | PatternFillSettingsのAngleプロパティを処理する                                |   機能       |
| PSDPYTHON-29 | TextLayerの垂直および水平スケールのサポート                                 |   機能       |
| PSDPYTHON-33 | [AIフォーマット] PDFベースのAIフォーマットの背景の正しいレンダリングを実装する |   機能       |
| PSDPYTHON-34 | Distortメカニズムを変更する                                                | 拡張機能     |
| PSDPYTHON-35 | ワープを高速化する                                                          | 拡張機能     |
| PSDPYTHON-36 | ドキュメントを開く際に "画像の読み込みに失敗しました。"の例外                   |     バグ    |
| PSDPYTHON-37 | ストロークパターンを持つpsdファイルを保存する問題を修正                        |     バグ    |
| PSDPYTHON-38 | ReplaceContentsを使用したスマートオブジェクトのテキストスタイルが正しくない       |     バグ    |
| PSDPYTHON-39 | [AIフォーマット] AIファイルでのCubic Bezierのレンダリングを修正                   |     バグ    |



## **公開APIの変更**
# **追加されたAPI:**
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.PtFlResource.Angle

# **削除されたAPI:**
- なし


## **使用例:**

## **使用例:**

**PSDPYTHON-28. PatternFillSettingsのAngleプロパティを処理する**

{{< highlight python >}}

	    fileName = "PatternFillLayerWide_0"
        sourceFile = fileName + ".psd"
        outputFile = fileName + "_output.psd"

        loadOpt = PsdLoadOptions()
        loadOpt.load_effects_resource = True
        with PsdImage.load(sourceFile, loadOpt) as img:
            image = cast(PsdImage, img)
            fillLayer = cast(FillLayer, image.layers[1])
            fillSettings = fillLayer.fill_settings
            fillSettings.angle = 70
            fillLayer.update()
            image.save(outputFile, PsdOptions())

        with PsdImage.load(outputFile, loadOpt) as img:
            image = cast(PsdImage, img)
            fillLayer = cast(FillLayer, image.layers[1])
            fillSettings = fillLayer.fill_settings

            assert fillSettings.angle == 70

{{< /highlight >}}

**PSDPYTHON-29. TextLayerの垂直および水平スケールのサポート**

{{< highlight python >}}

           sourceFile = "1719_src.psd"
           outputFile = "output.png"

           # いくつかのフォントを追加
           fontsFolder = "1719_Fonts"
           fontFolders = list(FontSettings.get_fonts_folders())
           fontFolders.append(fontsFolder)
           FontSettings.set_fonts_folders(fontFolders, True)

           with PsdImage.load(sourceFile) as image:
               image.save(outputFile, PngOptions())

{{< /highlight >}}

**PSDPYTHON-33. [AIフォーマット] PDFベースのAIフォーマットの背景を正しくレンダリングする**

{{< highlight python >}}

           sourceFile = "pineapples.ai"
           outputFile  = "pineapples.png"

           with AiImage.load(sourceFile) as image:
               image.save(outputFile, PngOptions())

{{< /highlight >}}

**PSDPYTHON-34. Distortメカニズムを変更する**

{{< highlight python >}}

        sourceFile = "crow_grid.psd"       
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

**PSDPYTHON-35. ワープを高速化する**

{{< highlight python >}}

        sourceFile = "output.psd"
        outputFile = "export.png"

        opt = PsdLoadOptions()
        opt.load_effects_resource = True
        opt.allow_warp_repaint = True

        start_time = time.time()

        pngOpt = PngOptions()
        pngOpt.compression_level = 9
        pngOpt.color_type = PngColorType.TRUECOLOR_WITH_ALPHA

        with PsdImage.load(sourceFile, opt) as img:
            img.save(outputFile, pngOpt)

        elapsed_time = time.time() - start_time

        # 古い値 = 193300
        # 新しい値 =  55500
        time_in_sec = int(elapsed_time * 1000)
        if time_in_sec > 100000:
            raise Exception("プロセス時間が長すぎます")

{{< /highlight >}}

**PSDPYTHON-36. ドキュメントを開く際に "画像の読み込みに失敗しました。"の例外**

{{< highlight python >}}
        sourceFile1 = "PRODUCT.ai"
        outputFile1 = "PRODUCT.png"

        with AiImage.load(sourceFile1) as image:
            image.save(outputFile1, PngOptions())

        sourceFile2 = "Dolota.ai"
        outputFile2 = "Dolota.png"

        with AiImage.load(sourceFile2) as image:
            image.save(outputFile2, PngOptions())       

        sourceFile3 = "ARS_novelty_2108_out_01(1).ai"
        outputFile3 = "ARS_novelty_2108_out_01(1).png"

        with AiImage.load(sourceFile3) as image:
            image.save(outputFile3, PngOptions())

        sourceFile4 = "bit_gear.ai"      
        outputFile4 = "bit_gear.png"

        with AiImage.load(sourceFile4) as image:
            image.save(outputFile4, PngOptions())

        sourceFile5 = "test.ai"
        outputFile5 = "test.png"

        with AiImage.load(sourceFile5) as image:
            image.save(outputFile5, PngOptions())
{{< /highlight >}}

**PSDPYTHON-37. ストロークパターンを持つpsdファイルを保存する問題を修正**

{{< highlight python >}}
        sourceFile = "StrokeShapePattern.psd"
        outputFile = "StrokeShapePattern_output.psd"

        newPatternBounds = Rectangle(0, 0, 4, 4)
        guid = str(uuid.uuid4())
        newPatternName = "$$$/Presets/Patterns/HorizontalLine1=Horizontal Line 9\0"
        newPattern = [
            Color.aqua.to_argb(), Color.red.to_argb(), Color.red.to_argb(), Color.aqua.to_argb(),
            Color.aqua.to_argb(), Color.white.to_argb(), Color.white.to_argb(), Color.aqua.to_argb(),
            Color.aqua.to_argb(), Color.white.to_argb(), Color.white.to_argb(), Color.aqua.to_argb(),
            Color.aqua.to_argb(), Color.red.to_argb(), Color.red.to_argb(), Color.aqua.to_argb(),
        ]

        with PsdImage.load(sourceFile) as img:
            image = cast(PsdImage, img)
            shapeLayer = cast(ShapeLayer, image.layers[1])
            strokeInternalFillSettings = shapeLayer.fill

            pattResource = None
            for globalLayerResource in image.global_layer_resources:
                pattResource = as_of(globalLayerResource, PattResource)
                if pattResource is not None:
                    patternItem = pattResource.patterns[0]  # ストローク内部のパターンデータ

                    patternItem.pattern_id = guid
                    patternItem.name = newPatternName
                    patternItem.set_pattern(newPattern, newPatternBounds)
                    break

            strokeInternalFillSettings.pattern_name = newPatternName
            strokeInternalFillSettings.pattern_id = guid + "\0"

            shapeLayer.update()

            image.save(outputFile)

        # 変更されたデータをチェックする。
        with PsdImage.load(outputFile) as img:
            image = cast(PsdImage, img)
            shapeLayer = cast(ShapeLayer, image.layers[1])
            strokeInternalFillSettings = shapeLayer.fill

            assert guid.upper() == strokeInternalFillSettings.pattern_id
            assert newPatternName == strokeInternalFillSettings.pattern_name + "\0"
{{< /highlight >}}

**PSDPYTHON-38. ReplaceContentsを使用したスマートオブジェクトのテキストスタイルが正しくない**

{{< highlight python >}}
        inputFile = "source.psd"
        output2 = "output.png"

        psdLoadOptions = PsdLoadOptions()
        psdLoadOptions.load_effects_resource = True

        with PsdImage.load(inputFile, psdLoadOptions) as image:
            psdImage = cast(PsdImage, image)
            smartObject = cast(SmartObjectLayer, psdImage.layers[1])

            smartObjectImage = cast(PsdImage, smartObject.load_contents(psdLoadOptions))

            with smartObjectImage:
                smartObject.replace_contents(smartObjectImage)

            pngOpt = PngOptions()
            pngOpt.color_type = PngColorType.TRUECOLOR_WITH_ALPHA
            psdImage.save(output2, pngOpt)

{{< /highlight >}}

**PSDPYTHON-39. [AIフォーマット] AIファイルでのCubic Bezierのレンダリングを修正**

{{< highlight python >}}

        sourceFile = "Typography.ai"
        outputFilePath = "Typography.png"

        with AiImage.load(sourceFile) as image:
            image.save(outputFilePath, PngOptions())

{{< /highlight >}}

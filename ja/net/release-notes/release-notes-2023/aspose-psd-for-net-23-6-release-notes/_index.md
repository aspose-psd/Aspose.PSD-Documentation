---
title: Aspose.PSD for .NET 23.6 - リリースノート
type: docs
weight: 70
url: /ja/net/aspose-psd-for-net-23-6-release-notes/
---

{{% alert color="primary" %}}

このページには、[Aspose.PSD for .NET 23.6](https://www.nuget.org/packages/Aspose.PSD/) のリリースノートが含まれています。

{{% /alert %}}

| **キー**   | **概要**                                                                                                                      | **カテゴリ** |
|:-----------|:-----------------------------------------------------------------------------------------------------------------------------|:-------------|
| PSDNET-1401 | TimeLine API のリファクタ                                                                                                      | 機能強化     |
| PSDNET-1517 | ワープのレンダリング時のアーティファクトを削除                                                                                  | 機能強化     |
| PSDNET-1528 | ワープのレンダリング最適化                                                                                                      | 機能強化     |
| PSDNET-147  | 閾値調整レイヤーのサポート                                                                                                     | 機能         |
| PSDNET-149  | 選択色調整レイヤーのサポート                                                                                                   | 機能         |
| PSDNET-801  | PSD TimeLine をアニメーション GIF ファイルにエクスポートする機能                                                                | 機能         |
| PSDNET-1555 | 四角形ボーダーのない TextLayer のサポート                                                                                        | 機能         |
| PSDNET-1582 | ShapeLayer のサポート                                                                                                          | 機能         |
| PSDNET-864  | スマートオブジェクト内の画像の置き換えが更新されない                                                                             | バグ         |
| PSDNET-1404 | PSD ファイルを PSD として保存できない：Rgb および Lab モードは、3 チャネル未満および 4 チャネルを超えることはできないという例外  | バグ         |
| PSDNET-1546 | Photoshop の編集モードで TextLayer を開いた場合にテキストの整列が失われる                                                           | バグ         |
| PSDNET-1548 | PSD ファイルを保存する際の Null 参照例外                                                                                    | バグ         |
| PSDNET-1578 | ShapeLayer の読み込み時の例外：ベクトル原点の境界のポイントはまだサポートされていません                                           | バグ         |
| PSDNET-1579 | VogkResource の読み込み時の例外：ポイントが DoubleStructures として保存されていますが、UnitStructures として読み取られています       | バグ         |
| PSDNET-1581 | ShapeLayer のレイヤータイプが空です                                                                                           | バグ         |


## **パブリック API の変更**
# **追加された API:**
- Aspose.PSD.FileFormats.Psd.Layers.Animation.Frame.#ctor
- M:Aspose.PSD.FileFormats.Psd.Layers.Animation.LayerState.#ctor
- T:Aspose.PSD.FileFormats.Psd.Layers.Animation.Timeline
- M:Aspose.PSD.FileFormats.Psd.Layers.Animation.Timeline.#ctor
- P:Aspose.PSD.FileFormats.Psd.Layers.Animation.Timeline.AFSt
- P:Aspose.PSD.FileFormats.Psd.Layers.Animation.Timeline.FsID
- P:Aspose.PSD.FileFormats.Psd.Layers.Animation.Timeline.ActiveFrameIndex
- P:Aspose.PSD.FileFormats.Psd.Layers.Animation.Timeline.Frames
- P:Aspose.PSD.FileFormats.Psd.Layers.Animation.Timeline.LoopesCount
- M:Aspose.PSD.FileFormats.Psd.Layers.Animation.Timeline.Save(System.String,Aspose.PSD.ImageOptionsBase)
- M:Aspose.PSD.FileFormats.Psd.Layers.Animation.Timeline.Save(System.IO.Stream,Aspose.PSD.ImageOptionsBase)
- M:Aspose.PSD.FileFormats.Psd.Layers.Animation.Timeline.SwitchActiveFrame(System.Int32)
- P:Aspose.PSD.FileFormats.Psd.PsdImage.Timeline
- P:Aspose.PSD.FileFormats.Core.VectorPaths.VectorShapeBoundingBox.PointsUnitType
- T:Aspose.PSD.FileFormats.Psd.Layers.AdjustmentLayers.CmykCorrection
- M:Aspose.PSD.FileFormats.Psd.Layers.AdjustmentLayers.CmykCorrection.#ctor
- P:Aspose.PSD.FileFormats.Psd.Layers.AdjustmentLayers.CmykCorrection.Cyan
- P:Aspose.PSD.FileFormats.Psd.Layers.AdjustmentLayers.CmykCorrection.Magenta
- P:Aspose.PSD.FileFormats.Psd.Layers.AdjustmentLayers.CmykCorrection.Yellow
- P:Aspose.PSD.FileFormats.Psd.Layers.AdjustmentLayers.CmykCorrection.Black
- T:Aspose.PSD.FileFormats.Psd.Layers.AdjustmentLayers.CorrectionMethodTypes
- F:Aspose.PSD.FileFormats.Psd.Layers.AdjustmentLayers.CorrectionMethodTypes.Relative
- F:Aspose.PSD.FileFormats.Psd.Layers.AdjustmentLayers.CorrectionMethodTypes.Absolute
- T:Aspose.PSD.FileFormats.Psd.Layers.AdjustmentLayers.SelectiveColorsTypes
- F:Aspose.PSD.FileFormats.Psd.Layers.AdjustmentLayers.SelectiveColorsTypes.Reds
- F:Aspose.PSD.FileFormats.Psd.Layers.AdjustmentLayers.SelectiveColorsTypes.Yellows
- F:Aspose.PSD.FileFormats.Psd.Layers.AdjustmentLayers.SelectiveColorsTypes.Greens
- F:Aspose.PSD.FileFormats.Psd.Layers.AdjustmentLayers.SelectiveColorsTypes.Cyans
- F:Aspose.PSD.FileFormats.Psd.Layers.AdjustmentLayers.SelectiveColorsTypes.Blues
- F:Aspose.PSD.FileFormats.Psd.Layers.AdjustmentLayers.SelectiveColorsTypes.Magentas
- F:Aspose.PSD.FileFormats.Psd.Layers.AdjustmentLayers.SelectiveColorsTypes.Whites
- F:Aspose.PSD.FileFormats.Psd.Layers.AdjustmentLayers.SelectiveColorsTypes.Neutrals
- F:Aspose.PSD.FileFormats.Psd.Layers.AdjustmentLayers.SelectiveColorsTypes.Blacks
- T:Aspose.PSD.FileFormats.Psd.Layers.AdjustmentLayers.SelectiveColorLayer
- P:Aspose.PSD.FileFormats.Psd.Layers.AdjustmentLayers.SelectiveColorLayer.Version
- P:Aspose.PSD.FileFormats.Psd.Layers.AdjustmentLayers.SelectiveColorLayer.CorrectionMethod
- M:Aspose.PSD.FileFormats.Psd.Layers.AdjustmentLayers.SelectiveColorLayer.GetCmykCorrection(Aspose.PSD.FileFormats.Psd.Layers.AdjustmentLayers.SelectiveColorsTypes)
- M:Aspose.PSD.FileFormats.Psd.Layers.AdjustmentLayers.SelectiveColorLayer.SetCmykCorrection(Aspose.PSD.FileFormats.Psd.Layers.AdjustmentLayers.SelectiveColorsTypes,Aspose.PSD.FileFormats.Psd.Layers.AdjustmentLayers.CmykCorrection)
- M:Aspose.PSD.FileFormats.Psd.PsdImage.AddSelectiveColorAdjustmentLayer
- T:Aspose.PSD.FileFormats.Psd.Layers.AdjustmentLayers.ThresholdLayer
- P:Aspose.PSD.FileFormats.Psd.Layers.AdjustmentLayers.ThresholdLayer.Level
- M:Aspose.PSD.FileFormats.Psd.PsdImage.AddThresholdAdjustmentLayer
- T:Aspose.PSD.FileFormats.Psd.Layers.ShapeLayer
- M:Aspose.PSD.FileFormats.Psd.Layers.ShapeLayer.#ctor
- M:Aspose.PSD.FileFormats.Psd.Layers.ShapeLayer.CreateInstance
- M:Aspose.PSD.FileFormats.Psd.Layers.ShapeLayer.Update
- P:Aspose.PSD.FileFormats.Psd.Layers.ShapeLayer.Path


# **削除された API:**
- M:Aspose.PSD.FileFormats.Psd.Layers.Animation.Frame.#ctor(Aspose.PSD.FileFormats.Psd.Layers.Animation.TimeLine)
- M:Aspose.PSD.FileFormats.Psd.Layers.Animation.LayerState.#ctor(System.Int32)
- T:Aspose.PSD.FileFormats.Psd.Layers.Animation.TimeLine
- M:Aspose.PSD.FileFormats.Psd.Layers.Animation.TimeLine.#ctor
- P:Aspose.PSD.FileFormats.Psd.Layers.Animation.TimeLine.AFSt
- P:Aspose.PSD.FileFormats.Psd.Layers.Animation.TimeLine.FsID
- P:Aspose.PSD.FileFormats.Psd.Layers.Animation.TimeLine.ActiveFrame
- P:Aspose.PSD.FileFormats.Psd.Layers.Animation.TimeLine.LoopesCount
- P:Aspose.PSD.FileFormats.Psd.Layers.Animation.TimeLine.Frames
- P:Aspose.PSD.FileFormats.Psd.Layers.Animation.TimeLine.LayerIds
- M:Aspose.PSD.FileFormats.Psd.Layers.Animation.TimeLine.InitializeFrom(Aspose.PSD.FileFormats.Psd.PsdImage)
- M:Aspose.PSD.FileFormats.Psd.Layers.Animation.TimeLine.ApplyTo(Aspose.PSD.FileFormats.Psd.PsdImage)


## **使用例:**

**PSDNET-147.  Threshold Adjustment Layer のサポート**

{{< highlight csharp >}}
string sourceFileWithThresholdLayer = "flowers_threshold_source.psd";
string outputPsdWithThresholdLayer = "flowers_threshold_output.psd";
string outputPngWithThresholdLayer = "flowers_threshold_output.png";

string sourceFileWithoutThresholdLayer = "flowers_source.psd";
string outputPsdWithoutThresholdLayer = "flowers_output.psd";
string outputPngWithoutThresholdLayer = "flowers_output.png";

void AssertAreEqual(object expected, object actual)
{
    if (!object.Equals(expected, actual))
    {
        throw new Exception("Objects are not equal.");
    }
}

// 画像から Threshold 調整レイヤーを取得、チェック、変更
using (var image = (PsdImage)Image.Load(sourceFileWithThresholdLayer))
{
    foreach (var layer in image.Layers)
    {
        if (layer is ThresholdLayer)
        {
            // Threshold 調整レイヤー取得
            ThresholdLayer thrsLayer = (ThresholdLayer)layer;
            var level = thrsLayer.Level;

            // レイヤーのパラメータをチェック
            AssertAreEqual(level, (short)115);

            // レイヤーのパラメータを設定
            thrsLayer.Level = 50;

            image.Save(outputPsdWithThresholdLayer);
            image.Save(outputPngWithThresholdLayer, new PngOptions());
        }
    }
}

// 画像に Threshold 調整レイヤーを追加、設定
using (var image = (PsdImage)Image.Load(sourceFileWithoutThresholdLayer))
{
    // Threshold 調整レイヤーを追加
    ThresholdLayer thresholdLayer = image.AddThresholdAdjustmentLayer();

    // レイヤーのパラメータを設定
    thresholdLayer.Level = 115;

    image.Save(outputPsdWithoutThresholdLayer);
    image.Save(outputPngWithoutThresholdLayer, new PngOptions());
}
{{< /highlight >}}

**PSDNET-149.  Selective Color Adjustment Layer のサポート**

{{< highlight csharp >}}
string sourceFileWithSelectiveColorLayer = "houses_selectiveColor_source.psd";
string outputPsdWithSelectiveColorLayer = "houses_selectiveColor_output.psd";
string outputPngWithSelectiveColorLayer = "houses_selectiveColor_output.png";

string sourceFileWithoutSelectiveColorLayer = "houses_source.psd";
string outputPsdWithoutSelectiveColorLayer = "houses_output.psd";
string outputPngWithoutSelectiveColorLayer = "houses_output.png";

void AssertAreEqual(object expected, object actual)
{
    if (!object.Equals(expected, actual))
    {
        throw new Exception("Objects are not equal.");
    }
}

// 画像から Selective Color 調整レイヤーを取得、チェック、変更
using (var image = (PsdImage)Image.Load(sourceFileWithSelectiveColorLayer))
{
    foreach (var layer in image.Layers)
    {
        if (layer is SelectiveColorLayer)
        {
            // Selective Color 調整レイヤー取得
            SelectiveColorLayer selcLayer = (SelectiveColorLayer)layer;
            var redCorrection = selcLayer.GetCmykCorrection(SelectiveColorsTypes.Reds);
            var yellowCorrection = selcLayer.GetCmykCorrection(SelectiveColorsTypes.Yellows);
            var greenCorrection = selcLayer.GetCmykCorrection(SelectiveColorsTypes.Greens);
            var blueCorrection = selcLayer.GetCmykCorrection(SelectiveColorsTypes.Blues);

            // レイヤーのパラメータをチェック
            AssertAreEqual(CorrectionMethodTypes.Absolute, selcLayer.CorrectionMethod);

            AssertAreEqual(redCorrection.Cyan, (short)-31);
            AssertAreEqual(redCorrection.Magenta, (short)-12);
            AssertAreEqual(redCorrection.Yellow, (short)27);
            AssertAreEqual(redCorrection.Black, (short)33);

            AssertAreEqual(yellowCorrection.Cyan, (short)-22);
            AssertAreEqual(yellowCorrection.Magenta, (short)-19);
            AssertAreEqual(yellowCorrection.Yellow, (short)8);
            AssertAreEqual(yellowCorrection.Black, (short)0);

            AssertAreEqual(greenCorrection.Cyan, (short)0);
            AssertAreEqual(greenCorrection.Magenta, (short)0);
            AssertAreEqual(greenCorrection.Yellow, (short)0);
            AssertAreEqual(greenCorrection.Black, (short)0);

            AssertAreEqual(blueCorrection.Cyan, (short)58);
            AssertAreEqual(blueCorrection.Magenta, (short)18);
            AssertAreEqual(blueCorrection.Yellow, (short)1);
            AssertAreEqual(blueCorrection.Black, (short)7);

            // レイヤーのパラメータを変更
            selcLayer.CorrectionMethod = CorrectionMethodTypes.Relative;
            selcLayer.SetCmykCorrection(SelectiveColorsTypes.Reds, new CmykCorrection { Cyan = 12, Magenta = -20, Yellow = 10, Black = -15 });
            selcLayer.SetCmykCorrection(SelectiveColorsTypes.Whites, new CmykCorrection { Cyan = 15, Magenta = 20, Yellow = -75, Black = 42 });

            image.Save(outputPsdWithSelectiveColorLayer);
            image.Save(outputPngWithSelectiveColorLayer, new PngOptions());
        }
    }
}

// 画像に Selective Color 調整レイヤーを追加、設定
using (var image = (PsdImage)Image.Load(sourceFileWithoutSelectiveColorLayer))
{
    // Selective Color 調整レイヤーを追加
    SelectiveColorLayer selectiveColorLayer = image.AddSelectiveColorAdjustmentLayer();

    // レイヤーのパラメータを設定
    selectiveColorLayer.CorrectionMethod = CorrectionMethodTypes.Absolute;
    selectiveColorLayer.SetCmykCorrection(SelectiveColorsTypes.Whites, new CmykCorrection { Cyan = 100, Magenta = -100, Yellow = 100, Black = 0 });
    selectiveColorLayer.SetCmykCorrection(SelectiveColorsTypes.Blacks, new CmykCorrection { Cyan = 10, Magenta = 15, Yellow = 17, Black = -3 });
    selectiveColorLayer.SetCmykCorrection(SelectiveColorsTypes.Neutrals, new CmykCorrection { Cyan = 45, Magenta = 21, Yellow = -14, Black = 0 });
    selectiveColorLayer.SetCmykCorrection(SelectiveColorsTypes.Magentas, new CmykCorrection { Cyan = 8, Magenta = -10, Yellow = -14, Black = 25 });

    image.Save(outputPsdWithoutSelectiveColorLayer);
    image.Save(outputPngWithoutSelectiveColorLayer, new PngOptions());
}
{{< /highlight >}}

**PSDNET-801.  PSD TimeLine をアニメーション GIF ファイルにエクスポートする機能**

{{< highlight csharp >}}
string sourceFile = "4_animated.psd";
string outputGif = "out_4_animated.psd.gif";

using (var psdImage = (PsdImage)Image.Load(sourceFile, new PsdLoadOptions() { LoadEffectsResource = true }))
{
    psdImage.Timeline.Save(outputGif, new GifOptions());
}
{{< /highlight >}}

**PSDNET-864.  スマートオブジェクト内の画像の置き換えが更新されない**

{{< highlight csharp >}}
string sourceFile = "neiyi.psd";
string changeFile = "bg6.png";

string exportFile = "export.psd";
string exportImgBefore = "export_before.png";
string exportImgAfter = "export_after.png";

using (var psdImage = (PsdImage)Image.Load(sourceFile))
{
    foreach (Layer layer in psdImage.Layers)
    {
        if (layer is SmartObjectLayer && layer.Name == "sucai1")
        {
            SmartObjectLayer smartObjectLayer = (SmartObjectLayer)layer;
            smartObjectLayer.ReplaceContents(changeFile);
            smartObjectLayer.EmbedLinked();

            break;                                                
        }
    }

    psdImage.Save(exportFile, new PsdOptions());
    psdImage.Save(exportImgBefore, new PngOptions());
}

using (var psdImage = (PsdImage)Image.Load(exportFile))
{
    psdImage.Save(exportImgAfter, new PngOptions());
}
{{< /highlight >}}

**PSDNET-1401.  TimeLine API のリファクタ**

{{< highlight csharp >}}
string sourceFile = "4_animated.psd";
string outputFile = "
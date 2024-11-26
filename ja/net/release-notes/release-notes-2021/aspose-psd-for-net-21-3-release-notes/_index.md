---
title: Aspose.PSD for .NET 21.3 - リリースノート
type: docs
weight: 100
url: /ja/net/aspose-psd-for-net-21-3-release-notes/
---

{{% alert color="primary" %}} 

このページには、[Aspose.PSD for .NET 21.3](https://www.nuget.org/packages/Aspose.PSD/) のリリースノートが含まれています。

{{% /alert %}} 

|**キー**|**概要**|**カテゴリ**|
| :- | :- | :- |
|PSDNET-823|レイヤーグループのエクスペリエンスを向上させるためのSectionDividerLayerを追加|機能の追加|
|PSDNET-694|PattResourceを読み取る際、幅と高さが入れ替わっていました|バグ|
|PSDNET-789|2つ以上のレイヤーエフェクトのブレンドが正しくない|バグ|
|PSDNET-805|2つ以上のレイヤーエフェクトが存在する場合のブレンド順序とロジックが正しくない|バグ|
|PSDNET-842|ストロークエフェクトのプロパティがPSDファイルに保存されていない|バグ|

## **Public API変更**
# **追加されたAPI:**
- T:Aspose.PSD.FileFormats.Psd.Layers.SectionDividerLayer
- M:Aspose.PSD.FileFormats.Psd.Layers.SectionDividerLayer.GetRelatedLayerGroup
- P:Aspose.PSD.FileFormats.Psd.Layers.SectionDividerLayer.IsVisibleInGroup

# **削除されたAPI:**
- なし

## **使用例**

**PSDNET-694. PattResourceを読み取る際、幅と高さが入れ替わっていました**

{{< highlight csharp >}}
            string sourceFile = "Untitled-1.psd";
            string outputFile = "output.png";

            using (var image = (PsdImage)Image.Load(sourceFile))
            {
                var fillLayer = (FillLayer)image.Layers[1];
                fillLayer.Update(); // パターンレンダリングを実行

                image.Save(outputFile, new PngOptions());
            }
{{< /highlight >}}

**PSDNET-789. 2つ以上のレイヤーエフェクトのブレンドが正しくない**

{{< highlight csharp >}}
            string srcFile = "source_789.psd";
            string outputSmartObjectPath = "output789.png";
            string outputFile = "output789.psd";

            using (PsdImage image = (PsdImage)Image.Load(srcFile, new PsdLoadOptions() { LoadEffectsResource = true }))
            {
                var length = image.Layers.Length;
                for (int i = 0; i < length; i++)
                {
                    var smart = image.Layers[i] as SmartObjectLayer;
                    if (smart != null && smart.Name == "__D__")
                    {
                        using (var stream = new MemoryStream(smart.Contents))
                        {
                            stream.Position = 0;
                            using (var imageInSmart = (PsdImage)Image.Load(stream))
                            {
                                for (int j = 0; j < imageInSmart.Layers.Length; j++)

                                {
                                    // テキストレイヤーを検索
                                    var textLayer = imageInSmart.Layers[j] as TextLayer;
                                    if (textLayer != null)
                                    {
                                        var textData = textLayer.TextData;

                                        textData.Items[0].Text = "Best";
                                        textData.Items[0].Style.FontSize = 170;
                                    }
                                }

                                smart.ReplaceContents(imageInSmart);
                            }
                        }

                        break;
                    }
                }
                // この方法で変更されたPSDファイルを保存しています
                image.Save(outputSmartObjectPath, new PngOptions() { ColorType = PngColorType.TruecolorWithAlpha });
                image.Save(outputFile);
            }
{{< /highlight >}}

**PSDNET-805. 2つ以上のレイヤーエフェクトが存在する場合のブレンド順序とロジックが正しくない**

{{< highlight csharp >}}
            string sourceFile = "1_200x200.psd";
            string contentFile = "Numbers1Best.png";

            string outputFilePng = "output.png";
            string outputFilePsd = "output.psd";

            using (PsdImage image = (PsdImage)Image.Load(sourceFile, new PsdLoadOptions() { LoadEffectsResource = true }))
            {
                var length = image.Layers.Length;
                for (int i = 0; i < length; i++)
                {
                    var smart = image.Layers[i] as SmartObjectLayer;
                    if (smart != null && smart.Name == "__D__")
                    {
                        smart.ReplaceContents(contentFile);
                        break;
                    }
                }

                // この方法で変更されたPSDファイルを保存しています
                image.Save(outputFilePng, new PngOptions() { ColorType = PngColorType.TruecolorWithAlpha });
                image.Save(outputFilePsd);
            }
{{< /highlight >}}

**PSDNET-823. レイヤーグループのエクスペリエンスを向上させるためにSectionDividerLayerを追加**

{{< highlight csharp >}}
            // 以下のコードは、SectionDividerLayerレイヤーと関連するLayerGroupを取得する方法を示しています。

            // レイヤー階層
            //    [0]: '</レイヤーグループ>' グループ1用のSectionDividerLayer
            //    [1]: 'レイヤー1' 通常レイヤー
            //    [2]: '</レイヤーグループ>' グループ2用のSectionDividerLayer
            //    [3]: '</レイヤーグループ>' グループ3用のSectionDividerLayer
            //    [4]: 'グループ3' グループレイヤー
            //    [5]: 'グループ2' グループレイヤー
            //    [6]: 'グループ1' グループレイヤー

            void AssertAreEqual(object expected, object actual, string message = null)
            {
                if (!object.Equals(expected, actual))
                {
                    throw new FormatException(message ?? "オブジェクトが等しくありません。");
                }
            }

            using (var image = new PsdImage(100, 100))
            {
                // レイヤー階層を作成
                // レイヤーグループ 'グループ1' を追加
                LayerGroup group1 = image.AddLayerGroup("グループ1", 0, true);
                // 通常のレイヤーを追加
                Layer layer1 = new Layer();
                layer1.DisplayName = "レイヤー1";
                group1.AddLayer(layer1);
                // レイヤーグループ 'グループ2' を追加
                LayerGroup group2 = group1.AddLayerGroup("グループ2", 1);
                // レイヤーグループ 'グループ3' を追加
                LayerGroup group3 = group2.AddLayerGroup("グループ3", 0);

                // SectionDividerLayerを取得
                SectionDividerLayer divider1 = (SectionDividerLayer)image.Layers[0];
                SectionDividerLayer divider2 = (SectionDividerLayer)image.Layers[2];
                SectionDividerLayer divider3 = (SectionDividerLayer)image.Layers[3];

                // SectionDividerLayer.GetRelatedLayerGroup() メソッドを使用して、関連するLayerGroupインスタンスを取得
                AssertAreEqual(group1.DisplayName, divider1.GetRelatedLayerGroup().DisplayName); // 同じLayerGroup
                AssertAreEqual(group2.DisplayName, divider2.GetRelatedLayerGroup().DisplayName); // 同じLayerGroup
                AssertAreEqual(group3.DisplayName, divider3.GetRelatedLayerGroup().DisplayName); // 同じLayerGroup

                LayerGroup folder1 = divider1.GetRelatedLayerGroup();
                AssertAreEqual(5, folder1.Layers.Length); // 'グループ1' には5つのレイヤーが含まれています
            }
{{< /highlight >}}

**PSDNET-842. ストロークエフェクトのプロパティがPSDファイルに保存されていません**

{{< highlight csharp >}}
            void AssertAreEqual(object expected, object actual, string message = null)
            {
                if (!object.Equals(expected, actual))
                {
                    throw new FormatException(message ?? "オブジェクトが等しくありません。");
                }
            }

            string srcFile = "badStrokeEffect.psd";
            string output = "output.psd";

            using (var image = (PsdImage)Image.Load(srcFile, new PsdLoadOptions() { LoadEffectsResource = true }))
            {
                var layer1 = new Layer();
                image.AddLayer(layer1);
                layer1.BlendingOptions.AddStroke(FillType.Color); // ArgumentNullException はスローされません

                StrokeEffect strokeEffect = image.Layers[1].BlendingOptions.AddStroke(FillType.Color);
                strokeEffect.Size = 10;
                strokeEffect.Position = StrokePosition.Outside;
                strokeEffect.Overprint = true;

                image.Save(output);
            }

            // 保存された値をチェック
            using (var image = (PsdImage)Image.Load(output, new PsdLoadOptions() { LoadEffectsResource = true }))
            {
                StrokeEffect strokeEffect = (StrokeEffect)image.Layers[1].BlendingOptions.Effects[0];

                AssertAreEqual(10, strokeEffect.Size);
                AssertAreEqual(StrokePosition.Outside, strokeEffect.Position);
                AssertAreEqual(true, strokeEffect.Overprint);
            }
{{< /highlight >}}

---
title: Aspose.PSD for .NET 21.1 - リリースノート
type: docs
weight: 120
url: /ja/net/aspose-psd-for-net-21-1-release-notes/
---

{{% alert color="primary" %}} 

このページには、[Aspose.PSD for .NET 21.1](https://www.nuget.org/packages/Aspose.PSD/) のリリースノートが含まれています。

{{% /alert %}} 

|**キー**|**概要**|**カテゴリ**|
| :- | :- | :- |
|PSDNET-766|Aspose.PSD 20.10: 特定のPsdファイルをpngに変換しようとすると例外が発生する|バグ|
|PSDNET-792|スマートオブジェクトを含むPSDをPNGで保存する際の例外|バグ|

## **パブリックAPI変更**
# **追加されたAPI:**
- なし

# **削除されたAPI:**
- なし

## **使用例:**
**PSDNET-766. Aspose.PSD 20.10: 特定のPsdファイルをpngに変換しようとすると例外が発生する**
{{< highlight csharp >}}
            const string baseFolder = "PSDNET766_1\\";
            const string outputFolder = baseFolder + "output\\";
            string sourceFilePath = baseFolder + "school-admission-flyer-template-05052019.psd";
            string outputFilePath = outputFolder + "chool-admission-flyer-template-05052019_output.psd";
            string outputPngFilePath = Path.ChangeExtension(outputFilePath, ".png");
            PsdLoadOptions options = new PsdLoadOptions();
            using (PsdImage image = (PsdImage)Image.Load(sourceFilePath, options))
            {
                image.Save(outputFilePath, new PsdOptions(image));
                image.Save(outputPngFilePath, new PngOptions() { ColorType = PngColorType.TruecolorWithAlpha });
            }
{{< /highlight >}}

**PSDNET-792. スマートオブジェクトを含むPSDをPNGで保存する際の例外**
{{< highlight csharp >}}
            const string baseFolder = "PSDNET792_1\\";
            const string outputFolder = baseFolder + "output\\";
            string sourceFilePath = baseFolder + "1.psd";
            string outputFilePath = outputFolder+ "1_output.psd";
            string outputPngFilePath = Path.ChangeExtension(outputFilePath, ".png");
            PsdLoadOptions options = new PsdLoadOptions() { LoadEffectsResource = true };
            using (PsdImage image = (PsdImage)Image.Load(sourceFilePath, options))
            {
                var length = image.Layers.Length;
                for (int i = 0; i < length; i++)
                {
                    // スマートオブジェクトを探す
                    var smart = image.Layers[i] as SmartObjectLayer;
                    if (smart != null && smart.Name == "__D__")
                    {
                        // メモリストリームからSmartObjectLayerを読み込んでいます
                        // ただし、smart.ExportContents(somePath)を使ってスマートオブジェクトをファイルにエクスポートすることもできます
                        using (var stream = new MemoryStream(smart.Contents))
                        {
                            stream.Position = 0;
                            using (var imageInSmart = (PsdImage)Image.Load(stream))
                            {
                                for (int j = 0; j < imageInSmart.Layers.Length; j++)
                                {
                                    // テキストレイヤーを探す
                                    var textLayer = imageInSmart.Layers[j] as TextLayer;
                                    if (textLayer != null)
                                    {
                                        // UpdateTextを使うことができますが、この方法はテキストを部分的に編集する機能を提供します
                                        // 複数行テキストレイヤーやその他のテキストと段落スタイリング機能を作成できます
                                        // 注意してください。スマートオブジェクトのコンテンツがPSDでない場合、このテキスト編集方法は使用できません
                                        // そのような場合は、Graphic APIを使用する必要があります: https://docs.aspose.com/psd/net/drawing-images-using-graphics/
                                        var textData = textLayer.TextData;
                                        textData.Items[0].Text = "最高";

                                        // 画像を見栄え良くするためにテキストのサイズを変更する必要があります
                                        textData.Items[0].Style.FontSize = 170;
                                    }
                                }

                                // ReplaceContentsを使用すると、Smart Objectが自動的に再レンダリングされます
                                smart.ReplaceContents(imageInSmart);
                            }
                        }
                    }
                }

                // この方法で変更したPSDファイルを保存します
                image.Save(outputFilePath, new PsdOptions(image));
                image.Save(outputPngFilePath, new PngOptions() { ColorType = PngColorType.TruecolorWithAlpha });
            }
{{< /highlight >}}

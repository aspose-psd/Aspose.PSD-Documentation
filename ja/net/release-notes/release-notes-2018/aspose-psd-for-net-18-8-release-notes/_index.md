---
title: Aspose.PSD for .NET 18.8 - リリースノート
type: docs
weight: 50
url: /ja/net/aspose-psd-for-net-18-8-release-notes/
---

|**キー**|**要約**|**カテゴリ**|
| :- | :- | :- |
|PSDNET-68|レイヤー作成日時プロパティのサポート|機能|
|PSDNET-67|SheetColorハイライトのサポート|機能|
|PSDNET-66|レイヤーを1つから別のレイヤーにマージする機能|機能|
|PSDNET-65|テキストレイヤーのBoundBoxプロパティの部分的なサポートを追加|機能|
|PSDNET-64|IopaResourceのサポートを追加|機能|
|PSDNET-56|PSD形式のレイヤーエフェクトのサポート|機能|
|PSDNET-55| .Net向けのInterruptMonitorサポート|機能|
|PSDNET-50|レイヤーを平坦化する可能性を持たせる|機能|
|PSDNET-49|レイヤーのフィル透明度プロパティのレンダリングを追加|機能|
|PSDNET-43|曲線調整レイヤーのレンダリングを実装|機能|
|PSDNET-42|曲線調整レイヤーのサポートを追加|機能|
|PSDNET-41|レベル調整レイヤーのレンダリングを実装|機能|
|PSDNET-40|レベル調整レイヤーのサポートを追加|機能|
|PSDNET-37|チャンネルミキサー調整レイヤーのサポートを追加|機能|
|PSDNET-35|色相/彩度調整レイヤーのサポートを追加|機能|
|PSDNET-34|エクスポートのための露光調整レイヤーの実装|機能|
|PSDNET-31|ChannelMixer調整レイヤーのエクスポートのサポートを追加|機能|
|PSDNET-26|クリッピングマスクのサポートを追加|機能|
|PSDNET-13|レイヤーマスクのサポートを追加|機能|
|PSDNET-9|フォトフィルター調整レイヤーのサポートを追加|機能|
|PSDNET-8|チャンネルミキサー調整レイヤーのサポートを追加|機能|
|PSDNET-7|露光調整レイヤーのサポートを追加|機能|
|PSDNET-6|明るさ/コントラスト調整レイヤーのサポートを追加|機能|
|PSDNET-5|調整レイヤーの部分的なサポートを追加|機能|
|PSDNET-3|PSD NoBreakテキストオプションのサポートを追加|機能|
|PSDNET-2|ランタイムでのテキストレイヤーの追加の機能|機能|
|PSDNET-62|TIFFコーデックが16ビットチャネルイメージを保存できない|改善|
|PSDNET-61|PSDイメージの保存が無効なイメージカラーを生成する|改善|
|PSDNET-60|左上隅の座標が更新時に正しくない|改善|
|PSDNET-59|テキストレイヤーの更新時に例外が発生する|改善|
|PSDNET-58|JPEG2000イメージのCodecプロパティを公開|改善|
|PSDNET-57|BMPへのエクスポートのための24bppオプション設定を修正|改善|
|PSDNET-46|CMYK PSD変換のための調整レイヤーが無視される|改善|

## **使用例:**
**PSDNET-68 レイヤー作成日時プロパティのサポート**

{{< highlight java >}}

 // レイヤー作成日時プロパティの使用例

string sourceFileName = "OneLayer.psd";

using (var im = (PsdImage)(Image.Load(sourceFileName)))

{

    var layer = im.Layers[0];

    var creationDateTime = layer.LayerCreationDateTime;

    var expectedDateTime = new DateTime(2018, 7, 17, 8, 57, 24, 769);

    Assert.AreEqual(expectedDateTime, creationDateTime);

    var now = DateTime.Now;

    var createdLayer = im.AddLevelsAdjustmentLayer();

    // 新しく作成されたレイヤーの作成日時が更新されたことを確認

    Assert.True(now <= createdLayer.LayerCreationDateTime);

}

{{< /highlight >}}

**PSDNET-67 SheetColorハイライトのサポート**

{{< highlight java >}}

 // SheetColorHighlightプロパティの使用例

string sourceFileName = "SheetColorHighlightExample.psd";

string exportPath = "SheetColorHighlightExampleChanged.psd";

using (var im = (PsdImage)(Image.Load(sourceFileName)))

{

    var layer1 = im.Layers[0];

    Assert.AreEqual(SheetColorHighlightEnum.Violet, layer1.SheetColorHighlight);

    var layer2 = im.Layers[1];

    Assert.AreEqual(SheetColorHighlightEnum.Orange, layer2.SheetColorHighlight);



    layer1.SheetColorHighlight = SheetColorHighlightEnum.Yellow;



    im.Save(exportPath);	

}

{{< /highlight >}}

**PSDNET-66 レイヤーを1つから別のレイヤーにマージする機能**

{{< highlight java >}}

 // 2つのレイヤーをマージする例

var sourceFile1 = "FillOpacitySample.psd";

var sourceFile2 = "ThreeRegularLayersSemiTransparent.psd";

var exportPath = "MergedLayersFromTwoDifferentPsd.psd" 

using (var im1 = (PsdImage)(Image.Load(sourceFile1)))

{

    var layer1 = im1.Layers[1];

    using (var im2 = (PsdImage)(Image.Load(sourceFile2)))

    {

        var layer2 = im2.Layers[0];

        layer1.MergeLayerTo(layer2);

	im2.Save(exportPath);	

    }

}

{{< /highlight >}}

**PSDNET-65 テキストレイヤーのBoundBoxプロパティの部分的なサポート**

{{< highlight java >}}

 // TextBoxBoundsの例

string sourceFileName = "LayerWithText.psd";

var correctOpticalSize = new Size(127, 45);

var correctBoundBox = new Size(172, 62);

using (var im = (PsdImage)(Image.Load(sourceFileName)))

{

    var textLayer = (TextLayer)im.Layers[1];

    // レイヤーのサイズはレンダリングエリアのサイズです

    var opticalSize = textLayer.Size;

    Assert.AreEqual(correctOpticalSize, opticalSize);

    // TextBoundBoxはテキストレイヤーの最大サイズです。 

    // この領域にPSはテキストを収めようとします

    var boundBox = textLayer.TextBoundBox;

    Assert.AreEqual(correctBoundBox, boundBox);

}

{{< /highlight >}}

**PSDNET-64 IopaResourceのサポートを追加**

{{< highlight java >}}

 // IopaResourceの変更によるFill Opacityプロパティの変更

string sourceFileName = "FillOpacitySample.psd";

string exportPath = "FillOpacitySampleChanged.psd";

using (var im = (PsdImage)(Image.Load(sourceFileName)))

{

    var layer = im.Layers[2];



    var resources = layer.Resources;

    foreach (var resource in resources)

    {

        if (resource is IopaResource)

        {

            var iopaResource = (IopaResource)resource;

            iopaResource.FillOpacity = 200;

        }

    }



    im.Save(exportPath);	

}

{{< /highlight >}}

**PSDNET-56 PSD形式のレイヤーエフェクトのサポート**

{{< highlight java >}}

 using (

    PsdImage image =

        (PsdImage)

        Aspose.PSD.Image.Load(

            sourceFileName,

            new Aspose.PSD.ImageLoadOptions.PsdLoadOptions()

            {

                LoadEffectsResource = true,

                UseDiskForLoadEffectsResource = true

            }))

{

    image.Save(

                output,

                new Aspose.PSD.ImageOptions.PngOptions()

                {

                    ColorType =

                            Aspose.PSD.FileFormats.Png

                            .PngColorType

                            .TruecolorWithAlpha

                });

}

{{< /highlight >}}

**PSDNET-55 InterruptMonitorの.NETサポート**

{{< highlight java >}}

         public void InterruptMonitorTest(string dir, string ouputDir)

        {

            ImageOptionsBase saveOptions = new ImageOptions.PngOptions();

            Multithreading.InterruptMonitor monitor = new Multithreading.InterruptMonitor();

            SaveImageWorker worker = new SaveImageWorker(dir + "big.psb", dir + "big_out.png", saveOptions, monitor);

            System.Threading.Thread thread = new System.Threading.Thread(new System.Threading.ThreadStart(worker.ThreadProc));

            try

            {

                thread.Start();

                // タイムアウトは、完全な画像変換に必要な時間よりも短くする必要があります。

                System.Threading.Thread.Sleep(3000);

                // プロセスを中断

                monitor.Interrupt();

                System.Console.WriteLine("保存スレッド#{0}を中断します: {1}", thread.ManagedThreadId, System.DateTime.Now);

                // 中断を待つ...

                thread.Join();

            }

            finally

            {

                // 削除するファイルが存在しない場合、例外がスローされません。

                System.IO.File.Delete(dir + "big_out.png");

            }

        }

        /// <summary>

        /// 画像変換を開始し、割り込みを待機します。

        /// </summary>

        private class SaveImageWorker

        {

            /// <summary>

            /// 入力イメージへのパス。

            /// </summary>

            private readonly string inputPath;

            /// <summary>

            /// 出力イメージへのパス。

            /// </summary>

            private readonly string outputPath;

            /// <summary>

            /// 割り込みモニター。

            /// </summary>

            private readonly Multithreading.InterruptMonitor monitor;

            /// <summary>

            /// 保存オプション。

            /// </summary>

            private readonly ImageOptionsBase saveOptions;

            /// <summary>

            /// <see cref="SaveImageWorker" />クラスの新しいインスタンスを初期化します。

            /// </summary>

            /// <param name="inputPath">入力イメージへのパス。</param>

            /// <param name="outputPath">出力イメージへのパス。</param>

            /// <param name="saveOptions">保存オプション。</param>

            /// <param name="monitor">割り込みモニター。</param>

            public SaveImageWorker(string inputPath, string outputPath, ImageOptionsBase saveOptions, Multithreading.InterruptMonitor monitor)

            {

                this.inputPath = inputPath;

                this.outputPath = outputPath;

                this.saveOptions = saveOptions;

                this.monitor = monitor;

            }

            /// <summary>

            /// 画像を別の形式に変換します。割り込みを処理します。

            /// </summary>

            public void ThreadProc()

            {

                using (Image image = Image.Load(this.inputPath))

                {

                    Multithreading.InterruptMonitor.ThreadLocalInstance = this.monitor;

                    try

                    {

                        image.Save(this.outputPath, this.saveOptions);

                        Assert.Fail("割り込みが予想されています。");

                    }

                    catch (CoreExceptions.OperationInterruptedException e)

                    {

                        System.Console.WriteLine("保存スレッド#{0}: {1}で終了しました", System.Threading.Thread.CurrentThread.ManagedThreadId, System.DateTime.Now);

                        System.Console.WriteLine(e);

                    }

                    catch (System.Exception e)

                    {

                        System.Console.WriteLine(e);

                    }

                    finally

                    {

                        Multithreading.InterruptMonitor.ThreadLocalInstance = null;

                    }

                }

            }

        }

{{< /highlight >}}

**PSDNET-50 レイヤーを平坦化する可能性** 

{{< highlight java >}}

 // PSD全体を平坦化する

string sourceFileName = "ThreeRegularLayersSemiTransparent.psd";

string exportPath = "ThreeRegularLayersSemiTransparentFlattened.psd";

using (var im = (PsdImage)(Image.Load(sourceFileName)))

{

    im.FlattenImage();

    im.Save(exportPath);	 

}

// レイヤーを他のレイヤーにマージする

string sourceFileName = "ThreeRegularLayersSemiTransparent.psd";

string exportPath = "ThreeRegularLayersSemiTransparentFlattenedLayerByLayer.psd";

using (var im = (PsdImage)(Image.Load(sourceFileName)))

{

    var bottomLayer = im.Layers[0];

    var middleLayer = im.Layers[1];

    var topLayer = im.Layers[2];

    var layer1 = im.MergeLayers(bottomLayer, middleLayer);

    var layer2 = im.MergeLayers(layer1, topLayer);

    // マージされたレイヤーを設定

    im.Layers = new Layer[] { layer2 };



    im.Save(exportPath);	 

}

{{< /highlight >}}

**PSDNET-49 レイヤーのフィル透明度プロパティのレンダリングを追加** 

{{< highlight java >}}

 // Fill Opacityプロパティの変更

string sourceFileName = "FillOpacitySample.psd";

string exportPath = "FillOpacitySampleChanged.psd";

using (var im = (PsdImage)(Image.Load(sourceFileName)))

{

    var layer = im.Layers[2];

    layer.FillOpacity = 5;

    im.Save(exportPath);	

}

{{< /highlight >}}

**PSDNET-43 曲線調整レイヤーのレンダリングを実装** 

{{< highlight java >}}

 // 曲線レイヤーの編集

string sourceFileName = "CurvesAdjustmentLayer";

string psdPathAfterChange = "CurvesAdjustmentLayerChanged";

string pngExportPath = "CurvesAdjustmentLayerChanged";

for (int j = 1; j < 2; j++)

{

    using (var im = LoadFile(sourceFileName + j.ToString() + ".psd"))

    {

        foreach (var layer in im.Layers)

	{

            if (layer is CurvesLayer)

            {

                 var curvesLayer = (CurvesLayer)layer;

                 if (curvesLayer.IsDiscreteManagerUsed)

                 {

                      var manager = (CurvesDiscreteManager)curvesLayer.GetCurvesManager();

                      for (int i = 10; i < 50; i++)

                      {

                           manager.SetValueInPosition(0, (byte)i, (byte)(15 + (i * 2)));

                      }

                 }

                 else

                 {

                      var manager = (CurvesContinuousManager)curvesLayer.GetCurvesManager();

                      manager.AddCurvePoint(0, 50, 100);

                      manager.AddCurvePoint(0, 150, 130);

                 }

            }

        }

    }



    // PSDを保存

    im.Save(psdPathAfterChange + j.ToString() + ".psd");



    // PNGを保存

    var saveOptions = new PngOptions();

    saveOptions.ColorType = PngColorType.TruecolorWithAlpha;

    im.Save(pngExportPath + j.ToString() + ".png", saveOptions);

}

{{< /highlight >}}

**PSDNET-42 曲線調整レイヤーのサポートを追加** 

{{< highlight java >}}

 // 曲線レイヤーの編集

string sourceFileName = "CurvesAdjustmentLayer";

string psdPathAfterChange = "CurvesAdjustmentLayerChanged";

for (int j = 1; j < 2; j++)

{

    using (var im = LoadFile(sourceFileName + j.ToString() + ".psd"))

    {

         foreach (var layer in im.Layers)

	 {

            if (layer is CurvesLayer)

            {

                 var curvesLayer = (CurvesLayer)layer;

                 if (curvesLayer.IsDiscreteManagerUsed)

                 {

                      var manager = (CurvesDiscreteManager)curvesLayer.GetCurvesManager();

                      for (int i = 10; i < 50; i++)

                      {

                           manager.SetValueInPosition(0, (byte)i, (byte)(15 + (i * 2)));

                      }

                 }

                 else

                 {

                      var manager = (CurvesContinuousManager)curvesLayer.GetCurvesManager();

                      manager.AddCurvePoint(0, 50, 100);

                      manager.AddCurvePoint(0, 150, 130);

                 }

            }

	}

    }



    // PSDを保存

    im.Save(psdPathAfterChange + j.ToString() + ".psd");

}

{{< /highlight >}}

**PSDNET-41 レベル調整レイヤーのレンダリングを実装** 

{{< highlight java >}}

 // レベルレイヤーの編集

string sourceFileName = "LevelsAdjustmentLayer.psd";

string psdPathAfterChange = "LevelsAdjustmentLayerChanged.psd";

string pngExportPath = "LevelsAdjustmentLayerChanged.png";

using (var im = LoadFile(sourceFileName))

{

    foreach (var layer in im.Layers)

    {

        if (layer is LevelsLayer)

        {

            var levelsLayer = (LevelsLayer)layer;

            var channel = levelsLayer.GetChannel(0);

            channel.InputMidtoneLevel = 2.0f;

            channel.InputShadowLevel = 10;

            channel.InputHighlightLevel = 230;

            channel.OutputShadowLevel = 20;

            channel.OutputHighlightLevel = 200;

        }

    }



    // PSDを保存

    im.Save(psdPathAfterChange);



    // PNGを保存

    var saveOptions = new PngOptions();

    saveOptions.ColorType = PngColorType.TruecolorWithAlpha;

    im.Save(pngExportPath, saveOptions);

}

{{< /highlight >}}

**PSDNET-40 レベル調整レイヤーのサポートを追加** 

{{< highlight java >}}

 // レベルレイヤーの編集

string sourceFileName = "LevelsAdjustmentLayer.psd";

string psdPathAfterChange = "LevelsAdjustmentLayerChanged.psd";

using (var im = LoadFile(sourceFileName))

{

    foreach (var layer in im.Layers)

    {

        if (layer is LevelsLayer)

        {

            var levelsLayer = (LevelsLayer)layer;

            var channel = levelsLayer.GetChannel(0);

            channel.InputMidtoneLevel = 2.0f;

            channel.InputShadowLevel = 10;

            channel.InputHighlightLevel = 230;

            channel.OutputShadowLevel = 20;

            channel.OutputHighlightLevel = 200;

        }

    }



    // PSDを保存

    im.Save(psdPathAfterChange);

}

{{< /highlight >}}

**PSDNET-37 チャンネルミキサー調整レイヤーのサポートを追加** 

{{< highlight java >}}



// RGBチャンネルミキサー

string sourceFileName = "ChannelMixerAdjustmentLayerRgb.psd";

string psdPathAfterChange = "ChannelMixerAdjustmentLayerRgbChanged.psd";

using (var im = LoadFile(sourceFileName))

{

    foreach (var layer in im.Layers)

    {

         if (layer is RgbChannelMixerLayer)

         {

              var rgbLayer = (RgbChannelMixerLayer)layer;

              rgbLayer.RedChannel.Blue = 100;

              rgbLayer.BlueChannel.Green = -100;

              rgbLayer.GreenChannel.Constant = 50;

         }

    }



    im.Save(psdPathAfterChange);

}

// CMYKチャンネルミキサー

string sourceFileName = "ChannelMixerAdjustmentLayerCmyk.psd";

string psdPathAfterChange = "ChannelMixerAdjustmentLayerCmykChanged.psd";

using (var im = LoadFile(sourceFileName))

{

    foreach (var layer in im.Layers)

    {

         if (layer is CmykChannelMixerLayer)

         {

             var cmykLayer = (CmykChannelMixerLayer)layer;

             cmykLayer.CyanChannel.Black = 20;

             cmykLayer.MagentaChannel.Yellow = 50;

             cmykLayer.YellowChannel.Cyan = -25;

             cmykLayer.BlackChannel.Yellow = 25;

         }

    }



    im.Save(psdPathAfterChange);

}



// 新しいレイヤーの追加（この例ではCmyk）

string sourceFileName = "CmykWithAlpha.psd";

string psdPathAfterChange = "ChannelMixerAdjustmentLayerCmykChanged.psd";

using (var im = LoadFile(sourceFileName))

{

    var newlayer = im.AddChannelMixerAdjustmentLayer();

    newlayer.GetChannelByIndex(2).Constant = 50;

    newlayer.GetChannelByIndex(0).Constant = 50;



    im.Save(psdPathAfterChange);

}		

{{< /highlight >}}

**PSDNET-35 色相/彩度調整レイヤーのサポートを追加** 

{{< highlight java >}}

 // 色相/彩度レイヤーの編集

string sourceFileName = "HueSaturationAdjustmentLayer.psd";

string psdPathAfterChange = "HueSaturationAdjustmentLayerChanged.psd";

using (var im = LoadFile(sourceFileName))

{

     foreach (var layer in im.Layers)

     {

           if (layer is HueSaturationLayer)

           {

                var hueLayer = (HueSaturationLayer)layer;

                hueLayer.Hue = -25;

                hueLayer.Saturation = -12;

                hueLayer.Lightness = 67;

                var colorRange = hueLayer.GetRange(2);

                colorRange.Hue = -40;

                colorRange.Saturation = 50;

                colorRange.Lightness = -20;

                colorRange.MostLeftBorder = 300;

           }

      }

      im.Save(psdPathAfterChange);

}



// 色相/彩度レイヤーの追加

string sourceFileName = "PhotoExample.psd";

string psdPathAfterChange = "PhotoExampleAddedHueSaturation.psd";



using (PsdImage im = LoadFile(sourceFileName))

{

     this.SaveForVisualTest(im, this.OutputPath, prefix + file, "before");

     var hueLayer = im.AddHueSaturationAdjustmentLayer();

     hueLayer.Hue = -25;

     hueLayer.Saturation = -12;

     hueLayer.Lightness = 67;

     var colorRange = hueLayer.GetRange(2);

     colorRange.Hue = -160;

     colorRange.Saturation = 100;

     colorRange.Lightness = 20;

     colorRange.MostLeftBorder = 300;



     im.Save(psdPathAfterChange);

}

{{< /highlight >}}
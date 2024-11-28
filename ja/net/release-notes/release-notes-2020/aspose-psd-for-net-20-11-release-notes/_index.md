---
title: Aspose.PSD for .NET 20.11 - リリースノート
type: docs
weight: 20
url: /ja/net/aspose-psd-for-net-20-11-release-notes/
---

{{% alert color="primary" %}} 

このページには、[Aspose.PSD for .NET 20.11](https://www.nuget.org/packages/Aspose.PSD/) のリリースノートが含まれています。

{{% /alert %}} 

|**キー**|**概要**|**カテゴリ**|
| :- | :- | :- |
|PSDNET-713|Aspose.PSD が PSD を他のカラーモード/ビット深度に変換できない問題|機能|
|PSDNET-754|PSD 画像内の Smart Object レイヤーをコピーする機能の追加|機能|
|PSDNET-267|レイヤーエフェクトを含む PSD ファイルの読み込みと保存時に例外発生|バグ|
|PSDNET-579|メソッド "Image.LoadRawData" が NullPointer 例外をスローする|バグ|
|PSDNET-741|ファイルを開こうとすると ImageLoadException がスローされる|バグ|
|PSDNET-744|Aspose.PSD 20.10: Psd を読み込めない|バグ|

## **パブリック API の変更**
# **追加された API:**
- M:Aspose.PSD.FileFormats.Psd.PsdImage.Convert(Aspose.PSD.ImageOptions.PsdOptions)
- F:Aspose.PSD.FileFormats.Psd.ResourceBlock.ResouceBlockMeSaSignature
- M:Aspose.PSD.FileFormats.Psd.Layers.SmartObjects.SmartObjectLayer.NewSmartObjectViaCopy
- M:Aspose.PSD.FileFormats.Psd.Layers.SmartObjects.SmartObjectLayer.DuplicateLayer
- M:Aspose.PSD.FileFormats.Psd.SmartObjectProvider.NewSmartObjectViaCopy(Aspose.PSD.FileFormats.Psd.Layers.SmartObjects.SmartObjectLayer)
- M:Aspose.PSD.FileFormats.Psd.SmartObjectProvider.ConvertToSmartObject(System.Int32[])
- M:Aspose.PSD.FileFormats.Psd.SmartObjectProvider.ConvertToSmartObject(Aspose.PSD.FileFormats.Psd.Layers.Layer[])
# **削除された API:**
- なし

## **使用例:**
**PSDNET-267. レイヤーエフェクトを含む PSD ファイルの読み込みと保存時に例外が発生する場合**
{{< highlight csharp >}}
            string dataDir = "PSDNET267_1\\";
            string inputFilePath = dataDir + "LayerEffectsTest.psd";
            string outputFilePath = dataDir + "LayerEffectsTestOutput.psd";
            using (var image = (PsdImage)Image.Load(inputFilePath, new PsdLoadOptions() { LoadEffectsResource = true }))
            {
                image.Save(outputFilePath, new PsdOptions(image));
            }
{{< /highlight >}}
**PSDNET-579. メソッド "Image.LoadRawData" が NullPointer 例外をスローする場合**
{{< highlight csharp >}}
            string dataDir = "PSDNET579_1\\";
            string srcFile = dataDir + "CmykWithAlpha_raw.psd";
            using (RasterImage image = (RasterImage)Image.Load(srcFile))
            {
                Rectangle rect = image.Bounds;
                RawDataRetriever rawDataRetriever = new RawDataRetriever(rect, image.RawDataSettings);
                image.LoadRawData(rect, image.RawDataSettings, rawDataRetriever);
                rawDataRetriever.GetData();
            }

    class RawDataRetriever : Aspose.PSD.IPartialRawDataLoader
    {
        private readonly byte[] rawData;
        private int rawDataIndex;

        public RawDataRetriever(Rectangle rectangle, RawDataSettings rawDataSettings)
        {
            int totalSize = rawDataSettings.LineSize * rectangle.Height;
            if (totalSize == 0)
            {
                totalSize = rectangle.Width * rectangle.Height * 5;
            }

            this.rawData = new byte[totalSize];
        }

        public byte[] GetData()
        {
            return this.rawData;
        }

        public void Process(Rectangle rectangle, byte[] data, Point start, Point end)
        {
            Array.Copy(data, 0, this.rawData, this.rawDataIndex, data.Length);
            this.rawDataIndex += data.Length;
        }

        public void Process(Rectangle rectangle, byte[] data, Point start, Point end, LoadOptions loadOptions)
        {
            throw new NotImplementedException();
        }
    }
{{< /highlight >}}
**PSDNET-713. Aspose.PSD が PSD を他のカラーモード/ビット深度に変換できない問題の場合**
{{< highlight csharp >}}
            string dataDir = "PSDNET713_1\\";
            string outputDir = dataDir + "output\\";

            // これらの例では、PSD 画像形式を他のカラーモード/ビット深度に変換する方法を示しています。
            ImageConversion(ColorModes.Grayscale, 16, 2);
            ImageConversion(ColorModes.Grayscale, 8, 2);
            ImageConversion(ColorModes.Grayscale, 8, 1);
            ImageConversion(ColorModes.Rgb, 8, 4);
            ImageConversion(ColorModes.Rgb, 16, 4);
            ImageConversion(ColorModes.Cmyk, 8, 5);
            ImageConversion(ColorModes.Cmyk, 16, 5);

            void ImageConversion(ColorModes colorMode, short channelBitsCount, short channelsCount)
            {
                var compression = channelBitsCount > 8 ? CompressionMethod.Raw : CompressionMethod.RLE;
                SaveToPsdThenLoadAndSaveToPng(
                    "SheetColorHighlightExample",
                    colorMode,
                    channelBitsCount,
                    channelsCount,
                    compression,
                    1);
                SaveToPsdThenLoadAndSaveToPng(
                    "FillOpacitySample",
                    colorMode,
                    channelBitsCount,
                    channelsCount,
                    compression,
                    2);
                SaveToPsdThenLoadAndSaveToPng(
                    "ClippingMaskRegular",
                    colorMode,
                    channelBitsCount,
                    channelsCount,
                    compression,
                    3);
            }

            // PSD に保存してから読み込んで PNG に保存します。
            void SaveToPsdThenLoadAndSaveToPng(
                string file,
                ColorModes colorMode,
                short channelBitsCount,
                short channelsCount,
                CompressionMethod compression,
                int layerNumber)
            {
                string srcFile = dataDir + file + ".psd";
                string postfix = colorMode.ToString() + channelBitsCount + "bits" + channelsCount + "channels" +
                                 compression;
                string fileName = file + "_" + postfix + ".psd";
                string exportPath = outputDir + fileName;
                PsdOptions psdOptions = new PsdOptions()
                {
                    ColorMode = colorMode,
                    ChannelBitsCount = channelBitsCount,
                    ChannelsCount = channelsCount,
                    CompressionMethod = compression
                };
                using (var image = (PsdImage)Image.Load(srcFile))
                {
                    image.Convert(psdOptions);

                    RasterCachedImage raster = image.Layers.Length > 0 && layerNumber >= 0
                        ? (RasterCachedImage)image.Layers[layerNumber]
                        : image;
                    Aspose.PSD.Graphics graphics = new Graphics(raster);
                    int width = raster.Width;
                    int height = raster.Height;
                    Rectangle rect = new Rectangle(
                        width / 3,
                        height / 3,
                        width - (2 * (width / 3)) - 1,
                        height - (2 * (height / 3)) - 1);
                    graphics.DrawRectangle(new Aspose.PSD.Pen(Color.DarkGray, 1), rect);

                    image.Save(exportPath);
                }

                string pngExportPath = Path.ChangeExtension(exportPath, "png");
                using (PsdImage image = (PsdImage)Image.Load(exportPath))
                {
                    image.Save(pngExportPath, new PngOptions() { ColorType = PngColorType.TruecolorWithAlpha });
                }
            }
{{< /highlight >}}
**PSDNET-741. ファイルを開こうとすると ImageLoadException がスローされる場合**
{{< highlight csharp >}}
            string dataDir = "PSDNET741_1\\";
            string inputFile = dataDir + "input.psd";
            string outputFile = dataDir + "output.psd";

            using (var psdImage = (PsdImage)Image.Load(inputFile))
            {
                psdImage.Save(outputFile, new PsdOptions(psdImage));
            }

            using (var psdImage2 = (PsdImage)Image.Load(outputFile))
            {
                // ここでは例外は発生しません...
            }
{{< /highlight >}}
**PSDNET-744. Aspose.PSD 20.10: Psd を読み込めない場合**
{{< highlight csharp >}}
            void AreEqual(object expected, object actual)
            {
                if (!object.Equals(expected, actual))
                {
                    throw new Exception("Values are not equal.");
                }
            }

            string srcFile = "GST-CHALLAN(2)1..psd";
            string output = "output.psd";

            using (PsdImage psdImage = (PsdImage)Image.Load(srcFile))
            {
                AreEqual(ResourceBlock.ResouceBlockMeSaSignature, psdImage.ImageResources[23].Signature);
                AreEqual(ResourceBlock.ResouceBlockMeSaSignature, psdImage.ImageResources[24].Signature);
                psdImage.Save(output);
            }
{{< /highlight >}}
**PSDNET-754. PSD 画像内で Smart Object レイヤーをコピーする機能の追加**
{{< highlight csharp >}}
            string dataDir = "PSDNET754_1\\";
            string outputDir = dataDir + "output\\";

            // これらの例は、PSD 画像でスマートオブジェクトレイヤーをコピーする方法を示しています。
            ExampleOfCopingSmartObjectLayer("r-embedded-psd");
            ExampleOfCopingSmartObjectLayer("r-embedded-png");
            ExampleOfCopingSmartObjectLayer("r-embedded-transform");
            ExampleOfCopingSmartObjectLayer("new_panama-papers-8-trans4");

            void ExampleOfCopingSmartObjectLayer(string fileName)
            {
                int layerNumber = 0; // コピーするレイヤー番号
                string filePath = dataDir + fileName + ".psd";
                string outputFilePath = outputDir + fileName + "_copy_" + layerNumber;
                string pngOutputPath = outputFilePath + ".png";
                string psdOutputPath = outputFilePath + ".psd";
                using (PsdImage image = (PsdImage)Image.Load(filePath))
                {
                    var smartObjectLayer = (SmartObjectLayer)image.Layers[layerNumber];
                    var newLayer = smartObjectLayer.NewSmartObjectViaCopy();
                    newLayer.IsVisible = false;
                    AssertIsTrue(object.ReferenceEquals(newLayer, image.Layers[layerNumber + 1]));
                    AssertIsTrue(object.ReferenceEquals(smartObjectLayer, image.Layers[layerNumber]));

                    var duplicatedLayer = smartObjectLayer.DuplicateLayer();
                    duplicatedLayer.DisplayName = smartObjectLayer.DisplayName + " 共有画像";
                    AssertIsTrue(object.ReferenceEquals(newLayer, image.Layers[layerNumber + 2]));
                    AssertIsTrue(object.ReferenceEquals(duplicatedLayer, image.Layers[layerNumber + 1]));
                    AssertIsTrue(object.ReferenceEquals(smartObjectLayer, image.Layers[layerNumber]));

                    using (var innerImage = (RasterImage)smartObjectLayer.LoadContents(null))
                    {
                        // 埋め込まれたスマートオブジェクト画像を反転させます（内部 PSD 画像の場合は最初のレイヤーのみを反転します）
                        InvertImage(innerImage);

                        // PSD レイヤー内の埋め込まれたスマートオブジェクト画像を置換します
                        smartObjectLayer.ReplaceContents(innerImage);
                    }

                    // 複製されたレイヤーは元のスマートオブジェクトとその埋め込まれた画像を共有し、
                    // 明示的に更新する必要があります。そうしないと、描画キャッシュが変更されません。
                    // すべてのスマートオブジェクトを更新して、NewSmartObjectViaCopy によって作成された新しいレイヤーが他の埋め込まれた画像と共有されないようにします。
                    image.SmartObjectProvider.UpdateAllModifiedContent();

                    image.Save(pngOutputPath, new PngOptions() { ColorType = PngColorType.TruecolorWithAlpha });
                    image.Save(psdOutputPath, new PsdOptions(image));
                }
            }

            // PSD 画像を含むラスター画像を反転します。
            void InvertImage(RasterImage innerImage)
            {
                var innerPsdImage = innerImage as PsdImage;
                if (innerPsdImage != null)
                {
                    InvertRasterImage(innerPsdImage.Layers[0]);
                }
                else
                {
                    InvertRasterImage(innerImage);
                }
            }

            // ラスター画像を反転します。
            void InvertRasterImage(RasterImage innerImage)
            {
                var pixels = innerImage.LoadArgb32Pixels(innerImage.Bounds);
                for (int i = 0; i < pixels.Length; i++)
                {
                    var pixel = pixels[i];
                    var alpha = (int)(pixel & 0xff000000);
                    pixels[i] = (~(pixel & 0x00ffffff)) | alpha;
                }

                innerImage.SaveArgb32Pixels(innerImage.Bounds, pixels);
            }

            void AssertIsTrue(bool condition)
            {
                if (!condition)
                {
                    throw new FormatException(string.Format("Expected true"));
                }
            }
{{< /highlight >}}
---
title: Aspose.PSD for .NET 19.8 - リリースノート
type: docs
weight: 50
url: /ja/net/aspose-psd-for-net-19-8-release-notes/
---

{{% alert color="primary" %}} 

このページには、Aspose.PSD for .NET 19.8のリリースノートが含まれています。

{{% /alert %}} 

|**キー**|**概要**|**カテゴリ**|
| :- | :- | :- |
|PSDNET-184|ストリームからPsdImageにJPEG、PNGなどの画像ファイルを読み込む|機能|
|PSDNET-134|塗りつぶしレイヤーのレンダリングを実装: グラデーション|機能|
|PSDNET-166|PSDをPDFに保存しても選択可能なテキストが提供されない|機能|
|PSDNET-158|PSBをPDFとして保存するサポート|機能|
|PSDNET-189|ReadOnlyモードでPSDを読み込む際の高いメモリ使用量|強化|
|PSDNET-171|新しいTextLayerを作成した後、PSDファイルがPSで読めなくなる|バグ|
|PSDNET-156|PSDを読み込む際の例外|バグ|

## **公開APIの変更**
# **追加されたAPI:**
- M:Aspose.PSD.FileFormats.Psd.Layers.Layer.#ctor(System.IO.Stream)
- M:Aspose.PSD.FileFormats.Psd.Layers.Layer.#ctor(Aspose.PSD.RasterImage,System.Boolean)
# **削除されたAPI:**
- M:Aspose.PSD.FileFormats.Psd.Layers.Layer.#ctor(Aspose.PSD.RasterImage)

## **使用例:**
**PSDNET-184. JPEG、PNGなどの画像ファイルをストリームからPsdImageに読み込む**

{{< highlight java >}}

    // JPEG、PNGなどの画像ファイルをストリームからPsdImageに読み込む

    string outputFilePath = "PsdResult.psd";

    var filesList = new string[]

    {

        "PsdExample.psd",

        "BmpExample.bmp",

        "GifExample.gif",

        "Jpeg2000Example.jpf",

        "JpegExample.jpg",

        "PngExample.png",

        "TiffExample.tif",

    };

    using (var image = new PsdImage(200, 200))

    {

        foreach (var fileName in filesList)

        {

            string filePath = fileName;

            using (var stream = new FileStream(filePath, FileMode.Open))

            {

                Layer layer = null;

                try

                {

                     layer = new Layer(stream);

                     image.AddLayer(layer);

                }

                catch (Exception e)

                {

                    if (layer != null)

                    {

                        layer.Dispose();

                    }

                    throw e;

                }

            }

        }

        image.Save(outputFilePath);

    }

{{< /highlight >}}

**PSDNET-134. 塗りつぶしレイヤーのレンダリングを実装: グラデーション**

{{< highlight java >}}

             // 塗りつぶしレイヤーのレンダリングを実装: グラデーション

            string fileName = "FillLayerGradient.psd";

            GradientType[] gradientTypes = new[]

            {

                GradientType.Linear, GradientType.Radial, GradientType.Angle, GradientType.Reflected, GradientType.Diamond

            };

            using (var image = Image.Load(fileName))

            {

                PsdImage psdImage = (PsdImage)image;

                FillLayer fillLayer = (FillLayer)psdImage.Layers[0];

                GradientFillSettings fillSettings = (GradientFillSettings)fillLayer.FillSettings;

                foreach (var gradientType in gradientTypes)

                {

                    fillSettings.GradientType = gradientType;

                    fillLayer.Update();

                    psdImage.Save(fileName + "_" + gradientType.ToString() + ".png", new PngOptions() { ColorType = PngColorType.TruecolorWithAlpha });

                }

            }

{{< /highlight >}}

**PSDNET-166. PSDをPDFに保存しても選択可能なテキストが提供されない**

{{< highlight java >}}

  // PSDをPDFに保存しても選択可能なテキストが提供されない

    string sourceFileName = "text.psd";

    using (PsdImage image = (PsdImage)Image.Load(sourceFileName))

    {

        string outFileName = "text.pdf";

        image.Save(outFileName, new PdfOptions());

    }

{{< /highlight >}}

**PSDNET-171. 新しいTextLayerを作成した後、PSDファイルがPSで読めなくなる**

{{< highlight java >}}

 // 新しいTextLayerを作成した後、ビルドサーバーでPSDファイルがPSで読めなくなる

    string sourceFileName = "OneLayer.psd";

    string outFileName = "OneLayerWithAddedText.psd";

    using (PsdImage image = (PsdImage)Image.Load(sourceFileName))

    {

        image.AddTextLayer("Some text", new Rectangle(50, 50, 100, 100));

        PsdOptions options = new PsdOptions(image);

        image.Save(outFileName, options);

    }

{{< /highlight >}}



**PSDNET-156. PSDを読み込む際の例外**

{{< highlight java >}}

 using (var image = Image.Load("isolated_Copy.psd"))

{

}

{{< /highlight >}}

**PSDNET-189. ReadOnlyモードでPSDを読み込む際の高いメモリ使用量**

{{< highlight java >}}

 // ReadOnlyモードでPSDを読み込む際の高いメモリ使用量

            string sourceFileName = "White 3D Text Effect.psd";

            string outFileName = "Exported.png";

            LoadOptions loadOptions = new PsdLoadOptions() { ReadOnlyMode = true };

            ImageOptionsBase saveOptions = new PngOptions() { ColorType = PngColorType.TruecolorWithAlpha };

            using (PsdImage image = (PsdImage)Image.Load(sourceFileName))

            {

                image.Save(outFileName, saveOptions);

            }

            double memoryUsed = (GC.GetTotalMemory(false) / 1024.0) / 1024.0;

            // これらの例ではメモリ使用量は100 MB未満である必要があります

            if (memoryUsed > 100)

            {

                throw new Exception("メモリ使用量が大きすぎます");

            }

{{< /highlight >}}

**PSDNET-158. PSBをPDFとして保存するサポート**

{{< highlight java >}}

 // PSBをPDFとして保存するサポート

    string sourceFileName = "sample.psb";

    using (PsdImage image = (PsdImage)Image.Load(sourceFileName))

    {

        string outFileName = "sample.pdf";

        image.Save(outFileName, new PdfOptions());

    }

{{< /highlight >}}

